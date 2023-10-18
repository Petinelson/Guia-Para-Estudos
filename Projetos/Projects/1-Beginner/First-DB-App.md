# Seu Primeiro App com BD

**Nível:** 1-Iniciante

Entender os conceitos de banco de dados e como usá-los em suas aplicações é
um conhecimento que todos os desenvolvedores precisam adquirir. O objetivo do Seu Primeiro App com BD
é fornecer uma introdução suave aos conceitos de banco de dados e aprender um
caso de uso para bancos de dados em um aplicativo frontend.

Sabia que os navegadores modernos possuem um sistema de gerenciamento de banco de dados
integrado a eles? O IndexedDB está integrado à maioria dos navegadores modernos e fornece aos
desenvolvedores recursos básicos de banco de dados, suporte a transações e persistência entre sessões no lado do cliente.

### Requisitos & Restrições

- O principal caso de uso para um banco de dados baseado em navegador é manter um estado ou
informações de status que precisam persistir entre sessões, ou como uma área de trabalho
para dados temporários. Por exemplo, dados recuperados de um servidor que devem ser
reformatados ou limpos antes de serem apresentados ao usuário.

- É importante ter em mente que, como o ambiente do navegador do lado do cliente
não pode ser protegido, você não deve manter nenhuma informação confidencial ou
informação pessoal identificável (PII) em um banco de dados baseado em navegador.

- A seguinte classe Javascript é fornecida com a funcionalidade que permite
que seu aplicativo inicialmente preencha e limpe o banco de dados do navegador para que você
possa testar a lógica de consulta que adicionará. Será necessário conectar
botões na página da web que você construir às funções `clearDB` e `loadDB`, e
escrever seu próprio manipulador `queryDB` para conectar ao botão `Query DB`. Você também
precisará adicionar uma função `queryAllRows` à classe Customer.

```js
class Customer {
  constructor(dbName) {
    this.dbName = dbName;
    if (!window.indexedDB) {
      window.alert("Your browser doesn't support a stable version of IndexedDB. \
        Such and such feature will not be available.");
    }
  }

  /**
   * Remove all rows from the database
   * @memberof Customer
   */
  removeAllRows = () => {
    const request = indexedDB.open(this.dbName, 1);

    request.onerror = (event) => {
      console.log('removeAllRows - Database error: ', event.target.error.code,
        " - ", event.target.error.message);
    };

    request.onsuccess = (event) => {
      console.log('Deleting all customers...');
      const db = event.target.result;
      const txn = db.transaction('customers', 'readwrite');
      txn.onerror = (event) => {
        console.log('removeAllRows - Txn error: ', event.target.error.code,
          " - ", event.target.error.message);
      };
      txn.oncomplete = (event) => {
        console.log('All rows removed!');
      };
      const objectStore = txn.objectStore('customers');
      const getAllKeysRequest = objectStore.getAllKeys();
      getAllKeysRequest.onsuccess = (event) => {
        getAllKeysRequest.result.forEach(key => {
          objectStore.delete(key);
        });
      }
    }
  }

  /**
   * Populate the Customer database with an initial set of customer data
   * @param {[object]} customerData Data to add
   * @memberof Customer
   */
  initialLoad = (customerData) => {
    const request = indexedDB.open(this.dbName, 1);

    request.onerror = (event) => {
      console.log('initialLoad - Database error: ', event.target.error.code,
        " - ", event.target.error.message);
    };

    request.onupgradeneeded = (event) => {
      console.log('Populating customers...');
      const db = event.target.result;
      const objectStore = db.createObjectStore('customers', { keyPath: 'userid' });
      objectStore.onerror = (event) => {
        console.log('initialLoad - objectStore error: ', event.target.error.code,
          " - ", event.target.error.message);
      };

      // Create an index to search customers by name and email
      objectStore.createIndex('name', 'name', { unique: false });
      objectStore.createIndex('email', 'email', { unique: true });

      // Populate the database with the initial set of rows
      customerData.forEach(function(customer) {
        objectStore.put(customer);
      });
      db.close();
    };
  }
}

// Web page event handlers
const DBNAME = 'customer_db';

/**
 * Clear all customer data from the database
 */
const clearDB = () => {
  console.log('Delete all rows from the Customers database');
  let customer = new Customer(DBNAME);
  customer.removeAllRows();
}

/**
 * Add customer data to the database
 */
const loadDB = () => {
  console.log('Load the Customers database');

  // Customers to add to initially populate the database with
  const customerData = [
    { userid: '444', name: 'Bill', email: 'bill@company.com' },
    { userid: '555', name: 'Donna', email: 'donna@home.org' }
  ];
  let customer = new Customer(DBNAME);
  customer.initialLoad(customerData);
}
```


## Histórias do Usuário

-   [ ] O usuário pode ver uma página da web contendo um painel de controle com três botões - 'Carregar BD', 'Consultar BD' e 'Limpar BD'.
-   [ ] O usuário pode ver um painel de notificações onde mensagens de status serão exibidas.
-   [ ] O usuário pode ver um painel de log rolável onde detalhes de execução que descrevem a operação do aplicativo e a interface com a instância do Cliente serão postados.
-   [ ] O usuário pode ver um histórico contínuo das mensagens do painel de notificações no painel de log.
-   [ ] O usuário pode ver uma área rolável de resultados de consulta onde os dados do cliente recuperados serão exibidos.
-   [ ] O usuário pode clicar no botão 'Carregar BD' para preencher o banco de dados com dados. O botão 'Carregar BD' em sua IU deve estar conectado ao manipulador de eventos `loadDB` fornecido.
-   [ ] O usuário pode ver uma mensagem exibida no painel de notificações quando a operação de carregamento de dados começa e termina.
-   [ ] O usuário pode clicar no botão 'Consultar BD' para listar todos os clientes na área de resultados da consulta. O botão 'Consultar BD' em sua IU deve estar conectado a um manipulador de eventos `queryDB` que você adicionará ao programa.
-   [ ] O usuário pode ver uma mensagem no painel de notificações quando a consulta começa e termina.
-   [ ] O usuário pode ver uma mensagem na área de resultados da consulta se não houver linhas para exibir.
-   [ ] O usuário pode clicar no botão 'Limpar BD' para remover todas as linhas do banco de dados. O botão 'Limpar BD' em sua IU deve estar conectado ao manipulador de eventos `clearDB` fornecido.
-   [ ] O usuário pode ver uma mensagem no painel de notificações quando a operação de limpeza começa e termina.

## Recursos Adicionais

-   [ ] O usuário pode ver botões ativados e desativados de acordo com a tabela a seguir.


    | State               | Load DB  | Query DB | Clear DB |
    |---------------------|----------|----------|----------|
    | Initial App display | enabled  | enabled  | disabled |
    | Load DB clicked     | disabled | enabled  | enabled  |
    | Query DB clicked    | disabled | enabled  | enabled  |
    | Clear DB clicked    | enabled  | enabled  | disabled |
    
-   [ ] O usuário pode ver campos de dados adicionais do Cliente adicionados aos que estão incluídos no código fornecido. O desenvolvedor deve adicionar a data do último pedido e as vendas totais do ano.
-   [ ] O desenvolvedor deve fazer uma retrospectiva sobre este projeto:
    - Quais casos de uso você vê para usar o IndexedDB em seus aplicativos frontend?
    - Quais vantagens e desvantagens você vê em comparação com o uso de um arquivo ou armazenamento local?
    - Em geral, quais critérios você usaria para determinar se o IndexedDB é adequado para o seu aplicativo. (Dica: 100% sim ou não não é uma resposta válida).

## Links e recursos úteis

- [Conceitos de IndexedDB (MDN)](http://tinyw.in/7TIr)
- [Usando IndexedDB (MDN)](http://tinyw.in/w6k0)
- [API do IndexedDB (MDN)](http://tinyw.in/GqnF)
- [Suporte de Navegador para IndexedDB](https://caniuse.com/#feat=indexeddb)

## Projetos de exemplo

- N/a

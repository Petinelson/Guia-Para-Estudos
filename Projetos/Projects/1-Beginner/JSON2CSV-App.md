# JSON2CSV

**Nível:** 1-Iniciante

Desenvolvedores e usuários finais são ambos especialistas em suas respectivas áreas e, portanto, 
cada um fala usando uma linguagem e terminologia específica de seu domínio. Isso também se estende
às ferramentas usadas para manipular dados. Os desenvolvedores encontraram no JSON um método 
universalmente aceito para transferir dados entre aplicações. Os usuários finais, por outro lado, 
dependem de planilhas para organizar e analisar dados.

O objetivo do JSON2CSV é ajudar a criar uma ponte entre JSON e CSV, 
convertendo JSON para CSV para tornar mais fácil revisar os dados em uma planilha. Ele
permite que o usuário cole o JSON em uma caixa de texto para gerar seu CSV equivalente.

### Restrições ###

- Você não pode usar nenhuma biblioteca ou pacote projetado para realizar esse tipo de
conversão.
- Se você optar por implementar isso em JavaScript, não use loops complicados
na sua primeira implementação. Em vez disso, use `Object.keys()` e `Object.values`
para gerar CSV para o cabeçalho e as linhas de dados.
- Estruturas JSON aninhadas não são suportadas.

## Histórias do Usuário

-   [ ] O usuário pode colar a sintaxe JSON em uma caixa de texto
-   [ ] O usuário pode clicar em um botão 'Converter' para validar a caixa de texto JSON e convertê-la para CSV
-   [ ] O usuário pode ver o CSV convertido em outra caixa de texto
-   [ ] O usuário pode ver uma mensagem de aviso se a caixa de texto JSON estiver vazia ou se não contiver JSON válido
-   [ ] O usuário pode clicar em um botão 'Limpar' para limpar o conteúdo de ambas as caixas de texto JSON e CSV.

## Recursos Extras

-   [ ] O usuário pode inserir o caminho para o arquivo JSON no sistema de arquivos local em uma caixa de texto
-   [ ] O usuário pode clicar em um botão 'Abrir' para carregar um arquivo contendo o JSON na caixa de texto
-   [ ] O usuário pode ver uma mensagem de aviso se o arquivo JSON não for encontrado
-   [ ] O usuário pode inserir o caminho do arquivo CSV a ser salvo em uma caixa de texto
-   [ ] O usuário pode clicar em um botão 'Salvar' para salvar o arquivo CSV no sistema de arquivos local
-   [ ] O usuário pode ver uma mensagem de aviso se a caixa de texto CSV estiver vazia ou se a operação de salvar falhou.
-   [ ] O usuário pode converter dados CSV para JSON. Veja [CSV2JSON](./CSV2JSON-App.md)

## Links e recursos úteis

- [Valores Separados por Vírgula (CSV)](https://en.wikipedia.org/wiki/Comma-separated_values)
- [Notação de Objeto JavaScript (JSON)](https://www.json.org/)
- [Objeto Javascript MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)
- [Salvando um arquivo com JS puro](https://codepen.io/davidelrizzo/pen/cxsGb)
- [Lendo arquivos em Javascript](https://codepen.io/jduprey/details/xbale)

## Projetos Exemplo

Tente concluir sua implementação JSON2CSV antes de revisar o(s) projeto(s) exemplo.

- [Conversor de JSON para CSV](https://codepen.io/JFarrow/pen/umjGF)
- [Conversor JSV](https://gpaiva00.github.io/json-csv)

# CSV2JSON

**Nível:** 1-Iniciante

No aplicativo [JSON2CSV](./JSON2CSV-App.md), você converteu JSON para um formato de valor separado por vírgula (CSV). O objetivo do CSV2JSON é inverter esse processo, convertendo um bloco de texto CSV para JSON.

No CSV2JSON, você começará copiando o aplicativo JSON2CSV que criou e depois modificará para permitir a conversão de CSV para JSON, bem como a conversão de JSON para CSV que já está presente. Além de fornecer uma função útil, esse desafio também lhe dará prática em modificar aplicativos existentes para adicionar novas funcionalidades.

### Restrições ###
- Leia atentamente as histórias dos usuários abaixo. Algumas das funcionalidades criadas para JSON2CSV precisarão ser modificadas.
- Você não pode usar bibliotecas ou pacotes projetados para realizar este tipo de conversão.
- Estruturas JSON aninhadas não são suportadas.

## Histórias do Usuário
- [ ] O usuário pode colar a sintaxe CSV em uma caixa de texto
- [ ] O usuário pode clicar em um botão 'Converter para JSON' para validar a caixa de texto CSV e convertê-la para JSON
- [ ] O usuário pode ver uma mensagem de aviso se a caixa de texto CSV estiver vazia ou se não contiver um CSV válido
- [ ] O usuário pode ver o CSV convertido na caixa de texto JSON

### Histórias já implementadas no JSON2CSV 
- [ ] O usuário pode colar a sintaxe JSON em uma caixa de texto
- [ ] O usuário pode clicar em um botão 'Converter para CSV' para validar a caixa de texto JSON e convertê-la para CSV
- [ ] O usuário pode ver uma mensagem de aviso se a caixa de texto JSON estiver vazia ou se não contiver um JSON válido
- [ ] O usuário pode clicar em um botão 'Limpar' para limpar o conteúdo de ambas as caixas de texto JSON e CSV.

## Funcionalidades Bônus
- [ ] O usuário pode inserir o caminho para o arquivo CSV no sistema de arquivos local em uma caixa de texto
- [ ] O usuário pode clicar em um botão 'Abrir CSV' para carregar o arquivo contendo o CSV na caixa de texto
- [ ] O usuário pode ver uma mensagem de aviso se o arquivo CSV não for encontrado
- [ ] O usuário pode clicar em um botão 'Salvar CSV' para salvar o arquivo CSV no arquivo inserido na mesma caixa de texto usada para abrir o arquivo CSV
- [ ] O usuário pode ver uma mensagem de aviso se a caixa de texto CSV estiver vazia ou se a operação de salvar falhar.
- [ ] O usuário pode inserir o caminho para o arquivo JSON no sistema de arquivos local em uma caixa de texto
- [ ] O usuário pode clicar em um botão 'Abrir JSON' para carregar o arquivo contendo o JSON na caixa de texto
- [ ] O usuário pode ver uma mensagem de aviso se o arquivo JSON não for encontrado
- [ ] O usuário pode clicar em um botão 'Salvar JSON' para salvar o arquivo JSON no arquivo inserido na mesma caixa de texto usada para abrir o arquivo JSON
- [ ] O usuário pode ver uma mensagem de aviso se a caixa de texto JSON estiver vazia ou se a operação de salvar falhar.

## Links e recursos úteis
- [Valores Separados por Vírgula (CSV)](https://pt.wikipedia.org/wiki/Comma-separated_values)
- [Notação de Objeto JavaScript (JSON)](https://www.json.org/)
- [Salvando um arquivo com JS puro](https://codepen.io/davidelrizzo/pen/cxsGb)
- [Lendo arquivos em Javascript](https://codepen.io/jduprey/details/xbale)

## Projetos Exemplo
- [Conversor CSV para JSON](https://codepen.io/JFarrow/pen/CAwyo)
- [Conversor JSV](https://gpaiva00.github.io/json-csv)

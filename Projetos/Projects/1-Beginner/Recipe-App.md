# Receita

**Nível:** 1-Iniciante

Talvez você não tenha percebido isso, mas receitas são nada mais do que algoritmos culinários. Como programas, receitas são uma série de etapas imperativas que, se seguidas corretamente, resultam em um prato saboroso.

O objetivo do aplicativo Receita é ajudar o usuário a gerenciar receitas de uma maneira que as torne fáceis de seguir.

### Restrições

- Para a versão inicial deste aplicativo, os dados da receita podem ser codificados como um arquivo JSON. Após implementar a versão inicial deste aplicativo, você pode expandir isso para manter receitas em um arquivo ou banco de dados.

## Histórias do Usuário

-   [ ] O usuário pode ver uma lista de títulos de receitas
-   [ ] O usuário pode clicar em um título de receita para exibir um cartão de receita contendo o título da receita, tipo de refeição (café da manhã, almoço, jantar ou lanche), número de pessoas que serve, seu nível de dificuldade (iniciante, intermediário, avançado), a lista de ingredientes (incluindo suas quantidades) e os passos de preparação.
-   [ ] O usuário pode clicar em um novo título de receita para substituir o cartão atual por uma nova receita.

## Funcionalidades Extras

-   [ ] O usuário pode ver uma foto mostrando como o item fica após ter sido preparado.
-   [ ] O usuário pode buscar por uma receita não na lista de títulos de receita, inserindo o nome da refeição em uma caixa de busca e clicando em um botão 'Pesquisar'. Qualquer API de receita de código aberto pode ser usada como fonte para receitas (veja The MealDB abaixo).
-   [ ] O usuário pode ver uma lista de receitas que correspondem aos termos de busca.
-   [ ] O usuário pode clicar no nome da receita para exibir seu cartão de receita.
-   [ ] O usuário pode ver uma mensagem de aviso se nenhuma receita correspondente foi encontrada.
-   [ ] O usuário pode clicar em um botão 'Salvar' nos cartões para receitas localizadas através da API para salvar uma cópia no arquivo de receitas deste aplicativo ou no banco de dados.

## Links e recursos úteis

- [Usando Fetch](https://developer.mozilla.org/pt-BR/docs/Web/API/Fetch_API/Using_Fetch)
- [Axios](https://www.npmjs.com/package/axios)
- [API The MealDB](https://www.themealdb.com/api.php)

## Projetos Exemplo

- [Caixa de Receitas - um Projeto do Free Code Camp (FCC)](https://codepen.io/eddyerburgh/pen/xVeJvB)
- [Caixa de Receitas em React](https://codepen.io/inkblotty/pen/oxWRme)

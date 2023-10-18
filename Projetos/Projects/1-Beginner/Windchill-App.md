# Sensação Térmica

**Nível:** 1-Iniciante

A sensação térmica combina a temperatura real com a velocidade do vento para calcular
o fator de sensação térmica ou qual é a temperatura percebida versus a temperatura
real.

## Histórias do Usuário

-   [ ] O usuário pode selecionar o sistema de medição em que os cálculos serão realizados - Métrico ou Inglês
-   [ ] O usuário pode inserir a temperatura real e a velocidade do vento
-   [ ] O usuário pode pressionar o botão `Calcular` para exibir a sensação térmica
-   [ ] O usuário receberá uma mensagem de erro quando `Calcular` for clicado se os valores dos dados não forem inseridos

## Funcionalidades Extras

-   [ ] O usuário receberá uma mensagem de erro quando `Calcular` for clicado se o fator de sensação térmica resultante for maior ou igual à temperatura real. Como isso indica um erro interno no cálculo, você também pode satisfazer esse requisito usando uma assertiva
-   [ ] O usuário será solicitado a inserir novos valores de dados se `Calcular` for pressionado sem antes alterar pelo menos um dos campos de entrada
-   [ ] O usuário verá um fator de sensação térmica atualizado sempre que novos valores de temperatura real ou velocidade do vento forem inseridos, sem a necessidade de clicar no botão `Calcular`

## Links e Recursos Úteis

-   [Sensação Térmica no Wikipedia](https://en.wikipedia.org/wiki/Wind_chill)
-   [JavaScript Assert](https://developer.mozilla.org/pt-BR/docs/Web/API/console/assert)

## Projetos Exemplo

[Calculadora de Sensação Térmica](http://www.jsmadeeasy.com/javascripts/Calculators/Wind%20Chill%20Calculator/index.htm)
[Índice de Sensação Térmica em Svelte por Gabriele Corti](https://codepen.io/borntofrappe/pen/WNNrrJg)

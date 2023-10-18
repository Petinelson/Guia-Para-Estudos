# Regressão Pearson

**Nível:** 1-Iniciante

Existem poucas, se houver, aplicações que não requerem algum tipo de 
conhecimento interdisciplinar para implementar funcionalidades úteis para
um usuário. No caso de um aplicativo para a profissão médica, pode ser expertise 
em biologia ou farmacologia. Um fabricante de tintas ou um negócio de ciência agrícola
pode depender de aplicativos com profundo conhecimento em química. E, um 
aplicativo de folha de pagamento certamente incorporará conceitos de RH e contabilidade.

Independente do segmento da indústria que um aplicativo é desenvolvido, uma expertise
comum a todos eles é a matemática. Como desenvolvedor de aplicativos,
você não precisa ser um matemático, mas é útil ter uma compreensão
de como aplicar conceitos matemáticos aos problemas que você está tentando resolver.

O objetivo deste aplicativo é aplicar o Coeficiente de Correlação de Pearson
em dois conjuntos de dados para fornecer ao usuário o grau em que eles
podem ou não estar relacionados. Por exemplo, dado um conjunto de temperaturas e outro
conjunto de preços de carros, isso permitiria ao usuário testar se eles estão relacionados
ou não (alerta de spoiler: eles não estão relacionados!).

### Restrições

- O Desenvolvedor deve programar todos os cálculos sem depender de um pacote.

## Histórias do Usuário

-   [ ] O usuário pode ver um painel de entrada com dois campos de entrada permitindo a inserção de coordenadas `x` 
e `y`, e botões 'Adicionar' e 'Calcular'.
-   [ ] O usuário pode inserir números nessas caixas onde `x` e `y` são observações
dos dois conjuntos de dados.
-   [ ] O usuário pode clicar no botão 'Adicionar' para adicionar o `x` e `y` a uma área tabular
mostrando os pares de observações.
-   [ ] O usuário pode ver uma mensagem de erro se qualquer um dos dois campos de entrada estiverem
vazios ou não contiverem números reais válidos.
-   [ ] O usuário pode ver que o botão 'Calcular' está desativado até que os erros tenham sido
corrigidos.
-   [ ] O usuário pode clicar no botão 'Calcular' para realizar a análise de regressão
e exibir seus resultados.
-   [ ] O usuário pode ver os resultados do cálculo que incluem:
    - Médias aritméticas para as observações `x` e `y`
    - Desvios padrão para as observações `x` e `y`
    - Coeficiente de correlação de Pearson com uma das seguintes interpretações:
      - Sem correlação
      - Neutro
      - Alguma correlação

## Recursos Bônus

-   [ ] O usuário pode ver um gráfico de dispersão das observações
-   [ ] O usuário pode carregar observações de um arquivo em sua máquina local.
-   [ ] O usuário pode ver uma linha de regressão sobrepondo o gráfico de dispersão

## Links e recursos úteis

- [Coeficiente de Correlação de Pearson (Wikipedia)](https://en.wikipedia.org/wiki/Pearson_correlation_coefficient)
- [Regressão Linear](https://en.wikipedia.org/wiki/Linear_regression)
- [Coeficiente de Correlação de Pearson](http://www.code-in-javascript.com/pearsons-correlation-coefficient-in-javascript/)

## Projetos exemplo

[Correlation](https://memory.psych.mun.ca/tech/js/correlation.shtml)

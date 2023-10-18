# CauseEffect

**Nível:** 1-Iniciante

Padrões são fundamentais para a engenharia de software e representam componentes potencialmente reutilizáveis na lógica do programa. No entanto, padrões não são usados apenas para lógica de programa, eles existem em outros domínios, como DevOps, suporte ao usuário e na interface do usuário.

Um padrão comum de interface do usuário é resumir dados em uma seção de uma página que consiste em algum tipo de lista (como texto, imagens ou ícones) que descreve ou categoriza um conjunto de dados. Quando um item da lista é clicado, os dados detalhados por trás dele são exibidos em um painel adjacente na página.

Por exemplo, em um site imobiliário ao clicar em um endereço em uma lista de propriedades à venda, são exibidos os detalhes sobre a propriedade em outra parte da página.

Este desafio exige que o desenvolvedor que o implemente siga estas restrições:

- Você é responsável por criar seus próprios dados de teste. Use um objeto Javascript hardcoded para definir seus dados de teste (veja abaixo).
- Use apenas HTML/CSS/Javascript nativo na sua primeira versão deste app.
- Você pode usar outros pacotes ou bibliotecas ao implementar versões subsequentes.

## Histórias do Usuário

- [ ] O usuário pode ver uma lista de nomes de pessoas organizados verticalmente em um painel de resumo na página.
- [ ] O usuário pode clicar em um nome na lista para atualizar um painel adjacente na página com o nome completo daquela pessoa, endereço, número de telefone e data de nascimento.
- [ ] O usuário pode clicar em outro nome na lista para atualizar o painel de detalhes com as informações dessa pessoa.

## Funcionalidades Bônus

- [ ] O usuário pode ver o nome da pessoa no painel de resumo destacado quando o cursor passa sobre ele.
- [ ] O usuário pode ver o nome da pessoa no painel de resumo destacado usando um efeito de seleção (cor, tamanho, etc.) quando ele é clicado. Este é um efeito diferente do efeito de passar o cursor.
- [ ] O usuário pode ver o efeito de seleção removido de um nome no painel de resumo quando um novo nome é clicado.

## Links e Recursos Úteis

- [Eventos DOM](https://developer.mozilla.org/pt-BR/docs/Web/API/Event)
- Considere definir seus dados de teste em um objeto JavaScript tendo um formato como este:



```
{nome: "...", rua: "...", cidade: "...", estado: "...", pais: "...", telefone: "...", aniversario: "..."},
.
.
.
{nome: "...", rua: "...", cidade: "...", estado: "...", pais: "...", telefone: "...", aniversario: "..."}
];
```


## Projetos Exemplo

Confira a interação entre os itens de Navegação no lado esquerdo da página e o corpo principal da página no [site Javascript MDN](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript).


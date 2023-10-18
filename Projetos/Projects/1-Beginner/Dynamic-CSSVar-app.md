# Variáveis CSS Dinâmicas

**Nível:** 1-Iniciante

As variáveis CSS são uma ferramenta poderosa que permite ao desenvolvedor associar um
nome simbólico a um valor e, em seguida, usar esse nome na folha de estilos onde aquele
valor é necessário. A vantagem é que quando uma mudança nesse valor é 
necessária, ela só precisa mudar na definição da variável CSS em vez de 
nos muitos lugares em que ela pode ser usada.

O que pode tornar isso ainda mais poderoso é mudar dinamicamente o valor de uma
variável CSS em tempo de execução.

O objetivo deste aplicativo é alterar dinamicamente a cor de fundo das caixas de texto
para que você ganhe experiência usando ambas as variáveis CSS e mudando-as dinamicamente 
de dentro do aplicativo.

## Histórias do Usuário

- [ ] O usuário pode ver três caixas para serem usadas para inserir um ID de usuário e uma senha
junto com os botões 'Cancelar' e 'Login' abaixo delas. A cor de fundo padrão
das caixas de texto é branca.
- [ ] O usuário pode inserir um ID de usuário e uma senha nas caixas de texto.
- [ ] O usuário pode clicar no botão 'Login' para validar o ID de usuário e a senha.
- [ ] O usuário pode ver uma mensagem de aviso se uma ou ambas as caixas de texto contêm
espaços e a cor de fundo da caixa de texto vazia mudará para amarelo claro.
- [ ] O usuário pode ver uma mensagem de aviso se o ID do usuário não corresponder a 'testuser'
e a cor de fundo da caixa de texto mudará para vermelho claro.
- [ ] O usuário pode ver uma mensagem de aviso se a senha não corresponder a 'mypassword'
e a cor de fundo da caixa de texto mudará para vermelho claro.
- [ ] O usuário pode clicar no botão 'Cancelar' para limpar as caixas de texto e redefinir
suas cores de fundo para branco.

## Funcionalidades Bônus

- [ ] O usuário pode ver a cor da borda da caixa de texto mudar quando um erro é
detectado
- [ ] O usuário pode ver o tamanho e a fonte do conteúdo da caixa de texto mudar
quando um erro é detectado.

## Links e Recursos Úteis

- [Propriedades personalizadas (--*): variáveis CSS (MDN)](https://developer.mozilla.org/pt-BR/docs/Web/CSS/--*)
- [CSSStyleDeclaration (MDN)](https://developer.mozilla.org/pt-BR/docs/Web/API/CSSStyleDeclaration)

## Projetos Exemplo

[Variáveis CSS Dinâmicas](https://codepen.io/gordawn/pen/oOWBXX)

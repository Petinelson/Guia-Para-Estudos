# Hello

**Nível:** 1-Iniciante

É um dado que as aplicações devem fornecer aos usuários a funcionalidade necessária para realizar alguma tarefa ou objetivo. A eficácia da funcionalidade do aplicativo é o primeiro determinante de como os usuários percebem os aplicativos que usam. No entanto, não é a única coisa que influencia a satisfação do usuário.

As características de Interface do Usuário e Experiência do Usuário (UI/UX) que os desenvolvedores incorporam nos aplicativos têm pelo menos uma influência igual na percepção dos usuários sobre um aplicativo. Pode ser uma simplificação excessiva, mas a UI/UX está em grande parte (mas não totalmente) preocupada com a "forma" dos aplicativos. Personalização é um aspecto da UX que personaliza características e ações para o usuário individual. Personalizar a funcionalidade do aplicativo dessa maneira trabalha para tornar o aplicativo mais fácil e mais agradável de usar.

O objetivo do aplicativo Hello é aproveitar a geolocalização para obter o país do usuário para que ele possa gerar uma saudação personalizada na língua nativa do usuário.

### Restrições

-   Os desenvolvedores devem usar o serviço [IP-API](http://ip-api.com/docs/api:json) para obter o IP do usuário.
-   Os desenvolvedores devem usar o serviço [Fourtonfish](https://www.fourtonfish.com/hellosalut/hello/) para obter a saudação na língua nativa do usuário, passando o IP do usuário.
-   Os desenvolvedores devem usar uma decodificação de entidades HTML para decodificar a mensagem de saudação.

## Histórias do Usuário

-   [ ] O usuário pode ver um painel de login fictício contendo um campo de entrada de nome de usuário, um campo de entrada de senha e os botões 'Login' e 'Logout'.
-   [ ] O usuário pode inserir um nome de login fictício no campo Nome de Usuário.
-   [ ] O usuário pode inserir uma senha fictícia no campo Senha. A entrada deve ser mascarada para que o usuário veja asteriscos (`*`) para cada caractere inserido em vez da senha em texto simples.
-   [ ] O usuário pode clicar no botão 'Login' para realizar um login fictício.
-   [ ] O usuário pode ver uma mensagem se um ou ambos os campos de entrada estiverem vazios e a cor da borda do(s) campo(s) em erro deve ser alterada para vermelho.
-   [ ] O usuário pode ver uma mensagem de reconhecimento de login no formato: `<saudação-na-língua-nativa> <nome-do-usuário> você fez login com sucesso!`
-   [ ] O usuário pode clicar no botão 'Logout' para limpar os campos de entrada de texto e quaisquer mensagens anteriores.
-   [ ] O usuário pode ver uma nova mensagem ao sair com sucesso no formato: `Tenha um ótimo dia <nome-do-usuário>!`

## Recursos adicionais

-   [ ] O usuário pode ver um campo de entrada de texto adicional para um código de idioma que será usado para substituir o IP obtido por geolocalização. Dica: este é um ótimo recurso para testar seu aplicativo.
-   [ ] O usuário pode ver informações adicionais de geolocalização após fazer login que inclui pelo menos o endereço IP local, cidade, região, nome do país, código postal, longitude, latitude e fuso horário.

## Links e recursos úteis

-   [Form Follows Function (Wikipedia)](https://pt.wikipedia.org/wiki/A_forma_segue_a_função)
-   [Personalização (Wikipedia)](https://pt.wikipedia.org/wiki/Personalização)
-   [Fourtonfish](https://www.fourtonfish.com/hellosalut/hello/)
-   [IP-API](http://ip-api.com/docs/api:json)


## Exemplo de Projetos

[Fourtonfish Hello World](https://fourtonfish.com/hellosalut/helloworld/)

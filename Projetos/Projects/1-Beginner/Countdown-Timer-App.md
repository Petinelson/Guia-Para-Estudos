# Cronômetro de Contagem Regressiva

**Nível:** 1-Iniciante

Todos nós temos eventos importantes que esperamos na vida, aniversários,
aniversários e feriados para citar alguns. Não seria bom ter um aplicativo
que conta os meses, dias, horas, minutos e segundos para um evento?
Cronômetro de Contagem Regressiva é exatamente esse aplicativo!

O objetivo do Cronômetro de Contagem Regressiva é fornecer uma exibição constantemente decrescente
dos meses, dias, horas, minutos e segundos para um evento inserido pelo usuário.

### Restrições

- Use apenas funções nativas da linguagem para seus cálculos em vez de confiar
em uma biblioteca ou pacote como [MomentJS](https://momentjs.com/). Isso assume,
claro, que a linguagem de sua escolha tem funções de manipulação de data e tempo adequadas incorporadas.
- Você não pode usar nenhum gerador de código como o site 
[Counting Down To](https://countingdownto.com/). Você deve desenvolver sua
própria implementação original.

## Histórias do Usuário

- [ ] O usuário pode ver uma caixa de entrada de evento contendo um campo de nome do evento, um
campo de data, um horário opcional e um botão 'Iniciar'.
- [ ] O usuário pode definir o evento inserindo seu nome, a data em que está
agendado para acontecer, e um horário opcional do evento. Se o horário for
omitido, assume-se que seja à meia-noite na data do evento no fuso horário local.
- [ ] O usuário pode ver uma mensagem de aviso se o nome do evento estiver em branco.
- [ ] O usuário pode ver uma mensagem de aviso se a data ou hora do evento forem inseridas
incorretamente.
- [ ] O usuário pode ver uma mensagem de aviso se o tempo até a data e hora do evento
que foi inserido ultrapassasse a precisão do cronômetro.
- [ ] O usuário pode clicar no botão 'Iniciar' para ver o cronômetro iniciar
a exibição dos dias, horas, minutos e segundos até o evento acontecer.
- [ ] O usuário pode ver os elementos no cronômetro automaticamente
decrementar. Por exemplo, quando a contagem de segundos restantes chegar a 0, a contagem de 
minutos restantes decrementará em 1 e os segundos começarão a contar regressivamente a partir de 59. Esse progresso deve ocorrer de segundos até a posição de dias restantes na exibição da contagem regressiva.

## Funcionalidades Bônus

- [ ] O usuário pode salvar o evento para que ele persista entre sessões
- [ ] O usuário pode ver um alerta quando o evento for atingido
- [ ] O usuário pode especificar mais de um evento.
- [ ] O usuário pode ver cronômetros para cada evento que foi definido.

## Links e Recursos Úteis

- Imagens de cronômetros de tubo analógico podem ser encontradas 
[aqui](https://nixieshop.com/)
- [`clearInterval` MDN](https://developer.mozilla.org/en-US/docs/Web/API/WindowOrWorkerGlobalScope/clearInterval)
- [`setInterval` MDN](https://developer.mozilla.org/en-US/docs/Web/API/WindowOrWorkerGlobalScope/setInterval)
- [Date MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)

## Projetos Exemplo

[Cronômetro/Temporizador Simples](https://codepen.io/karlo-stekovic/pen/OajKVK)
[Contagem Regressiva feita com React](https://www.florin-pop.com/blog/2019/05/countdown-built-with-react/)

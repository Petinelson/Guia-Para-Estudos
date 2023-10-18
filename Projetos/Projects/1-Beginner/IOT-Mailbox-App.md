# Simulador de Caixa de Correio IOT

**Nível:** 1-Iniciante

O objetivo do Simulador de Caixa de Correio IOT é imitar como uma caixa de correio física habilitada para Internet das Coisas (IOT) pode ser usada para notificá-lo quando a correspondência "tradicional" chegou. Ao fazer isso, ele fornecerá a você experiência no uso de callbacks para comunicar o estado entre diferentes componentes de um aplicativo que são dependentes um do outro.

### Requisitos & Restrições

- Mesmo que este aplicativo seja especificado usando conceitos e terminologias de Javascript, você está livre para implementá-lo no idioma de sua escolha.

- A seguinte classe Javascript é fornecida para iniciar e parar o processo de monitoramento e para sinalizar a página do aplicativo com o estado da porta da caixa de correio (aberta ou fechada) em intervalos predefinidos. Lembre-se de que o intervalo que você especificar não deve exceder o tempo que normalmente leva para abrir ou fechar a porta, ou você pode perder uma entrega!

```
/**
 * Monitor the light levels inside an IOT enabled snail mailbox to detect
 * when the mailbox door has been opened and closed.
 * @class IOTMailbox
 */
class IOTMailbox {
  /**
   * Creates an instance of IOTMailbox.
   * @param {number} [signalInterval=500] Timer interval for checking mailbox status.
   * @param {function} signalCallback Function to invoke when the timer interval expires.
   * @memberof IOTMailbox
   */
  constructor(signalInterval = 500, signalCallback) {
    this.signalInterval = signalInterval;
    this.signalCallback = signalCallback;
    this.intervalID = null;
    this.lastLightLevel = 0;
  }

  /**
   * Start monitoring of the mailbox and invoke the caller specified callback
   * function when the interval expires.
   * @memberof IOTMailbox
   */
  startMonitoring = () => {
    console.log(`Starting monitoring of mailbox...`);
    this.intervalID = window.setInterval(this.signalStateChange, this.signalInterval);
  }

  /**
   * Stop monitoring the mailbox status
   * @memberof IOTMailbox
   */
  stopMonitoring = () => {
    if (this.intervalID === null) return;
    window.clearInterval(this.intervalID);
    this.intervalID = null;
    console.log(`Mailbox monitoring stopped...`);
  }

  /**
   * Pass the current light level inside the mailbox to the users callback
   * function. The positive light levels indicate the door is open while 
   * negative levels indicate it is closed. Depending on the sampling interval 
   * the mailbox door could be in any postion from fully closed to fully open. 
   * This means the light level varies from interval-to-interval.
   * @memberof IOTMailbox
   */
  signalStateChange = () => {
    const lightLevel = this.lastLightLevel >= 0 
      ? Math.random().toFixed(2) * -1 
      : Math.random().toFixed(2);
    console.log(`Mailbox state changed - lightLevel: ${lightLevel}`);
    this.signalCallback(this.lightLevel);
    this.lastLightLevel = lightLevel;
  }
};
```

## Histórias do Usuário

-   [ ] O usuário pode ver uma página da web contendo um painel de controle com três
botões - 'Iniciar Monitoramento', 'Parar Monitoramento' e 'Redefinir'.
-   [ ] O usuário pode ver um painel de notificações onde o status da caixa de correio será exibido.
-   [ ] O usuário pode ver um painel de registro rolável onde os detalhes da execução que descrevem 
a operação do aplicativo e a interface com a instância IOTMailbox serão postados.
-   [ ] O usuário pode clicar no botão 'Iniciar Monitoramento' para começar a receber notificações de estado
da caixa de correio.
-   [ ] O usuário pode ver uma mensagem adicionada ao painel de registro quando o monitoramento começa.
-   [ ] O usuário pode ver uma mensagem adicionada ao painel de registro para o nível de luz passado
através da função de retorno (callback). Isso deve incluir o nível de luz numérico
e se a porta está aberta ou fechada.
-   [ ] O usuário pode ver uma mensagem adicionada ao painel de notificações quando a porta foi
aberta.
-   [ ] O usuário pode clicar no botão 'Parar Monitoramento' para parar de receber notificações de estado
da caixa de correio.
-   [ ] O usuário pode ver uma mensagem adicionada ao painel de registro quando o monitoramento para.

## Recursos Extras

-   [ ] O usuário pode ver o botão 'Iniciar Monitoramento' desativado até que o monitoramento seja
parado.
-   [ ] O usuário pode ver o botão 'Parar Monitoramento' desativado até que o monitoramento seja
iniciado.
-   [ ] O usuário pode ver um campo no painel de controle permitindo que a duração do
intervalo de monitoramento seja especificado.
-   [ ] O usuário pode ver uma mensagem adicionada ao painel de notificações se a porta permanecer
aberta.
-   [ ] O usuário pode ouvir um alerta audível quando a porta é aberta.

## Links e recursos úteis

- [Correio Tradicional (Wikipedia)](https://en.wikipedia.org/wiki/Snail_mail)
- [Internet das Coisas (Wikipedia)](https://en.wikipedia.org/wiki/Internet_of_things)
- [Caixa de Correio IOT: Uma Introdução](https://iotexpert.com/2018/08/13/iot-mailbox-an-introduction/)
- [O que diabos é um Callback?](https://codeburst.io/javascript-what-the-heck-is-a-callback-aba4da2deced)
- [window.setInterval (MDN)](https://developer.mozilla.org/en-US/docs/Web/API/WindowOrWorkerGlobalScope/setInterval)

## Projetos Exemplo

N/a

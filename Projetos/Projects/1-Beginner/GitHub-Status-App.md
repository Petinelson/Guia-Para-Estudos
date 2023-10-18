# GitHub Status

**Nível:** 1-Iniciante

Aplicativos web adquirem dados de várias maneiras. Através da entrada do usuário em páginas web, através de APIs para sistemas backend, de arquivos e bancos de dados e, às vezes, "raspando" sites. O objetivo do aplicativo GitHub Status é apresentar a você uma maneira de raspar informações de outro site.

O GitHub Status utiliza o pacote NPM Request para recuperar o status atual do site GitHub do site [GitHub Status](https://www.githubstatus.com/). O pacote Request permite que sites sejam recuperados não para uma janela de navegador, mas como um documento JSON que pode ser facilmente acessado pelo seu código.

Embora esta especificação de aplicativo dependa fortemente de Javascript, sinta-se à vontade para desenvolvê-lo usando sua linguagem de escolha!

## Histórias do Usuário

-   [ ] O usuário pode ver o status atual para operações Git do GitHub, solicitações de API, problemas operacionais, PRs, painel, projetos, notificações operacionais, gists operacionais e páginas do GitHub operacionais como uma lista na janela principal do aplicativo.
-   [ ] O usuário pode recuperar o status mais recente do site GitHub Status clicando em um botão 'Obter Status'.

## Recursos adicionais

-   [ ] O usuário pode ver qualquer um dos componentes do GitHub que não estejam em status 'Operacional' destacado por uma cor diferente, animação de fundo ou qualquer outra técnica para fazê-lo se destacar. Use sua imaginação!

## Links e recursos úteis

- [Web Scraping (Wikipedia)](https://en.wikipedia.org/wiki/Web_scraping)
- [NPM Request](https://www.npmjs.com/package/request)
- [JSON em Javascript (MDN)](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/JSON)
- [Javascript Object Notation](https://json.org/)
- Dica! Você pode usar o seguinte código para exibir o JSON para a página do site GitHub Status a partir do comando de linha `node ghstatus`. Você pode usar essa saída para determinar quais elementos JSON contêm as informações de status de que você precisará para desenvolver este aplicativo.


```
ghstatus.js

const request = require('request');
request('https://www.githubstatus.com/',  { json: true }, (err, res, body) => {  
    console.log(body);
});
```

## Projetos de exemplo

- [Exemplo de Peter Luczynski](https://peterluczynski.github.io/github-status/)
- [Exemplo de Diogo Moreira](https://diogomoreira.github.io/github-status/)

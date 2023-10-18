# Cifra de Vigenère

**Nível:** 1-Iniciante

A taxa e o impacto das violações de segurança nos últimos anos tornam imperativo que os desenvolvedores entendam os métodos que os atores mal-intencionados usam para comprometer aplicativos. Compreender como um aplicativo pode ser comprometido é o primeiro passo para criar medidas de proteção eficazes.

Uma das maneiras mais fáceis de atores mal-intencionados comprometerem um aplicativo é acessar dados que são deixados sem criptografia pelo desenvolvedor. Existem vários algoritmos de criptografia fortes disponíveis para garantir que os dados não sejam legíveis mesmo que o acesso seja comprometido. Estes incluem AES, Blowfish e TripleDES, para citar alguns.

No entanto, esses algoritmos podem ser bastante complexos para implementar. Então, o objetivo deste aplicativo é implementar um algoritmo de criptografia clássico, a Cifra de Vigenère, para aprender o básico de como as cifras funcionam.

### Requisitos & Restrições

- Os desenvolvedores devem usar apenas os recursos nativos da linguagem para implementar a Cifra de Vigenère. Bibliotecas não são permitidas.
- Os desenvolvedores devem projetar e implementar sua própria solução usando apenas a descrição dos passos no algoritmo da Cifra de Vigenère.
- Após implementar com sucesso este algoritmo, o desenvolvedor deve se fazer as seguintes perguntas:
    - Você se sentiria confiante em criptografar suas informações financeiras usando a Cifra de Vigenère? Por quê?
    - Como você detectaria que uma mensagem foi criptografada usando a Cifra de Vigenère?
    - Como você tentaria quebrar essa criptografia?

## Histórias do Usuário

-   [ ] O usuário pode ver a janela do aplicativo com os seguintes componentes:
    - Campo de entrada para texto simples
    - Campo de entrada para a chave de criptografia
    - Botões de ação - 'Criptografar' e 'Descriptografar'
    - Mensagem resultante criptografada ou descriptografada
-   [ ] O usuário pode inserir o texto a ser criptografado no campo de entrada de texto simples
-   [ ] O usuário pode inserir a chave de criptografia que o algoritmo de Vigenère usará para criptografar a mensagem
-   [ ] O usuário pode ver o botão 'Descriptografar' desativado até que o texto simples tenha sido criptografado
-   [ ] O usuário pode clicar no botão 'Criptografar' para criptografar a mensagem
-   [ ] O usuário pode ver a mensagem criptografada exibida no campo de resultado
-   [ ] O usuário pode ver o botão 'Descriptografar' ativado depois que a mensagem criptografada for exibida
-   [ ] O usuário pode clicar no botão 'Descriptografar' para descriptografar a mensagem criptografada e exibir seu conteúdo no campo de resultado

## Funcionalidades Extras

-   [ ] O usuário pode ver um botão 'Comparar' após a descriptografia que compara a mensagem original em texto simples com a mensagem descriptografada
-   [ ] O usuário pode ver uma mensagem de erro se a 'Comparação' detectar diferenças no conteúdo destes dois campos

## Links e Recursos Úteis

- [Atores Mal-intencionados](http://solutionsreservoir.com/resources/introduction-to-cybersecurity/part-1-cybersecurity-overview)
- [Cifra de Vigenère](https://www.geeksforgeeks.org/vigenere-cipher/)

## Projetos Exemplo

[Criptografia Vigenère](https://codepen.io/max1128/pen/VdyJmd)

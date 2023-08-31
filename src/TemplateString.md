# Template String

## [Voltar](./StrManipulation.md)

Bora lançar aquele texto padrão no nosso chat bot?

```js
let username = prompt("Qual seu nome?");
let credits = prompt("Quantos créditos tem?");

let returnMessage = "Olá " + username + "\nVocê tem " + credits + " créditos";
```

Hmm, mas isso está muito poluído, ai que entra nossa _template string_, que nos ajuda a formatar esse texto de forma mais elegante, permitindo incluir as quebras de linhas e variáveis de maneira melhor:

```js
let userInfo {
    name: '',
    credits: 0
};

userInfo.name = prompt("Qual seu nome?");
userInfo.credits = prompt("Quantos créditos tem?");

let returnMessage = `Olá ${userInfo.name}
Você tem ${userInfo.credits} créditos`;
```

### [Próximo - Set](./Set.md)

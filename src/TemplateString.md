# Template String

## [Voltar](./StrManipulation.md)

Bora lançar aquele texto padrão no nosso chat bot?

```js
let nomeUsuario = prompt("Qual seu nome?");
let creditos = prompt("Quantos créditos tem?");

let retornoMensagem = "Olá " + nomeUsuario + "\nVocê tem " + creditos + " créditos";
```

Hmm, mas isso está muito poluído, ai que entra nossa _template string_, que nos ajuda a formatar esse texto de forma mais elegante, permitindo incluir as quebras de linhas e variáveis de maneira melhor:

```js
let infoUsuario {
    nome: '',
    creditos: 0
};

infoUsuario.nome = prompt("Qual seu nome?");
infoUsuario.creditos = prompt("Quantos créditos tem?");

let retornoMensagem = `Olá ${infoUsuario.nome}
Você tem ${infoUsuario.creditos} créditos`;
```

### [Próximo - Set](./Set.md)

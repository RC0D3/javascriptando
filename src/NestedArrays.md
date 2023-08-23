# Nested Arrays (Arrays aninhadas)

## [Voltar](./Map.md)

Nested arrays são nada mais nada menos que uma array dentro de outra array:

```js
let nomesGatos = ["Tom", "Mel", "Raisco"];
let nomesCachorros = ["Amora", "Thor", "Toby"];

let nomesAnimais = ["Café", "Paçoca", nomesGatos, nomesCachorros];
// ['Café', 'Paçoca', Array(3), Array(3)]

console.log(nomesAnimais[2][2]); // Raisco
```

### [Próximo - Spread Operator](./SpreadOperator.md)

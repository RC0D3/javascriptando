# Spread Operator (Operador espalhador)

## [Voltar](./NestedArrays.md)

Diferente das nested arrays, com este operador(_..._) nós copiamos o valor da array e concatenamos na array atual:

```js
let nomesGatos = ["Tom", "Mel", "Raisco"];
let nomesCachorros = ["Amora", "Thor", "Toby"];

let nomesAnimais = ["Café", "Paçoca", ...nomesGatos, ...nomesCachorros];
// ['Café', 'Paçoca', 'Tom', 'Mel', 'Raisco', 'Amora', 'Thor', 'Toby']

console.log(nomesAnimais[4]); // Raisco
```

Simples e muito útil no dia a dia.

### [Próximo - Destructuring Arrays](./ArrayDestructuring.md)

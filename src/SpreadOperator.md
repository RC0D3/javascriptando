# Spread Operator (Operador espalhador)

## [Voltar](./NestedArrays.md)

Diferente das nested arrays, com este operador(_..._) nós copiamos o valor da array e concatenamos na array atual:

```js
let catNames = ["Tom", "Mel", "Raisco"];
let dogNames = ["Amora", "Thor", "Toby"];

let animalsNames = ["Café", "Paçoca", ...catNames, ...dogNames];
// ['Café', 'Paçoca', 'Tom', 'Mel', 'Raisco', 'Amora', 'Thor', 'Toby']

console.log(animalsNames[4]); // Raisco
```

Simples e muito útil no dia a dia.

### [Próximo - Destructuring Arrays](./ArrayDestructuring.md)

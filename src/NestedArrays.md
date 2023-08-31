# Nested Arrays (Arrays aninhadas)

## [Voltar](./Map.md)

Nested arrays são nada mais nada menos que uma array dentro de outra array:

```js
let catNames = ["Tom", "Mel", "Raisco"];
let dogNames = ["Amora", "Thor", "Toby"];

let animalsNames = ["Café", "Paçoca", catNames, dogNames];
// ['Café', 'Paçoca', Array(3), Array(3)]

console.log(animalsNames[2][2]); // Raisco
// ['Café', 'Paçoca', ['Tom', 'Mel', 'Raisco'], ['Amora', 'Thor', 'Toby']]
```

### [Próximo - Spread Operator](./SpreadOperator.md)

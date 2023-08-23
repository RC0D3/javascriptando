# Spread Operator (Operador espalhador)

## [Voltar](./ObjectLiterals.md)

É basicamente o mesmo exemplo do spread operator com arrays, mas agora com um objeto

```js
const gato = {
    nome: "Raisco",
    som: "Miau!",
    chamado: "Pspspsps"
};

const animal = {
    gato
}; // {gato: {…}}

console.log(animal.gato.nome); // Raisco
```

Porém agora com o spread operator, tornamos as propriedades do outro objeto parte do objeto:

```js
const gato = {
    nome: "Raisco",
    som: "Miau!",
    chamado: "Pspspsps"
};

const animal = {
    ...gato
}; // {nome: 'Raisco', som: 'Miau!', chamado: 'Pspspsps'}

console.log(animal.nome); // Raisco
```

### [Próximo - Destructuring Objects](./ObjectsDestructuring.md)

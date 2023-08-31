# Spread Operator (Operador espalhador)

## [Voltar](./ObjectLiterals.md)

É basicamente o mesmo exemplo do spread operator com arrays, mas agora com um objeto

```js
const cat = {
    name: "Raisco",
    sound: "Miau!",
    call: "Pspspsps"
};

const animal = {
    cat
}; // {cat: {…}}

console.log(animal.cat.name); // Raisco
```

Porém agora com o spread operator, tornamos as propriedades do outro objeto parte do objeto:

```js
const cat = {
    name: "Raisco",
    sound: "Miau!",
    call: "Pspspsps"
};

const animal = {
    ...cat
}; // {name: 'Raisco', sound: 'Miau!', call: 'Pspspsps'}

console.log(animal.name); // Raisco
```

### [Próximo - Destructuring Objects](./ObjectsDestructuring.md)

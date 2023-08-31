# For...of / For...in

## [Voltar](./SpreadOperatorObjects.md)

Todo mundo deve conhecer o **for...in**, ele nos retorna o índice, ou a chave para acessar o elemento:

```js
const test = ["zero", "um", "dois"];

for(const key in test){
    console.log(key);
}
// 0
// 1
// 2
```

Exemplo com um objeto:

```js
const test = {
    zero: 0,
    um: 1,
    dois: 2
};
    
for(const key in test){
    console.log(`${key}:${test[key]}`);
}
// zero:0
// um:1
// dois:2
```

Já o **for...of** retorna o valor correspondente:

```js
const test = ["zero", "um", "dois"];

for(const value of test){
    console.log(value);
}
// "zero"
// "um"
// "dois"
```

### [Próximo - Geradores](./Generators.md)

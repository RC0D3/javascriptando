# For...of / For...in

## [Voltar](./SpreadOperatorObjects.md)

Todo mundo deve conhecer o **for...in**, ele nos retorna o índice, ou a chave para acessar o elemento:

```js
const test = ["zero", "um", "dois"];

for(const chave in test){
    console.log(chave);
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
    
for(const chave in test){
    console.log(`${chave}:${test[chave]}`);
}
// zero:0
// um:1
// dois:2
```

Já o **for...of** retorna o valor correspondente:

```js
const test = ["zero", "um", "dois"];

for(const valor of test){
    console.log(valor);
}
// "zero"
// "um"
// "dois"
```

### [Próximo - Geradores](./Generators.md)

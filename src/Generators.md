# Geradores

## [Voltar](./ForOfForIn.md)

Geradores são bem peculiares em javascript, mas basicamente seria um iterator com um elemento para cada retorno. É controlado de forma manual, bem diferente do que estamos acostumados a ver...

A definição de um gerador é marcada com um _*_ em frente ao keyword da _function_:

```js

function* markerGenerator(){
    yield 1;
    yield 2;
    yield 3;
}

let id = markerGenerator();

id.next().value;
// 1
id.next().value;
// 2
id.next().value;
// 3

```

Mas olha, que interessante, ele também aceita variáveis no seu corpo e parâmetros.

```js

function* markerGenerator(){
    let index = 1;

    while(true){
        yield index++;
    }
}
let id = markerGenerator();

id.next().value;
// 1
id.next().value;
// 2
id.next().value;
// 3 ... assim por diante infinitamente (?)

```

para algo sequencial é deveras interessante, pode ver mais sobre eles na documentação [clicando aqui](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*).

### [Próximo - Introdução a classes](./.md)

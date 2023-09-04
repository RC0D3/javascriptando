# Async / Await

## [Voltar](./Fetch.md)

**Async e await** são um par, basicamente o _async_, diz que uma função é assíncrona.
Já o _await_ diz para o que está dentro da função que deve esperar ser completo para continuar a exeução do código.

Vou dar um exemplo simples:

```js
const delay = (seconds) =>
    new Promise((resolve) => setTimeout(resolve, seconds * 1000))

const count = () => {
    console.log("Zero");
    delay(1);
    console.log("Um");
    delay(2);
    console.log("Dois");
}

count();
```

Rodando esse código, vai perceber que irá printar os 3 consoles instantaneamente, pois ele não está esperando a função delay terminar, para isso serve o async/await:

```js
const delay = (seconds) =>
    new Promise((resolve) => setTimeout(resolve, seconds * 1000))

const count = async() => {
    console.log("Zero");
    await delay(1);
    console.log("Um");
    await delay(2);
    console.log("Dois");
}

count();
```

Rodando este outro exemplo vai ver que antes do log do "Um", ele vai esperar 1 segundo, e para o número dois a mesma coisa, assim certificamos que a operação assíncrona vai ser concluída antes de prosseguir.

PS: Leia-se de passagem que assíncrono seria algo que não ocorre ao mesmo tempo, e não sabemos quanto tempo pode demorar.

### [Próximo - ??](./.md)
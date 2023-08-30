# Pomises

## [Voltar](./GetSet.md)

A queridia dos dev javascript, ela veio para ajudar e muito em requisições ou funções assíncronas, deixando estiloso e fácil lidar com os dados.

Ela é uma classe aonde você instância e recebe dois parâmetros, sendo um opcional.
Primeiro é a resolve e reject (opcional).

```js
const delay = (segundos) => // arrow function
    new Promise((resolve) => // instância a promise com o resolve
        setTimeout(resolve, segundos * 1000) // chama o resolve após 1 segundo
    );

console.log('0 segundos - síncrono');
delay(2).then(() => console.log('2 segundos - assíncrono')); // Chama a promise, e quando ela for resolvida executa o código

// 0 segundos - síncrono
// 2 segundos - assíncrono
```

Agora vamos implementar o reject, que seria quando algo nessa chamada assíncrona der errado.

```js

const delay = (segundos) => // arrow function
    new Promise((resolve, reject) => { // instância a promise com o resolve
        if(typeof segundos !== "number"){
            reject(
                new Error ("Os segundos devem ser do tipo numérico")
            );
        }
        setTimeout(resolve, segundos * 1000) // chama o resolve após 1 segundo
    });

console.log('0 segundos - síncrono');
delay("dois").then(() => console.log('2 segundos - assíncrono')); // Chama a promise, e quando ela for resolvida executa o código
// Porém agora com o parâmetro do tipo incorreto, ela vai jogar um erro na tela.

// 0 segundos - síncrono
// 2 segundos - assíncrono
```

Bora capturar esse erro e tratar, utilizando o método _catch_.

```js
// code
delay("dois")
    .then(() => console.log('2 segundos - assíncrono'))
    .catch((erro) => console.log(`Deu pau no parâmetro bro
    mensagem de erro:
    ${erro}`));


```

### [Próximo - Fetch](./Fetch.md)

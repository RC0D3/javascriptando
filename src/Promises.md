# Pomises

## [Voltar](./GetSet.md)

A queridia dos dev javascript, ela veio para ajudar e muito em requisições ou funções assíncronas, deixando estiloso e fácil lidar com os dados.

Ela é uma classe aonde você instância e recebe dois parâmetros, sendo um opcional.
Primeiro é a resolve e o segundo reject (opcional).

Utilizamos o **then(retornoResolve, retornoReject)** para tratar os dados.
Se utilizarmos apenas uma arrow function nele, seria o mesmo que _then(retornoResolve, null)_

```js
const delay = (seconds) => // arrow function
    new Promise((resolve) => // instância a promise com o resolve
        setTimeout(resolve, seconds * 1000) // chama o resolve após 1 segundo
    );

console.log('0 segundos - síncrono');
delay(2).then(() => console.log('2 segundos - assíncrono')); // Chama a promise, e quando ela for resolvida executa o código

// 0 segundos - síncrono
// 2 segundos - assíncrono
```

Agora vamos implementar o reject, que seria quando algo nessa chamada assíncrona der errado.

```js

const delay = (seconds) => // arrow function
    new Promise((resolve, reject) => { // instância a promise com o resolve
        if(typeof seconds !== "number"){
            reject(
                new Error ("Os segundos devem ser do tipo numérico")
            );
        }
        setTimeout(resolve, seconds * 1000) // chama o resolve após 1 segundo
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
    .catch((error) => console.log(`Deu pau no parâmetro bro
    mensagem de erro:
    ${error}`));


```

Também podemos retornar parâmetros quando resolvida, para tratarmos dados ou afins.

```js
const myJson = new Promise((resolve) => {
    setTimeout(() => {
        resolve({
        "name": "Pedro",
        "age": 21,
        "description": "Estudante na Federal"
    })
    }, 2000)
});

myJson().then((data) => console.log(data));

// {nome: 'Pedro', idade: 21, descricao: 'Estudante na Federal'}
```

Agora que tal pegarmos dados de verdade? Vamos utilizar a api do github. Exemplo aprimorado da aula [Destructuring Objects](./ObjectsDestructuring.md)

```js
const getUserInformation = (user) => {
    return new Promise((resolve, reject) => {
        const apiURL = `https://api.github.com/users/${user}`; // Define URL da API
        const request = new XMLHttpRequest(); // Cria objeto para tratar da requisição
        request.open("GET", apiURL); // Define o método e a URL

        request.onload = () => { // Quando carregar a requisição
            if(request.status === 200){ // Verifica se deu tudo OK
                resolve(JSON.parse(request.response)); // Retorna o JSON
            }else{
                reject(Error(request.status)); // Mostra o http code
            }
        };
        request.onerror = (error) => reject(error); // Mostra qualquer outro erro da requisição caso aconteça
        request.send();
    })
};



function showUserImage({login, avatar_url, created_at}){
    
    writeOnSite(login);

    let img = document.createElement("img");
    img.src = avatar_url;


    const p = document.createElement("p");
    const textNodeP = document.createTextNode(created_at);
    p.appendChild(textNodeP);


    document.getElementsByTagName('body')[0].appendChild(img);
    document.getElementsByTagName('body')[0].appendChild(p);
}

function writeOnSite(message){
    const h1 = document.createElement("h1");
    const textNode = document.createTextNode(message);
    h1.appendChild(textNode);
    document.getElementsByTagName('body')[0].appendChild(h1);
}

getUserInformation("RC0D3")
    .then((userInformation) => showUserImage(userInformation));
```

Porém se mandarmos um usuário que não existe? Bora tratar esse erro!

```js
// Code...

getUserInformation("RC0D3;USERNOTFOUND_. 123")
    .then((userInformation) => showUserImage(userInformation))
    .catch((error) => {
        if(error.message == "404") writeOnSite("Usuário não encontrado!")
        else writeOnSite("Erro inesperado.")
    });
```

ou:

```js
// Code...

getUserInformation("RC0D3;USERNOTFOUND_. 123")
    .then(
        (userInformation) => showUserImage(userInformation),
        (error) => {
            if(error.message == "404") writeOnSite("Usuário não encontrado!")
            else writeOnSite("Erro inesperado.")
        }
    );
```

### [Próximo - Fetch](./Fetch.md)
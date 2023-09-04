# Fetch

## [Voltar](./Promises.md)

Diferente das _XMLHttpRequest_ o **fetch** é baseado em promisses. No PHP seria equivalente ao nosso Curl.

Vamos subsituir nosso _XMLHttpRequest_ pelo nosso **fetch** na chamada da api.

```js

const getUserInformation = (user) => {
    return fetch(`https://api.github.com/users/${user}`);
};

function showUserImage({login, avatar_url, created_at}){//Código}
function writeOnSite(message){//Código}

getUserInformation("RC0D3")
            .then((res) => {
                if (res.status == "404") {
                    throw new Error("Usuário não encontrado!")
                } else if (!res.ok) {
                    throw new Error("Erro inesperado.")
                }

                return res
            })
            .then((res) => res.json()) // pega o json do body da requisição
            .then(showUserImage) // manda para a função
            .catch((error) => writeOnSite(error.message))
```

Ficou bem mais compacta e ainda continua funcionando.

### [Próximo - Async / await](./AsyncAwait.md)
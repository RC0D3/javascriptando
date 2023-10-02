# Filter

## [Voltar](./IncludeInArray.md)

Como o próprio nome diz, **_filter_**, será aplicado um filtro, este recebe uma função a qual precisa retornar verdadeiro ou falso. Assim o que cair na condição falsa, é ignorado da nova cópia do array.

```js
let clients = ["RC0D3", "Daniel He4rt", "Filipe Deschaps", "Fábio Akita", "Alan"];

const VIPClients = clients.filter((client) => client.length <= 5); // Cliente com nome igual ou menor que cinco

console.log(VIPClients);
// (2) ['RC0D3', 'Alan']
```

Outro exemplo útil:

```js
let words = ["Linguagem C", "Linguagem C#", "Linguagem F#", "Linguagem C++", "Linguagem PHP", "Linguagem Python"];

function searchItems(array, query){
    return array.filter((item) => item.toLowerCase().includes(query.toLowerCase()));
}


console.log(searchItems(words, "P"));
//(2) ['Linguagem PHP', 'Linguagem Python']
```

### [Próximo - Objetos literais](./ObjectLiterals.md)

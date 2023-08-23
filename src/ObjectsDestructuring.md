# Destructuring Arrays (Desestruturando arrays)

## [Voltar](./SpreadOperatorObjects.md)

Este é altamente interessante, desestruturar um objeto, porém diferente das arrays ande cada um equivale à um índice, aqui podemos escolher qual índice iremos extrair:

```js
let jsonObject = { 
    login: "RC0D3",
    avatar_url: "https://avatars.githubusercontent.com/u/19766549?v=4",
    url: "https://api.github.com/users/RC0D3", // API do Github
    subscriptions_url: "https://api.github.com/users/RC0D3/subscriptions",
    organizations_url: "https://api.github.com/users/RC0D3/orgs",
    repos_url: "https://api.github.com/users/RC0D3/repos",
    type: "User",
    public_repos: 4,
    public_gists: 1,
    followers: 2,
    following: 6,
    created_at: "2016-06-05T23:07:22Z",
    updated_at: "2023-08-10T18:23:04Z"
};

function showUserImage({login, avatar_url, created_at}){
    const h1 = document.createElement("h1");
    const textNode = document.createTextNode(login);
    h1.appendChild(textNode);

    let img = document.createElement("img");
    img.src = avatar_url;


    const p = document.createElement("p");
    const textNodeP = document.createTextNode(created_at);
    p.appendChild(textNodeP);

    document.getElementsByTagName('body')[0].appendChild(h1);
    document.getElementsByTagName('body')[0].appendChild(img);
    document.getElementsByTagName('body')[0].appendChild(p);
}

showUserImage(jsonObject);

```

Assim nossa extração de dados fica muito mais bonita e simplifica na criação das variaveis locais.

### [Próximo - For...of / for..in](./ForOfForIn.md)

# String Manipulation

## [Voltar](./Const.md)

Nossas queridas strings, nosso canhão para matar baratas kkk, serve para tudo. Mas é sem sabermos manipulá-las adequadamente não conseguimos trabalhar com elas de forma eficiente, então bora ver como utilziar no dia a dia!

Essa é muito útil quando estamos fazendo aquele chat bot básico hehe

Famoso _startsWith_ aonde ele verifica se o início da string é igual ao que precisamos

```js
const PrefixoComando = "/";

let comando = prompt("Chat bot, insira o que preisa:");

function Principal(){
    if(!VerificarComandoVálido()){
        return; // Early Return
    }

    //Comandos
}
Principal();
function VerificarComandoVálido (){
    return comando.startsWith(PrefixoComando);
}
```

Também temos o inverso, o _endsWith_ que compara o final da string se é igual ao que passamos

```js

let comando = prompt("Chat bot, insira o que preisa:");

if(comando.endsWith('refrigerante')){
    console.log('Desculpe, eu sou apenas um chat bot e não consigo consumir alimentos/bebidas');
}
```

E se quisermos um texto em qualquer lugar da string? Temos o _includes_

```js

let texto = "Vaca marrom pulou o portão";

console.log(texto.includes("pulo")); // Retorna true pois existe no texto

```

Agora se quisermos saber exatamente a posicão deste texto, podemos utilizar o _search_, ele também aceita regex, pode ver mais [clicando aqui](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/search)

> Lembrando que a contagem inicia do número 0

```js

let texto = "eu pulo na cama";

console.log(texto.search("pulo")); // Retorna 3, a posição de início dele

```

Para repetirmos um texto, também há um função o _repeat(quantidade)_

```js

let gato = "miau ";

console.log(gato.repeat(5)); // miau miau miau miau miau 

```

### [Próximo - Template String](./TemplateString.md)

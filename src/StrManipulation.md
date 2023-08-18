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

if(comando.endsWith('Refrigerante')){
    console.log('Desculpe, eu sou apenas um chat bot e não consigo consumir alimentos/bebidas');
}
```

### [Próximo - Template String](./.md)

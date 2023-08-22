# Set's

## [Voltar](./TemplateString.md)

Hmm que tal uma coleção de dados? Poisé eles existe, e tem algumas peculiaridades este, em particular:

>- Aceita apenas tipos [primitivos](https://developer.mozilla.org/en-US/docs/Glossary/Primitive) (strings, números, etc) ou referências a objetos
>- Não duplica dados

Com essa coleção de dados podemos fazer um removedor de linhas duplicadas:

```html
<html>
    <head>
        <script>
            function removerDuplicados(){
                let texto = document.getElementById('textarea'); //Pega o textarea
                let novoTexto = new Set(texto.value.split('\n')); //Pega o texto dele e quebra em uma array baseado nas qubras de linha e joga no Set
                texto.value = [...novoTexto].join('\n'); // Transforma o Set em uma array e depois concatena tudo com a quebra de linha novamente
                //Assim o Set remove as linhas duplicadas e devolvemos ao texto
            }
        </script>
    </head>
    <body>
        <textarea id='textarea'></textarea>
        <br>
        <button onclick='removerDuplicados()'>Remover Duplicados</button>

    </body>
</html>
```

Mas voltando ao básico dessa coleção, ela possuí alguns métodos como:

- **add(value)** que adiciona um elemento para a coleção
- **has(value)** que verifica se existe um item na coleção
- **delete(value)** que remove um item da coleção
- **clear()** limpa toda a coleção

E também uma propriedade

- **size** retorna quantos itens há dentro da coleção

```js
let setmaroto = new Set('casa', 'carro');

setmaroto.add('comida'); // setmaroto = {'casa', 'carro', 'comida'}

setmaroto.has('casa'); // true

setmaroto.add('casa'); // setmaroto = {'casa', 'carro', 'comida'}

setmaroto.delete('casa'); // setmaroto = {'carro', 'comida'}

setmaroto.size; // 2

setmaroto.clear(); // setmaroto = {}
```

Agora você está apto para dar uma olhadinha nos demais tipos de coleções que seráo bastante importantes! 😉

### [Próximo - Map](./Map.md)

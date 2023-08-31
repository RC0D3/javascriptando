# Objetos literais

## [Voltar](./IncludeInArray.md)

Que tal voltarmos um pouquinho no exemplo de [Desestruturando arrays](./ArrayDestructuring.md), vemos que há repetição no objeto _jsonOrder_ no nome da variável

```js
// Código
function orderToJson([client, ...ingredientes]){
    let jsonOrder = {
        this.client: client,          // <<<
        this.ingredients: ingredients // <<<
    };

    // Código
}
```

Para não ter essa reptição e também ficar mais legível, podemos transformar o que recebemos na própria propriedade:

```js
// Código
function orderToJson([client, ...ingredients]){
    let jsonOrder = {
        client,
        ingredients
    };

    // Código
}
```

Assim o próprio javascript define o nome da variavel do objeto como a propriedade e o valor dela como o valor da propriedade

### [Próximo - Spread Operator com Objetos](./SpreadOperatorObjects.md)

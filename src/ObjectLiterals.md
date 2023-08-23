# Objetos literais

## [Voltar](./IncludeInArray.md)

Que tal voltarmos um pouquinho no exemplo de [Desestruturando arrays](./ArrayDestructuring.md), vemos que há repetição no objeto _pedidoJson_

```js
// Código
function transformarPedido([cliente, ...ingredientes]){
    let pedidoJson = {
        this.cliente: cliente,          // <<<
        this.ingredientes: ingredientes // <<<
    };

    // Código
}
```

Para não ter essa reptição e também ficar mais legível, podemos transformar o que recebemos na própria propriedade:

```js
// Código
function transformarPedido([cliente, ...ingredientes]){
    let pedidoJson = {
        cliente,
        ingredientes
    };

    // Código
}
```

Assim o próprio javascript define o nome da variavel do objeto como a propriedade e o valor dela como o valor da pripriedade

### [Próximo - Spread Operator com Objetos](./SpreadOperatorObjects.md)

# Destructuring Arrays (Desestruturando arrays)

## [Voltar](./SpreadOperator.md)

Essa dica vale ouro! Desestruturar arrays pode-se dizer que é pareciado ao list() do PHP, pois damos nomes ao elementos de um array.

```js
let [numero1, operador, numero2] = [5, "+", 5];
if(operador == "+")
    console.log(`A conta é: ${numero1} ${operador} ${numero2} = ${numero1 + numero2}`);
if(operador == "-")
    console.log(`A conta é: ${numero1} ${operador} ${numero2} = ${numero1 - numero2}`);
```

Agora um exemplo mais prático, adicionando a propriedade "rest", que adicionamos o resto da array em outro local. É utilizada como spread operator (_..._)

```js
let dadosPedido = ["RC0D3", "Pão", "Carne", "Tomate", "Alface", "Pão"];
let dadosPedido2 = ["Daniel He4rt", "Pão", "Carne", "Carne", "Tomate", "Alface", "Cebola", "Pão"];


function transformarPedido([cliente, ...ingredientes]){
    let pedidoJson = {
        this.cliente: cliente,
        this.ingredientes: ingredientes
    };

    pedidoJson = JSON.stringify(pedidoJson);

    console.log(pedidoJson);

}
transformarPedido(dadosPedido);
// {"nome":"RC0D3","ingredientes":["Pão","Carne","Tomate","Alface","Pão"]}
transformarPedido(dadosPedido2);
// {"nome":"Daniel He4rt","ingredientes":["Pão","Carne","Carne","Tomate","Alface","Cebola","Pão"]}

```

### [Próximo - Destructuring Arrays](./ArrayDestructuring.md)

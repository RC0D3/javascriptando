# Destructuring Arrays (Desestruturando arrays)

## [Voltar](./SpreadOperator.md)

Essa dica vale ouro! Desestruturar arrays pode-se dizer que é pareciado ao list() do PHP, pois damos nomes ao elementos de um array.

```js
let [number1, operator, number2] = [5, "+", 5];
if(operator == "+")
    console.log(`A conta é: ${number1} ${operator} ${number2} = ${number1 + number2}`);
if(operator == "-")
    console.log(`A conta é: ${number1} ${operator} ${number2} = ${number1 - number2}`);
```

Agora um exemplo mais prático, adicionando a propriedade "rest", que adicionamos o resto da array em outro local. É utilizada como spread operator (_..._)

```js
let orderData = ["RC0D3", "Pão", "Carne", "Tomate", "Alface", "Pão"];
let orderData2 = ["Daniel He4rt", "Pão", "Carne", "Carne", "Tomate", "Alface", "Cebola", "Pão"];


function orderToJson([client, ...ingredients]){
    let jsonOrder = {
        this.client: client,
        this.ingredients: ingredients
    };

    jsonOrder = JSON.stringify(jsonOrder);

    console.log(jsonOrder);

}
orderToJson(orderData);
// {"nome":"RC0D3","ingredientes":["Pão","Carne","Tomate","Alface","Pão"]}
orderToJson(orderData2);
// {"nome":"Daniel He4rt","ingredientes":["Pão","Carne","Carne","Tomate","Alface","Cebola","Pão"]}

```

### [Próximo - Pesquisando na array](./IncludeInArray.md)

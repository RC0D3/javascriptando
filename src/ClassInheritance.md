# Herança de classes

## [Voltar](./ClassIntroduction.md)

Conceito muito utilizado em programação orientada a objetos (POO) é a herança de classes, aonde ela herda(recebe) todos os métodos da classe pai.

Marcada pela expressão _extentds_ após o nome da classe, indicando na frente o nome da classe a qual vai herdar.

```js

class Calculator {
    constructor(){ // Método construtor chamado ao instânciar nova classe
        console.log("Estou pronto para somar!")
    }
    /* Funções */
    sum(number, number2){
        return number + number2;
    }

    subtraction(number, number2){
        return number - number2;
    }

    division(number, number2){
        return number / number2;
    }
    
    multiplication(number, number2){
        return number * number2;
    }

}

class ScientificCalculator extends Calculator {
    squareRoot(number){
        return Math.sqrt(number);
    }

    square(number, power){
        return Math.pow(number, power);
    }
}

const calc = new ScientificCalculator();
// "Etou pronto para somar!"

console.log(calc.sum(5,19)); // 24

console.log(calc.square(3,2)); // 3² = 9

```

> Caso seja necessário utilizar constructor na classe que herda, precisamos chamar o construtor da classe pai, utilizando a expressão _super_.

```js
class ScientificCalculator extends Calculator {
    
    constructor(){
        super(); // Chama o construtor da classe pai (Calculadora)
        console.log("e realizar outras operações!")
    }
    
    // Código...
}
// Estou pronto para somar!
// e realizar outras operações!
```

### [Próximo - Getters and setters](./GetSet.md)

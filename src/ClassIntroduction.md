# Introdução à classes

## [Voltar](./Generators.md)

Você já deve ter visto classes em outras linguagens, no javsacript é bastante parecido sua estrutura, vamos dar uma olhada melhor.

```js
class Calculator {
    constructor(name){ // Método construtor chamado ao instânciar nova classe
        this.name = name;
        console.log(`Estou pronto para somar ${this.name}!`);
    }
    /* Funções */
    sum(number, number2){
        return number + number2;
    }

    subtraction(number, number2){
        return number - number2;
    }

}

const calc = new Calculator('RC0D3');
// "Etou pronto para somar nome!"

console.log(calc.soma(5,19)); // 24
```

### [Próximo - Herança de classes](./ClassInheritance.md)

# Herança de classes

## [Voltar](./ClassIntroduction.md)

Conceito muito utilizado em programação orientada a objetos (POO) é a herança de classes, aonde ela herda(recebe) todos os métodos da classe pai.

Marcada pela expressão _extentds_ após o nome da classe, indicando na frente o nome da classe a qual vai herdar.

```js

class Calculadora {
    constructor(){ // Método construtor chamado ao instânciar nova classe
        console.log("Estou pronto para somar!")
    }
    /* Funções */
    soma(numero, numero2){
        return numero + numero2;
    }

    subtracao(numero, numero2){
        return numero - numero2;
    }

    divisao(numero, numero2){
        return numero / numero2;
    }
    
    multiplicacao(numero, numero2){
        return numero * numero2;
    }

}

class CalculadoraCientifica extends Calculadora {
    raizQuadrada(numero){
        return Math.sqrt(numero);
    }

    elevarNumero(numero, potencia){
        return Math.pow(numero, potencia);
    }
}

const calc = new CalculadoraCientifica();
// "Etou pronto para somar!"

console.log(calc.soma(5,19)); // 24

console.log(calc.elevarNumero(3,2)); // 3² = 9

```

> Caso seja necessário utilizar constructor na classe que herda, precisamos chamar o construtor da classe pai, utilizando a expressão _super_.

```js
class CalculadoraCientifica extends Calculadora {
    
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

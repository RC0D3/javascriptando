# Introdução à classes

## [Voltar](./Generators.md)

Você já deve ter visto classes em outras linguagens, no javsacript é bastante parecido sua estrutura, vamos dar uma olhada melhor.

```js

class Calculadora {
    constructor(nome){ // Método construtor chamado ao instânciar nova classe
        this.nome = nome;
        console.log(`Estou pronto para somar ${this.nome}!`);
    }
    /* Funções */
    soma(valor, valor2){
        return valor + valor2;
    }

    subtracao(valor, valor2){
        return valor - valor2;
    }

}

const calc = new Calculadora();
// "Etou pronto para somar nome!"

console.log(calc.soma(5,19)); // 24


```

### [Próximo - Herança de classes](./ClassInheritance.md)

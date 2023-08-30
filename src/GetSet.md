# Getters and setters

## [Voltar](./ClassInheritance.md)

Esse também bastante popular, porém em algumas linguagens tem muita "overengineering"  (vulgo java, farpas), utilizando eles sem necessidades.

Getters e setters servem para alteramos os dados antes de inserirmos ou recebê-los.

```js

class Banco {

    constructor(dinheiro){
        this.valor = dinheiro;
    }

    get dinheiro(){
        return new Intl.NumberFormat('pt-BR', {
                                    style: 'currency',
                                    currency: 'BRL',
        }).format(this.valor); // Formata para o padrão brasileiro de moedas
    }

    set definirDinheiro(valor){
        this.valor = valor;
    }
    
}

const conta = new Banco(1000);

console.log(conta.dinheiro); // R$ 1.000,00

conta.definirDinheiro = 500;

console.log(conta.dinheiro); // R$ 500,00

```

> Podem também ser utilizados em objetos


### [Próximo - Promises](./Promises.md)

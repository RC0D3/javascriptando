# Getters and setters

## [Voltar](./ClassInheritance.md)

Esse também bastante popular, porém em algumas linguagens tem muita "overengineering"  (vulgo java, farpas), utilizando eles sem necessidades.

Getters e setters servem para alteramos os dados antes de inserirmos ou recebê-los.

```js

class Bank {
    constructor(money){
        this.value = money;
    }

    get money(){
        return new Intl.NumberFormat('pt-BR', {
                                    style: 'currency',
                                    currency: 'BRL',
        }).format(this.value); // Formata para o padrão brasileiro de moedas
    }

    set setMoney(value){
        this.value = value;
    }
}

const accountBank = new Banco(1000);

console.log(accountBank.money); // R$ 1.000,00

conta.setMoney = 500;

console.log(accountBank.money); // R$ 500,00

```

> Podem também ser utilizados em objetos


### [Próximo - Promises](./Promises.md)

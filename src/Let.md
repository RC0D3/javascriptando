# Let

## [Voltar](../READMEPT.md)

Nosso querido _let_ serve para limitarmos por escopo.

Mas o que é um escopo? Fica a pergunta.

Um escopo é limitado no javascript pelos blocos que ficam entre as chaves, como no código abaixo:

```js
    //Escopo global
    let estouNoEscopoGlobal = true;
    if (estouNoEscopoGlobal){
        //Escopo local deste if
        let estouNoEscopoLocal = true;
    }
```

Isto é muito útil em dois casos, primeiro quando temos uma arquivo muito grande, assim não dá conflito de nomes por escopo.
E quando há mais de um arquivo sendo lido junto
> Por exemplo quando adicionamos dois script em uma página cada um com sua função  

### [Próximo - Const](./Const.md)

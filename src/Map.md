# Map's

## [Voltar](./Set.md)

Mais e mais coleções, vamos ver uma das mais utilizadas!

Nosso querido _Map_, ele é similar com o Set, porém aceita outros tipos de dados, seria como um dicionário genérico em outra linguagens, pois recebe uma key e um value.

Ele possuí alguns métodos como:

- **set(key, value)** que adiciona um elemento para a coleção
- **get(key)** retorna o valor do elemento
- **has(key)** que verifica se existe um item na coleção
- **delete(key)** que remove um item da coleção
- **clear()** limpa toda a coleção
- **entries()** retorna os arrays com [key, value]
- **values()** retorna apenas os valores
- **keys()** retorna apenas as chaves/índices

E também uma propriedade assim como o Set

- **size** retorna quantos itens há dentro da coleção

```js
let mapmaroto = new Map([
    ['casa', 'carro'],
    ['mansão', 'iate']
]);

mapmaroto.set('casebre', 'bicicleta'); // mapmaroto = {'casa' => 'carro', 'mansão' => 'iate', 'casebre' => 'bicicleta'}

mapmaroto.has('casa'); // true

mapmaroto.set('casa', {hasCar: true}); // mapmaroto = {'casa' => {…}, 'mansão' => 'iate', 'casebre' => 'bicicleta'}

mapmaroto.delete('casa'); //retorna true | mapmaroto = {'mansão' => 'iate', 'casebre' => 'bicicleta'}

mapmaroto.size; // 2

for(const map of mapmaroto.entries()){
    console.log(map);
    //['mansão', 'iate']
    //['casebre', 'bicicleta']
}

/*
const iterator = mapmaroto.entries();

console.log(iterator1.next().value);
// Array ["0", "foo"]

console.log(iterator1.next().value);
// Array [1, "bar"]
*/

for(const value of mapmaroto.values()){
    console.log(value);
    //'iate'
    //bicicleta
}

for(const key of mapmaroto.keys()){
    console.log(key);
    //'mansão'
    //'casebre'
}

mapmaroto.clear(); // mapmaroto = {}
```

### [Próximo - Nested Arrays](./NestedArrays.md)

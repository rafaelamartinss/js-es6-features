# ES6 Features
Uma coleção de funcionalidades do ES6 (ECMAScript 2015). Essa lista foi inspirada no curso do [Willian Justen](https://github.com/willianjusten), 
[JS com TDD na Prática](https://www.udemy.com/course/js-com-tdd-na-pratica/).

*Leia em outros idiomas: [English](README.en.md).

## Funcionalidades
  - [Array](#array)
  - [Recomendações](#recomendações)
    - [Array From](#array.from)
    - [Array Fill](#array.fill)
    - [Array Of](#array.of)
    - [Array Find](#array.find)
    - [Array FindIndex](#array.findIndex)
  - [Shorthand ](#shorthand)



## Recomendações
- [Mais sobre os métodos](https://exploringjs.com/es6/ch_arrays.html#sec_new-static-array-methods) (inglês)
- [Array vs. Objeto](https://dev.to/zac_heisey/objects-vs-arrays-2g0e) (inglês)

## Array
Antes de tudo, quando usamos array? O array é recomendado quando se quer criar coleções ordenadas, em única variável,
onde seus items podem ser acessados por sua posição númerica na lista. 

### Array.from
Esse método retorna um array de qualquer objeto com a propriedade *length* ou que seja uma objeto iterável. 
Ainda dentro desse método é possível já mapear o array que será retornado.

```javascript
let arr = Array.from(object, mapFunction, thisValue);
```
#### Exemplos
##### Array from com string
```javascript
let arr = Array.from('github');

// ['g', 'i', 't', 'h', 'u', 'b']
```
##### Array from usando o método map
```javascript
let arr = Array.from([1, 2, 3], x => x + x);

// [2, 4, 6] 
```
*Mais sobre: [Array.from()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/from)*
### Array.fill
Preenche todos os elementos de um array com um valor estático, começando pelo primeiro elemento, de index 0, e terminando no último, 
por padrão. Retorna o array modificado.
```javascript
const sandwich = ['cheese', 'bread', 'meat'];

sandwich.fill('tomato');
// ['tomato', 'tomato', 'tomato']
```
 É possível especificar as posições de ínicio e fim.
 
 ```javascript
 const nums = [3, 4, 5, 7, 8];
 
 nums.fill(0, 1, 3);
 // [3, 0, 0, 7, 8]
 ```

*Mais sobre: [Array.fill()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/fill)*
### Array.of
Cria um novo array de acordo com os argumentos passados, independente do tipo dos argumentos;
```javascript
const array = Array.of(1, 5, 'Jhon', {name: 'Doe'});

// [1, 5, "Jhon", {name: "Doe"}] 
```
*Mais sobre: [Array.of()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/of)*
### Array.find
O método *find* retorna o valor do primeiro elemento que satifaz as condições definidas na função de teste.
```javascript
const years = [2019, 2020, 2021, 2022];
const yearFound = years.find(item => item > 2020);

// 2019  
```
*Mais sobre: [Array.find()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find)*
### Array.findIndex
Retorna o valor do index do primeiro elemento que satifaz as condições definidas na função de teste.

```javascript
const sampleArray = [4, -5, 0, -1];
const underZeroIndex = sampleArray.findIndex(x => x < 0);
// 1
```
*Mais sobre: [Array.findIndex()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex)*

## Shorthand
Em tradução direta o "código abreviado" é um conjunto de técnicas, para tornar funções, 
validações, atribuição para propriedades de objetos, e muito mais, menores.
Um exemplo disso é o if...else.
```javascript
let egg;

if (x > 10) {
  egg = true;
} else {
  egg = false;
}

//Abreviado (Shorthand)
let egg = (x > 10) ? true : false;

// ou ainda
let egg = (x > 10);
```

*Mais sobre: [Javascript Shorthand Coding Techniques](https://gist.github.com/pongstr/9f273cdfbd5b600bc758)*

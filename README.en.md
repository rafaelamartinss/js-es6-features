# ES6 Features
A collection of cool features of ES6 (ECMAScript 2015). This cheat sheet was 
inspired by [Willian Justen](https://github.com/willianjusten)'s course, named 
[JS com TDD na Prática](https://www.udemy.com/course/js-com-tdd-na-pratica/) (JS with TDD in Practice).

*Read this in other languages: [Portuguese](README.md).

##Features
  - [Array](#array)
    - [Recommendations](#recommendations)
    - [Array From](#array.from)
    - [Array Fill](#array.fill)
    - [Array Of](#array.of)
    - [Array Find](#array.find)
    - [Array FindIndex](#array.findIndex)

## Array
When should we use arrays? When we want create and store a list of elements in a single variable. 
Where these elements can be accessed by their numerical position in the list.

###Recommendations
- [More about methods](https://exploringjs.com/es6/ch_arrays.html#sec_new-static-array-methods)
- [Array vs. Objeto](https://dev.to/zac_heisey/objects-vs-arrays-2g0e)

### Array.from
This method creates a new array from an array-like (objects with a length property and indexed elements) 
or iterable objects (Map and Set).
```javascript
let arr = Array.from(object, mapFunction, thisValue);
```
#### Exemplos
##### Array from with string
```javascript
let arr = Array.from('github');

// ['g', 'i', 't', 'h', 'u', 'b']
```
##### Array from using map method
```javascript
let arr = Array.from([1, 2, 3], x => x + x);

// [2, 4, 6] 
```
More about: *[Array.from()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/from)*
### Array.fill
Fills all the elements of an array with a static value from a start index to an end index. 
It returns the modified array.
```javascript
const sandwich = ['cheese', 'bread', 'meat'];

sandwich.fill('tomato');
// ['tomato', 'tomato', 'tomato']
```
 You can specify start and end positions.
 ```javascript
 const nums = [3, 4, 5, 7, 8];
 
 nums.fill(0, 1, 3);
 // [3, 0, 0, 7, 8]
 ```

More about: *[Array.fill()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/fill)*
### Array.of
This method creates a new array instance from arguments, regardless of number or type of the arguments.
```javascript
const array = Array.of(1, 5, 'Jhon', {name: 'Doe'});

// [1, 5, "Jhon", {name: "Doe"}] 
```
More about: *[Array.of()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/of)*
### Array.find
Returns the value of the first element in the provided array that satisfies the provided testing function.
```javascript
const years = [2019, 2020, 2021, 2022];
const yearFound = years.find(item => item > 2020);

// 2019  
```
More about: *[Array.find()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find)*
### Array.findIndex
Returns the value of the index of the first element in the provided array that satisfies the provided testing function
```javascript
const sampleArray = [4, -5, 0, -1];
const underZeroIndex = sampleArray.findIndex(x => x < 0);
// 1
```
More about: *[Array.findIndex()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex)*

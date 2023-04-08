## Spread oprator
The spread operator,, is a feature introduced in ECMAScript 6 (ES6) that allows an iterable such as an array or a string to be expanded into individual elements. The spread operator can be used in several ways in JavaScript, such as:
- To spread the contents of an array into a new array:
 ```
const arr1 = [1, 2, 3];
const arr2 = [...arr1, 4, 5, 6];
console.log(arr2); // [1, 2, 3, 4, 5, 6]
```
- To concatenate multiple arrays:
 ```
const arr1 = [1, 2];
const arr2 = [3, 4];
const arr3 = [5, 6];
const arr4 = [...arr1, ...arr2, ...arr3];
console.log(arr4); // [1, 2, 3, 4, 5, 6]
```
- To copy an array:
```
const arr1 = [1, 2, 3];
const arr2 = [...arr1];
console.log(arr2); // [1, 2, 3]
```
- To pass arguments as individual values to a function:
```
  function myFunction(x, y, z) {
  console.log(x + y + z);
}
const arr = [1, 2, 3];
myFunction(...arr); // 6
```
  

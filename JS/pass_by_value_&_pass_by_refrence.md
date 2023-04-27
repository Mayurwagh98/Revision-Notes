### Passed by Value:
1. When a primitive data type (such as numbers, strings, booleans) is passed as an argument to a function, it is passed by value.
2. This means that a copy of the value is created and passed to the function.
3. Any changes made to the value inside the function do not affect the original value outside the function. Here's an example:
```
function updateValue(value) {
  value = 10; // Modifying the copy of the value
  console.log(value); // Output: 10
}

let x = 5;
updateValue(x);
console.log(x); // Output: 5 (original value remains unchanged)
```
4. In the example, the variable x is passed as an argument to the updateValue() function. The function receives a copy of the value stored in x. When the value is modified inside the function, it only affects the copy, and the original value of x remains unchanged.

### Passed by Reference:
1. When an object (including arrays and functions) is passed as an argument to a function, it is passed by reference.
2. This means that a reference to the original object is passed, rather than a copy of the object itself. 
3. Any changes made to the object inside the function will affect the original object outside the function. Here's an example:
```
function updateArray(arr) {
  arr.push(4); // Modifying the original array
  console.log(arr); // Output: [1, 2, 3, 4]
}

let myArray = [1, 2, 3];
updateArray(myArray);
console.log(myArray); // Output: [1, 2, 3, 4] (original array is modified)
```
4. In this example, the updateArray() function receives a reference to the myArray object. The function modifies the original array by adding an element to it. As the object was passed by reference, the changes made inside the function are reflected in the original array outside the function.

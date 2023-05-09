## Callback function

A callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.

```
function greeting(name) {
  alert(`Hello, ${name}`);
}

function processUserInput(callback) {
  const name = prompt("Please enter your name.");
  callback(name);
}

processUserInput(greeting);
```
```
function divide(x,y){
    return x/y
}

function multiply(x,y){
    return x*y
}

function compute(callBack, x, y){
    return callBack(x,y)
}

console.log(compute(divide, 10, 5))    // 2
console.log(compute(multiply, 10, 5))` // 50
```
```
function modifyArray(arr, callback) {
  // do something to arr here
  arr.push(100);
  // then execute the callback function that was passed
  callback();
}

var arr = [1, 2, 3, 4, 5];

modifyArray(arr, function() {
  console.log("array has been modified", arr);
});
```

The most common examples of callback functions in JavaScript are addEventListener, array functions (filter, map, reduce) etc.


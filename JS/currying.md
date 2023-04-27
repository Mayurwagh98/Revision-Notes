1. Currying is a concept in JavaScript and other functional programming languages that allows you to transform a function with multiple arguments into a sequence of functions, each taking a single argument.
2. The curried function returns a new function with each argument partially applied until all arguments are provided, and then it executes and returns the final result.
```
function add (a) {
  return function(b){
    return a + b;
  }
}

add(3)(4) 
```
3. For Example, if we have a function f(a,b), then the function after currying, will be transformed to f(a)(b).
4. By using the currying technique, we do not change the functionality of a function, we just change the way it is invoked.
```
function multiply(a,b){
  return a*b;
}

function currying(fn){
  return function(a){
    return function(b){
      return fn(a,b);
    }
  }
}

var curriedMultiply = currying(multiply);

multiply(4, 3); // Returns 12

curriedMultiply(4)(3); // Also returns 12
```

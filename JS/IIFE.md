1. IIFE stands for Immediately Invoked Function Expression. It is a common pattern used in JavaScript to create a function and execute it immediately after its definition.
```
(function() {
  // Function code goes here
})();
```
2. In the above code, an anonymous function is defined within parentheses and immediately followed by another set of parentheses. This second set of parentheses invokes the function immediately after its definition.
3. IIFEs are often used to create a local scope for variables, allowing you to encapsulate code and avoid polluting the global namespace.
4. Any variables declared inside the IIFE are not accessible from the outside, providing a way to create private variables and functions.
```
(function() {
  var name = "John";

  function sayHello() {
    console.log("Hello, " + name + "!");
  }

  sayHello(); // Output: Hello, John!
})();

console.log(name); // Error: name is not defined
```
5. In the above example, the IIFE creates a local scope with the variable name and the function sayHello(). These are not accessible from outside the IIFE. The IIFE is immediately invoked, resulting in the output "Hello, John!" being logged to the console. When trying to access name outside the IIFE, it throws an error because the variable is not defined in the outer scope.
6. 

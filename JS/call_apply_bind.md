## bind() method
For such cases we can use the ECMAScript 5 bind() method of the Function.prototype property. This means bind() can be used by every single function.
```
var myCarDetails = car.displayDetails.bind(car); 

myCarDetails(); // GA12345 Toyota
```
The bind() method creates a new function where “this” refers to the parameter in the parenthesis in the above case “car”. This way the bind() method enables calling a function with a specified “this” value.

What if we would like to pass a parameter to the displayDetails function? We can use the bind method again. The following argument of the bind() method will provide an argument to the function bind() is called on.

Let me rewrite the car object:
```
var car = { 
    registrationNumber: "GA12345",
    brand: "Toyota",

    displayDetails: function(ownerName){
        console.log(ownerName + ", this is your car: " + this.registrationNumber + " " + this.brand);
    }
}
```
Example of passing arguments with bind():
```
var myCarDetails = car.displayDetails.bind(car, "Vivian"); // Vivian, this is your car: GA12345 Toyota
```

## call() and apply() methods

Similar but slightly different usage provide the call() and apply() methods which also belong to the Function.prototype property.

This time there is a car object without the displayDetails function, which is located in the global context.
```
var car = { 
    registrationNumber: "GA12345",
    brand: "Toyota"
}

function displayDetails(ownerName) {
    console.log(ownerName + ", this is your car: " + this.registrationNumber + " " + this.brand);
}
```
We can use the apply() function:
```
displayDetails.apply(car, ["Vivian"]); // Vivian, this is your car: GA12345 Toyota
```
Or
```
displayDetails.call(car, "Vivian"); // Vivian, this is your car: GA12345 Toyota
```
Note that when using the apply() function the parameter must be placed in an array. Call() accepts both an array of parameters and a parameter itself. Both are great tools for borrowing functions in JavaScript.

---------------------------------

### call: 
1. The call() method allows you to invoke a function with a specific this value and arguments passed individually.

Syntax: function.call(thisArg, arg1, arg2, ...)
```
function greet() {
  console.log(`Hello, ${this.name}`);
}

const person = { name: "John" };

greet.call(person); // output: Hello, John
```
2. Example 2:
```
function sayHello(){
  return "Hello " + this.name;
}
        
var obj = {name: "Sandy"};
        
sayHello.call(obj);
        
// Returns "Hello Sandy"	
```
3. call() method allows an object to use the method (function) of another object.
4. Example 3:
```
var person = {
  age: 23,
  getAge: function(){
    return this.age;
  }
}        
var person2 = {age:  54};
person.getAge.call(person2);      
// Returns 54  
```
5. call() accepts arguments:
```
function saySomething(message){
  return this.name + " is " + message;
}     
var person4 = {name:  "John"};     
saySomething.call(person4, "awesome");
// Returns "John is awesome" 
```
apply: The apply() method is similar to call(), but it accepts arguments as an array.

Syntax: function.apply(thisArg, [argsArray])
```
function greet(greeting) {
  console.log(`${greeting}, ${this.name}`);
}

const person = { name: "John" };

greet.apply(person, ["Hello"]); // output: Hello, John
```
bind: The bind() method returns a new function with a specific this value and any arguments passed to it.

Syntax: function.bind(thisArg[, arg1[, arg2[, ...]]])
```
function greet(greeting) {
  console.log(`${greeting}, ${this.name}`);
}

const person = { name: "John" };

const greetPerson = greet.bind(person);

greetPerson("Hello"); // output: Hello, John
```
```
var bikeDetails = {
    displayDetails: function(registrationNumber,brandName){
    return this.name+ " , "+ "bike details: "+ registrationNumber + " , " + brandName;
  }
}
   
var person1 = {name:  "Vivek"};
     
var detailsOfPerson1 = bikeDetails.displayDetails.bind(person1, "TS0122", "Bullet");
      
// Binds the displayDetails function to the person1 object
        
      
detailsOfPerson1();
//Returns Vivek, bike details: TS0122, Bullet
```

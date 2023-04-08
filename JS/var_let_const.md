  
## var, let and const

| var  | let | const |
| ------------- | ------------- | ------------- | 
| The scope of a var variable is functional scope. | The scope of a let variable is block scope. | The scope of a const variable is block scope. |
|It can be updated and re-declared into the scope. |It can be updated but cannot be re-declared into the scope. | It cannot be updated or re-declared into the scope.|
|It can be declared without initialization. |It can be declared without initialization. |It cannot be declared without initialization.|
|It can be accessed without initialization as its default value is “undefined”. |It cannot be accessed without initialization otherwise it will give ‘referenceError’. |It cannot be accessed without initialization, as it cannot be declared without initialization.|
|hoisting done, with initializing as ‘default’ value |Hoisting is done , but not initialized (this is the reason for the error when we access the let variable before declaration/initialization |Hoisting is done, but not initialized (this is the reason for error when we access the const variable before declaration/initialization |

## Scopes
https://developer.mozilla.org/en-US/docs/Glossary/Scope
- Global Scope

In a programming environment, the global scope is the scope that contains, and is visible in, all other scopes.

In client-side JavaScript, the global scope is generally the web page inside which all the code is being executed.

- Local scope 

Local scope is a characteristic of variables that makes them local (i.e., the variable name is only bound to its value within a scope which is not the global scope).

- block scope

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/block

The scope created with a pair of curly braces (a block).

Block scoping rules with let, const, class, or function declaration in strict mode
By contrast, identifiers declared with let, const, and class do have block scope:
```
let x = 1;
{
  let x = 2;
}
console.log(x); // 1
```
The x = 2 is limited in scope to the block in which it was defined.

The same is true of const:
```
const c = 1;
{
  const c = 2;
}
console.log(c); // 1; does not throw SyntaxError
```
Note that the block-scoped const c = 2 does not throw a SyntaxError: Identifier 'c' has already been declared because it can be declared uniquely within the block.

## Common.js
1. CommonJS (or CJS) is a module format used in Node.js and other server-side JavaScript environments. It was designed to provide a way to organize and reuse code in a modular way.
2. In CommonJS, modules are defined using the require() function to import dependencies and the module.exports object to export the module's public API.
3. CommonJS modules are loaded synchronously
4. all dependencies must be loaded before the module can be executed, which can result in slower startup times for large applications
5. For example, to define a module that exports a function:
```
// my-module.js
function myFunction() {
  // ...
}

module.exports = myFunction;
```
6. And to import that module:
```
// app.js
const myFunction = require('./my-module');

myFunction();
```
## ES modules
1. ES modules (or ES6 modules) are a newer module format introduced in ECMAScript 6 (ES6). 
2. They are designed to be used in both server-side and client-side environments, and provide a more modern and flexible way to organize and reuse code.
3. ES modules are loaded asynchronously
4. In ES modules, modules are defined using the import and export keywords. For example, to define a module that exports a function:
```
// my-module.js
export function myFunction() {
  // ...
}
```
5. And to import that module:
```
// app.js
import { myFunction } from './my-module.js';

myFunction();
```

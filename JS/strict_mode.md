## Strict Mode

Strict mode makes several changes to normal JavaScript semantics:

1. Eliminates some JavaScript silent errors by changing them to throw errors.
2. Fixes mistakes that make it difficult for JavaScript engines to perform optimizations: strict mode code can sometimes be made to run faster than identical code that's not strict mode.
3. Prohibits some syntax likely to be defined in future versions of ECMAScript.

- Invoking strict mode
Strict mode applies to entire scripts or to individual functions. It doesn't apply to block statements

- Strict mode for scripts
```
// Whole-script strict mode syntax
"use strict";
const v = "Hi! I'm a strict mode script!";
```
- Strict mode for functions
```
function myStrictFunction() {
  // Function-level strict mode syntax
  "use strict";
  function nested() {
    return "And so am I!";
  }
  return `Hi! I'm a strict mode function! ${nested()}`;
}
function myNotStrictFunction() {
  return "I'm not strict.";
}
```
- Changes in strict mode
1. changes converting mistakes into errors (as syntax errors or at runtime)
2. changes simplifying how variable references are resolved
3. changes simplifying eval and arguments
4. changes making it easier to write "secure" JavaScript
5. changes anticipating future ECMAScript evolution.

- Converting mistakes into errors
1. Strict mode changes some previously-accepted mistakes into errors. JavaScript was designed to be easy for novice developers, and sometimes it gives operations which should be errors non-error semantics.
2. Sometimes this fixes the immediate problem, but sometimes this creates worse problems in the future. Strict mode treats these mistakes as errors so that they're discovered and promptly fixed.

- Assigning to undeclared variables
```
"use strict";
let mistypeVariable;

// Assuming no global variable mistypeVarible exists
// this line throws a ReferenceError due to the
// misspelling of "mistypeVariable" (lack of an "a")
mistypeVarible = 17;
```

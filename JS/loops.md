## for loop
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for

```
for (initialization; condition; afterthought)
  statement
```
```
let str = '';

for (let i = 0; i < 9; i++) {
  str = str + i;
}

console.log(str);
// Expected output: "012345678"
```
## while loop
The while statement creates a loop that executes a specified statement as long as the test condition evaluates to true. The condition is evaluated before executing the statement.

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/while

```
while (condition)
  statement
```
```
let n = 0;

while (n < 3) {
  n++;
}

console.log(n);
// Expected output: 3
```
## do...while
The do...while statement creates a loop that executes a specified statement until the test condition evaluates to false. The condition is evaluated after executing the statement, resulting in the specified statement executing at least once.

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/do...while

`syntax`

 ```
do
  statement
while (condition);
```
```
let result = '';
let i = 0;

do {
  i = i + 1;
  result = result + i;
} while (i < 5);

console.log(result);
// Expected output: "12345"
```
```
let result = "";
let i = 0;
do {
  i += 1;
  result += `${i} `;
} while (i > 0 && i < 5);
// Despite i === 0 this will still loop as it starts off without the test

console.log(result);
```

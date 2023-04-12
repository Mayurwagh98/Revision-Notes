## readFile
1. readFile is an asynchronous method that takes in a file path and a callback function.
2. It reads the file and then executes the callback function with two parameters: an error (if any) and the data from the file.
3. The advantage of using readFile is that it allows your code to continue running while the file is being read, which is particularly useful in applications where you need to perform multiple tasks concurrently.
4. However, you need to handle the asynchronous nature of the callback function and make sure that any code that relies on the data from the file is placed inside the callback function.

```
const fs = require('fs');

// Using readFile method
fs.readFile('/path/to/file', (err, data) => {
  if (err) throw err;
  console.log(data);
});
```

## readFileSync
1. synchronous method that takes in a file path and returns the data from the file.
2. It blocks the execution of the code until the file is read completely.
3. While it simplifies your code by allowing you to read the file synchronously without callbacks, it can lead to blocking issues if you use it for large files or when you need to perform multiple I/O operations simultaneously.

```
const fs = require('fs');

// Using readFileSync method
const data = fs.readFileSync('/path/to/file');
console.log(data);
```

## Blocking
1. blocking refers to an operation that prevents the execution of further code until it has completed. 
2. his means that if a blocking operation is being performed, Node.js will not execute any other code until that operation has finished. 
3. This can cause performance issues, especially in applications that handle a lot of simultaneous connections or I/O operations.

## Non-Blocking
1. refers to an operation that allows other code to be executed while it is being processed. 
2. This means that Node.js can continue to handle other requests while an I/O operation is being performed.
3. Node.js is designed to be non-blocking, which means that it can handle multiple connections and I/O operations simultaneously.
4. This is achieved through the use of asynchronous programming, promises, callbacks, which allows code to be executed in a non-blocking manner.

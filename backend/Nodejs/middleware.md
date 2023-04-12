1. In Node.js, middleware is a software layer that sits between the application logic and the underlying system infrastructure, providing additional functionality to the application. 
2. Middleware functions are essentially functions that have access to the request and response objects in an application's HTTP request-response cycle.
3. They can perform tasks such as modifying the request or response objects, invoking additional logic, or terminating the request-response cycle.
4. Middleware functions can be used in different parts of a Node.js application, including:
  - Application level middleware: These middleware functions are loaded using the app.use() method and are executed for every request made to the application.
  - Router level middleware: These middleware functions are attached to specific routes using the router.use() method and are executed for every request that matches the specified route.
  - Error handling middleware: These middleware functions are used to handle errors that occur in the application.

```
const express = require('express');
const app = express();

// Application level middleware
app.use((req, res, next) => {
  console.log('Middleware function called');
  next();
});

// Route handler
app.get('/hello', (req, res) => {
  res.send('Hello, world!');
});

app.listen(3000, () => {
  console.log('Server started on port 3000');
});
```
- In this example, we define an application level middleware function that logs a message to the console whenever a request is made to the application. 
- We then define a route handler for the /hello endpoint that sends a response back to the client. 
- When a request is made to the /hello endpoint, the middleware function is executed first, logging a message to the console, before the route handler sends the response back to the client. 

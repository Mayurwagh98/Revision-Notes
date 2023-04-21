1. In Express, you can manage cookies by using the cookie-parser middleware. The cookie-parser middleware is a popular module that parses HTTP cookies and populates the req.cookies object with the cookie name-value pairs.
2. Here's an example of how to set up cookie-parser middleware in your Express app:
```
const express = require('express');
const cookieParser = require('cookie-parser');

const app = express();

// Set up cookie-parser middleware
app.use(cookieParser());

// Set up a route to set a cookie
app.get('/set-cookie', (req, res) => {
  res.cookie('myCookie', 'Hello, world!', { maxAge: 900000, httpOnly: true });
  res.send('Cookie set!');
});

// Set up a route to read a cookie
app.get('/read-cookie', (req, res) => {
  const myCookie = req.cookies.myCookie;
  res.send(`Cookie value is: ${myCookie}`);
});

// Start the server
app.listen(3000, () => {
  console.log('Server started on port 3000');
});
```
3. In this example, the cookie-parser middleware is set up to parse HTTP cookies. Once the middleware is set up, you can use the res.cookie method to set a cookie. The res.cookie method takes three arguments: the cookie name, the cookie value, and an optional options object. In this example, the cookie is set with a maxAge of 900000 milliseconds (15 minutes) and an httpOnly flag, which makes the cookie inaccessible to JavaScript code.
4. Once the cookie is set, you can use the req.cookies object to read the cookie value. In the example above, two routes are set up: one to set a cookie (/set-cookie) and one to read a cookie (/read-cookie). The cookie value is stored in the req.cookies object, which is automatically populated by the cookie-parser middleware.
5. Note that cookies are automatically sent in the HTTP response headers and included in subsequent requests. By default, cookies are sent with every request to the same domain and path that set the cookie. You can configure the cookie settings by passing options to the res.cookie method, such as the maxAge, secure, and domain options.
 




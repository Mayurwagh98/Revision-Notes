https://nodejs.org/en/docs/guides/anatomy-of-an-http-transaction
```
const http = require('http');

const options = {
  hostname: 'www.example.com',
  port: 80,
  path: '/path/to/resource',
  method: 'GET'
};

const req = http.request(options, (res) => {
  console.log(`statusCode: ${res.statusCode}`);

  res.on('data', (d) => {
    process.stdout.write(d);
  });
});

req.on('error', (error) => {
  console.error(error);
});

req.end();
```
1. we create an options object with the hostname, port, path, and method properties, which define the details of the request we want to send. 
2. We then create a request object using the http.request method, passing in the options object and a callback function that handles the server's response.
3. The req object emits an 'error' event if there is an error in sending the request. Finally, we call req.end() to actually send the request to the server.
4. The callback function logs the status code of the response to the console and listens for data events on the response object, which represent chunks of data received from the server.
5. In this example, we write the data to the standard output using process.stdout.write. You can replace this with any function that processes the data as needed.
6. 

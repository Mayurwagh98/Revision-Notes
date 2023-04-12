1. we first import the http module and the fs module for reading the HTML file.
2. We then create a server using the http.createServer method, which takes a callback function that will be called whenever a client makes a request to the server. 
3. The callback function receives two arguments: a request object and a response object.
4. Inside the callback function, we check if the requested URL is '/'.
5. If it is, we read the index.html file using the fs.readFile method and send its contents as the response body with a 200 status code and text/html content type.
6. If there is an error in reading the file, we send a 500 status code with a plain text error message.
7. If the requested URL is not '/', we send a 404 status code with a plain text error message.
8. Finally, we listen to incoming connections on port 3000 using the server.listen method, which takes a port number and an optional callback function to be called when the server starts listening.
```
const http = require('http');
const fs = require('fs');

const server = http.createServer((req, res) => {
  if (req.url === '/') {
    fs.readFile('index.html', (err, data) => {
      if (err) {
        res.writeHead(500, {'Content-Type': 'text/plain'});
        res.end('Internal server error');
      } else {
        res.writeHead(200, {'Content-Type': 'text/html'});
        res.end(data);
      }
    });
  } else {
    res.writeHead(404, {'Content-Type': 'text/plain'});
    res.end('Page not found');
  }
});

server.listen(3000, () => {
  console.log('Server is listening on port 3000');
});
```

# What is node.js, what are servers, what are frameworks?

## What is 'Express'?

first lets make a server with strictly node,js. then we will build it again with express to compare. 


```
// example of node server creation..
const http = require('http');
const PORT = 3001;

http.createServer(function (req, res) {
  console.log(req) // <- req and res are large objects provided by node via the createServer method>
})
.listen(8080);
```

`req` = stuff client inputs to server.

`res` = stuff that will be sent to client



## What is a `route` ?
example: const route = `${req.method} ${req.url}`;

<br>

# What is routing?

Routing refers to how an application’s endpoints (URIs) respond to client requests. Each endpoint (or route) can have one or more handler functions, which are executed when the route is matched. See http://expressjs.com/en/guide/routing.html.

<br>

### We will be focusing more on express rather than straight node for making a server. see lecture notes.



# Middleware

## Definition

Middleware is a software that provides services to software applications beyond those available from the operating system.

## Use in Javascript

Example: server32.js

```javascript
const express = require('express'); // import express
const app = express();            // create an express app

app.use(mw1); // use middleware, this will expose mw1 to all routes
// a route is a combination of an HTTP method and a path (endpoint)

function mw1(req, res, next) {
  console.log('mw1');           // print to console
  next();                    // call next middleware, 
//   if there this line is not called, the request will be stuck here
}

function myfunction1(req, res, next) {
  res.send('<h1>myfunction1</h1>'); // send response
}

app.get('/', mw1, myfunction1); // use middleware

app.listen(3000);

console.log('Server running at http://localhost:3000/');
```

We use `app.use()` to use middleware. We can use multiple middleware in a route. The order of middleware is important. The request will be stuck if we don't call `next()`.

Whenever a function is passed as an argument to `app.use()`, it is considered middleware. And the function inside will be called for every request. 

With `app.use()`, we can use middleware for all routes. If we want to use middleware for a specific route, we can use `app.get()`, `app.post()`, etc.

The order of execution of middleware depends on the order of `app.use()` and `app.get()`, `app.post()`, etc.
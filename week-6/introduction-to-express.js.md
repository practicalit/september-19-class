**Introduction to Express**

_Express application setup and configuration:_

Express is a minimalist web application framework for Node.js. It provides a robust set of features for web and mobile applications. To setup an Express application, you need to initialize a new instance of Express and define routes to handle requests.

_Example 3:_ Basic Express application

```
const express = require('express');
const app = express();
const port = 3000;

app.get('/', (req, res) => res.send('Hello World!'))

app.listen(port, () => console.log(`App listening at http://localhost:${port}`))

```

_Routing, middleware, and handling HTTP requests:_

Express.js allows you to handle different HTTP requests at different routes. Middleware functions are functions that have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle.

_Example 4:_ Express application with routing and middleware

```
const express = require('express');
const app = express();
const port = 3000;

// Middleware
app.use((req, res, next) => {
  console.log('Time:', Date.now());
  next();
});

// Routing
app.get('/', (req, res) => res.send('Home Page'));
app.get('/about', (req, res) => res.send('About Page'));

app.listen(port, () => console.log(`App listening at http://localhost:${port}`))

```

_Exercise 3:_ Create an Express application with routes for "/home", "/about", and "/contact". Each route should return a simple HTML page.

_Exercise 4:_ Add a middleware function to the above application that logs the current date and the request method (GET, POST, etc.) for each request.

**Introduction to Node.js**

_Node.js architecture and event loop:_

Node.js is a runtime environment for executing JavaScript code outside of a browser. The backbone of Node.js is its event-driven, non-blocking I/O model, which makes it lightweight and efficient. The event-driven architecture can handle multiple client requests concurrently through the event loop mechanism. The event loop handles all asynchronous callbacks in the application.

_Example 1:_ Simple Node.js server

```
const http = require('http');

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello World\n');
});

server.listen(3000, '127.0.0.1', () => {
  console.log('Server running at http://127.0.0.1:3000/');
});

```

_Asynchronous programming with callbacks, promises, and async/await:_

Callbacks are the basic mechanism for managing async operations in JavaScript. However, they can lead to unmanageable "callback hell" if not handled properly. Promises are used to avoid callback hell and write clean code. Async/await further improves code readability by making it look more synchronous while keeping it asynchronous.

_Example 2:_ Reading a file asynchronously using callbacks, promises, and async/await

```
const fs = require('fs');

// Callbacks
fs.readFile('/etc/passwd', (err, data) => {
  if (err) throw err;
  console.log(data);
});

// Promises
fs.promises.readFile('/etc/passwd')
  .then(data => console.log(data))
  .catch(err => console.error(err));

// Async/await
async function readPasswd() {
  try {
    const data = await fs.promises.readFile('/etc/passwd');
    console.log(data);
  } catch (err) {
    console.error(err);
  }
}

readPasswd();

```

_Exercise 1:_ Create a Node.js application that reads a file and writes its content to another file using callbacks.

_Exercise 2:_ Rewrite the above application using promises and then async/await.

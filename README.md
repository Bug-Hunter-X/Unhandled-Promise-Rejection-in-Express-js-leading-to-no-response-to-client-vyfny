# Unhandled Promise Rejection in Express.js leading to no response to client

This repository demonstrates a common error in Node.js Express.js applications where an unhandled promise rejection during asynchronous operations results in the server not responding to client requests.

## The Bug
The `bug.js` file contains an Express.js server with an asynchronous operation. If the asynchronous operation fails, the error is caught, but the client receives no response.

## The Solution
The `bugSolution.js` file provides a solution to this problem by using a `try...catch` block to handle errors during the asynchronous operation and send an appropriate response to the client.

## How to reproduce the bug
1. Clone the repository.
2. Run `node bug.js`.
3. Make multiple requests to `http://localhost:3000/`. You will notice that sometimes the request times out, while other times it returns a 'Hello, world!' response.

## How to fix the bug
1. Replace `bug.js` with `bugSolution.js`.
2. Run `node bugSolution.js`.
3. Make multiple requests to `http://localhost:3000/`. You'll see a more consistent response, with error messages when necessary.
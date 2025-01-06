# Node.js Server Unresponsiveness Due to Long-Running Tasks

This repository demonstrates a common issue in Node.js servers: unresponsiveness caused by long-running operations that block the event loop.  The `server.js` file showcases the problem, while `serverSolution.js` provides a solution using asynchronous techniques.

## Problem

The original `server.js` creates an HTTP server that simulates a slow operation using `setTimeout`.  During the 5-second delay, the server becomes unresponsive to new requests. This is because Node.js is single-threaded, and the `setTimeout` blocks the event loop.

## Solution

The `serverSolution.js` demonstrates a solution by using asynchronous operations with promises.  This prevents blocking the event loop, allowing the server to remain responsive to requests even while performing long-running tasks.

## How to Run

1. Clone the repository.
2. Navigate to the repository's directory in your terminal.
3. Run `node server.js` to see the unresponsive behavior.
4. Run `node serverSolution.js` to see the solution in action.
# Unhandled Error in Express.js Async Request Handler

This repository demonstrates a common error in Express.js applications: unhandled errors within asynchronous request handlers.  When an asynchronous operation throws an error, and the error isn't caught and handled appropriately, the server might crash without providing clear error messages. This example shows the problematic code and a solution to gracefully handle such errors.

## Problem
The `bug.js` file contains an Express.js server with an asynchronous request handler. The `someAsyncOperation()` function simulates an asynchronous operation that throws an error.  Crucially, the `catch` block within the `.then().catch()` chain is empty, meaning the error isn't handled. This results in the server silently failing.

## Solution
The `bugSolution.js` file provides a corrected version.  It demonstrates the proper way to handle errors within asynchronous request handlers.  By catching the error and sending an appropriate response (e.g., a 500 Internal Server Error), the server remains operational, and users receive informative error messages.

# Node.js Server Hangs on Long Requests

This repository demonstrates a common issue in Node.js applications where long-running operations in request handlers can block the event loop, causing the server to become unresponsive.  The example simulates a 5-second delay, but this could be due to any lengthy operation like database queries or file processing.

## Problem

The `server.js` file contains a simple HTTP server.  However, the request handler includes a `while` loop that simulates a long-running task. During this time, the server cannot process any other requests, leading to a hang.

## Solution

The `serverSolution.js` file demonstrates a solution using asynchronous operations with `setTimeout`. This prevents blocking the event loop and keeps the server responsive.
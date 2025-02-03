# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js where a long-running operation in a request handler blocks the event loop, making the server unresponsive to other requests.  The `bug.js` file contains the problematic code.  The `bugSolution.js` file shows how to address this using asynchronous operations.

## Problem

Node.js is single-threaded, so long-running synchronous operations can block the event loop, preventing it from processing other requests.  This causes the server to become unresponsive.

## Solution

The solution involves using asynchronous operations (e.g., promises, async/await) to avoid blocking the event loop.  Asynchronous code allows the event loop to continue processing other events while the long-running operation is performed in the background.
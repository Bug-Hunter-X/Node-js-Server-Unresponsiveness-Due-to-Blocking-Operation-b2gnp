# Node.js Server Unresponsiveness Due to Blocking Operation

This repository demonstrates a common Node.js issue: server unresponsiveness caused by a long-running synchronous operation that blocks the event loop.  The `server.js` file contains the problematic code, while `serverSolution.js` provides a corrected version using asynchronous operations.

## Problem

The original code includes a `while` loop that simulates a lengthy process. This blocks the event loop, preventing Node.js from handling other requests or events.  This leads to the server becoming unresponsive and potentially causing other issues.

## Solution

The solution involves using asynchronous operations to avoid blocking the event loop. This allows Node.js to continue handling other requests concurrently.
# Node.js Server Hang Issue

This repository demonstrates an intermittent server hang issue in a Node.js application. The server appears to hang after a certain number of requests, especially under load.  The issue is subtle and difficult to reproduce consistently, highlighting a potential race condition or resource exhaustion problem.

## Bug Report

The `bug.js` file contains a simple HTTP server that simulates a delay in responding to requests.  Under heavy load, the server sometimes fails to respond to subsequent requests, appearing to hang. This is a common problem in event-driven architectures where asynchronous operations aren't properly managed.

## Solution

The `bugSolution.js` file provides a solution to this issue by leveraging proper error handling and resource management. The improved server uses the 'cluster' module to handle multiple requests efficiently.
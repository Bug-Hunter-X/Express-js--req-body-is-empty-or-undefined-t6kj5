# Express.js: req.body is empty or undefined

This repository demonstrates a common issue in Express.js applications where the request body (req.body) is empty or undefined, usually when the Content-Type header is missing or incorrect in POST requests.

## Bug

The `bug.js` file shows an Express.js app that attempts to access the request body.  If a POST request is made without the correct `Content-Type: application/json` header, `req.body` will be empty.

## Solution

The `bugSolution.js` file demonstrates the solution. By explicitly adding the `express.json()` middleware *before* the route handler, the application correctly parses JSON data from the request body, regardless of any header issues.
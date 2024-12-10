# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  the lack of proper error handling when dealing with user inputs.

The `bug.js` file shows a route that attempts to find a user by ID. However, it fails to handle cases where the ID is not a valid number, leading to potential crashes or unexpected behavior.

The `bugSolution.js` file provides a corrected version with robust error handling, showcasing best practices for handling invalid inputs in Express.js applications.

## How to reproduce the bug
1. Clone this repository
2. Run `npm install` to install the required dependencies
3. Run `node bug.js`
4. Make a request to `/users/abc` (or any non-numeric ID).  The server will likely crash or return an unexpected error.

## How to fix the bug
Refer to the `bugSolution.js` file for an example of implementing proper error handling using `isNaN` and sending appropriate HTTP status codes.
# Express.js Route Handler: Missing Error Handling for Invalid User IDs

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  The provided code attempts to access a user based on their ID, but fails to handle cases where the ID is not a valid integer, resulting in a server crash.

The `bug.js` file contains the erroneous code.  The `bugSolution.js` file provides a corrected version with proper error handling.

## How to reproduce

1. Clone this repository.
2. Run `npm install express`
3. Run `node bug.js`
4. Access the route `/users/abc` (or any non-numeric ID) in a browser or using a tool like curl.  You should see a server crash.

## Solution

The solution involves adding error handling to check if the `userId` is a valid number before attempting to access the user data. The improved code is found in `bugSolution.js`.
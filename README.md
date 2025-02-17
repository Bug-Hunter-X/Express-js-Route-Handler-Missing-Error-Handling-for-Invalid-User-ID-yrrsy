# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, the code attempts to parse a user ID from the route parameters as an integer without validating the input.

## Bug

The `bug.js` file contains the flawed code.  The route handler for `/users/:id` attempts to find a user based on the `id` parameter.  It parses the `id` as an integer using `parseInt()`, but it does not handle the case where the `id` parameter is not a valid integer. This could lead to errors if a user enters non-numeric data.

## Solution

The `bugSolution.js` file provides a corrected version of the code.  The solution includes explicit checks to ensure the `userId` is a number before attempting to parse it and uses error handling to return appropriate responses for invalid inputs.
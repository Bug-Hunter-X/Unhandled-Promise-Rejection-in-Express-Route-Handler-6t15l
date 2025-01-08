# Unhandled Promise Rejection in Express Route Handler

This repository demonstrates a common error in Express.js applications where an unhandled promise rejection in a route handler prevents the server from sending a response to the client.  The error is logged to the console, but the client experiences a timeout.

## Bug

The `bug.js` file contains an Express.js app with a route handler that performs an asynchronous operation. If the operation throws an error, the error is caught, logged, but no response is sent back to the client.

## Solution

The `bugSolution.js` file shows the corrected version.  Always send a response, even in case of an error. This ensures that the client receives feedback, preventing timeouts and improving the user experience.  Proper error handling is crucial for robust applications.
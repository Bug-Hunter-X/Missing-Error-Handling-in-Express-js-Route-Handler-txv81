# Missing Error Handling in Express.js Route Handler

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input. The `bug.js` file shows the problematic code, while `bugSolution.js` provides a corrected version.

**Problem:** The original code attempts to parse the user ID from the request parameters as an integer without checking for errors. If the ID is not a valid integer, the `parseInt` function will return `NaN`, causing the `find` method to fail silently or throw an exception.

**Solution:** The solution incorporates error handling to gracefully handle invalid user IDs.  It checks if the parsed ID is a number and returns a 404 error if the user is not found.
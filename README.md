# Improper Exception Handling in Asynchronous Dart Code

This repository demonstrates a common error in Dart:  improper exception handling in asynchronous operations using `Future` and `async/await`.  The original code lacks a crucial `rethrow` statement, hindering the ability of calling functions to handle the exception effectively. The solution provides the correction.

## Bug
The `fetchData` function in `bug.dart` demonstrates the error.  The `catch` block prints the error but doesn't propagate it upwards using `rethrow`, making it difficult for calling functions to react appropriately to errors.

## Solution
The corrected `fetchData` function in `bugSolution.dart` includes a `rethrow` statement, ensuring that exceptions are properly propagated up the call stack, allowing for more robust error handling.
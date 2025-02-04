# Unhandled jsonDecode Exception in Dart

This repository demonstrates a common error in Dart asynchronous programming: neglecting to handle potential exceptions thrown by `jsonDecode` when parsing JSON data fetched from an API.  The `bug.dart` file shows the flawed code, while `bugSolution.dart` provides a corrected version.

## Problem

The original code lacks proper exception handling for the `jsonDecode` function. If the API response isn't valid JSON, a `FormatException` is thrown, leading to a crash or unexpected behavior. 

## Solution

The solution adds a `try-catch` block around `jsonDecode` to specifically handle `FormatException`.  This prevents the application from crashing and allows for more graceful error handling, such as displaying a user-friendly message or retrying the request.
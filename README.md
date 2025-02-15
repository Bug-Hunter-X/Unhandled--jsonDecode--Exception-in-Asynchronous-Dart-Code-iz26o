# Unhandled jsonDecode Exception in Asynchronous Dart

This repository demonstrates a common error in Dart asynchronous programming:  failure to handle exceptions thrown by `jsonDecode`. The `bug.dart` file shows the problematic code, and `bugSolution.dart` provides a corrected version.

The bug arises from not explicitly catching exceptions that `jsonDecode` may throw if the response from a network request isn't valid JSON. This can lead to unexpected app crashes.

The solution involves adding a `try-catch` block specifically around the `jsonDecode` call to gracefully handle potential `FormatException` exceptions.
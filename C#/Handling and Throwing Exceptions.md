The following list identifies practices to avoid when throwing exceptions:

- Don't use exceptions to change the flow of a program as part of ordinary execution. Use exceptions to report and handle error conditions.
- Exceptions shouldn't be returned as a return value or parameter instead of being thrown.
- Don't throw `System.Exception`, `System.SystemException`, `System.NullReferenceException`, or `System.IndexOutOfRangeException` intentionally from your own source code.
- Don't create exceptions that can be thrown in debug mode but not release mode. To identify runtime errors during the development phase, use `Debug.Assert` instead.

> [!info] The `Debug.Assert` method is a tool for catching logic errors during development. By default, the `Debug.Assert` method works only in debug builds. You can use `Debug.Assert` in debug sessions to check for a condition that should never occur. The method takes two parameters: a Boolean condition to check, and an optional string message to display if the condition is `false`. `Debug.Assert` should not be used in place of throwing an exception, which is a way to handle exceptional situations during normal execution of your code. You should use `Debug.Assert` to catch errors that should never occur, and use exceptions to handle errors that could occur during normal execution of your program.

`throw ex` loses the original stack trace, while `throw` preserves it.
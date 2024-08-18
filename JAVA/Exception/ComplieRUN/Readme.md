# Exception Handling in Java

## Overview

In Java, exceptions are events that disrupt the normal flow of a program. They can occur during the runtime of a program and are categorized into two types:

1. **Compile-time Exceptions**
2. **Runtime Exceptions**

## Compile-time Exceptions

- Compile-time exceptions are those that are checked at compile time.
- The compiler ensures that these exceptions are handled using a `try-catch` block or declared in the method signature using the `throws` keyword.
- If compile-time exceptions are not handled, the program will not compile.

## Runtime Exceptions

- Runtime exceptions are those that are ignored by the compiler.
- The compiler does not check for runtime exceptions, meaning they are not required to be caught or declared in the method signature.
- These exceptions occur at runtime, and if not properly handled, they can cause the program to terminate abruptly.

## Summary

- **Compile-time Exceptions:** Checked by the compiler at compile time and must be handled.
- **Runtime Exceptions:** Ignored by the compiler at compile time, occur at runtime, and should be handled to prevent program crashes.



# Exception Handling in Java

Whenever an exception occurs, the method in which the exception occurs will create an object. This object stores three things:
1. **Exception name**
2. **Description**
3. **Stack trace**

The object is then passed to the JVM. If the JVM can't handle the exception, it sends the object to the exception handler, which prints the exception details. To allow the JVM to handle these objects manually, we use a `try` and `catch` block.

## Exception Handling Keywords

We can handle exceptions in Java using the following five keywords:
1. `try`
2. `catch`
3. `finally`
4. `throw`
5. `throws`

## Syntax

```java
try {
    // risky code
} catch (ExceptionClassName refVarName) {
    // handling code
}

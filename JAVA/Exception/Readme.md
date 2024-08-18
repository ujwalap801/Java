# Exception Handling in Java

## What is an Exception?

An **exception** is an unwanted or unexpected event that occurs during the execution of a program, i.e., at runtime, which disrupts the normal flow of the program.

## Exception Handling

**Exception handling** is the process of responding to unwanted or unexpected events when a computer program runs. It provides an alternative way to respond to exceptions, ensuring that the program or system does not crash. Without exception handling, exceptions would disrupt the normal operation of a program.

## Key Concepts

- **Object Class:** The `Object` class is the parent class of all classes in Java.
- **Throwable Class:** `Throwable` is the parent class of the `Exception` class. This means that for both exceptions and errors, the parent class is `Throwable`.
  - **Exceptions:** These are events that occur due to issues in our programs.
  - **Errors:** These occur due to the lack of system resources, not because of our programs. Programmers cannot handle or prevent errors.


# Exceptions and Errors in Java

## Exceptions
Exceptions are recoverable and can be handled using try-catch blocks or by throwing them further up the call stack. They are broadly categorized into two types:

1. **Compile-Time Exceptions (Checked Exceptions):**
   - These are exceptions that are checked by the compiler at the time of compilation.
   - Example: `IOException`, `SQLException`.

2. **Runtime Exceptions (Unchecked Exceptions):**
   - These are exceptions that occur during the runtime of the program.
   - Example: `NullPointerException`, `ArrayIndexOutOfBoundsException`.

## Errors
Errors are not recoverable and indicate serious problems that a reasonable application should not try to catch. They usually represent issues related to the runtime environment, like memory leaks or stack overflow. There is one main type:

1. **Runtime Error (Unchecked Exception):**
   - These errors are typically unrecoverable and are not meant to be handled by the program.
   - Example: `OutOfMemoryError`, `StackOverflowError`.

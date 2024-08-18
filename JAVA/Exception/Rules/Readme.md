## Exception Handling in Java

In Java, the `try-catch-finally` block is a powerful construct used for exception handling. Below are some key points about its usage:

### Basic Structure
```java
try {
    // risk code
} catch (Exception e) {
    // handling code
} finally {
    // cleanup code
}


try block: Contains the code that might throw an exception.
catch block: Handles the exception thrown by the try block.
finally block: Executes cleanup code, regardless of whether an exception was thrown or not.

Important Notes:
We can use multiple catch blocks with one try block to handle different types of exceptions, but only one finally block can be used with a single try block.


The statements present in the finally block will execute even if the try block contains control transfer statements (jump statements) like return, break, or continue.
Conditions That May Prevent the Execution of the finally Block:
The use of the System.exit() method.
Causing a fatal error that leads to process termination.
An exception occurring within the finally block itself.
The death of the thread executing the finally block.


Example with finally Block Only
try {
    // code that may throw an exception
} finally {
    // cleanup code
}

Note: A finally block must be associated with a try block. It cannot be used alone without a try block.
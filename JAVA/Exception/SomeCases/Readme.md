## Exception Handling in Java

### 1. Usage of `try`, `catch`, and `finally` blocks

In Java, the `try`, `catch`, and `finally` blocks must be used in a specific manner to avoid compilation errors.

#### Incorrect Example 1

```java
try {
    // Code that might throw an exception
} 
catch(Exception e) {
    // Handling the exception
} 
catch(Exception e) {
    // Handling the exception
}


Error: We cannot use the parent class Exception in multiple catch blocks. This will result in a compilation error because the second catch block is unreachable.


Ex:

try {
    // Code that might throw an exception
} 
catch(ArithmeticException e) {
    // Handling ArithmeticException
} 
catch(Exception e) {
    // Handling any other exceptions
}


Explanation: This is correct because the child class ArithmeticException is used in the first catch block, and the parent class Exception is used in the second catch block. This ensures that more specific exceptions are caught first.



try {
    // Code that might throw an exception
} 
finally {
    // Code that will always execute
} 
catch(Exception e) {
    // Handling the exception
}

Error: The finally block should come after the catch block if one is present. Placing the finally block before the catch block will result in a compilation error.

Key Takeaways
You cannot have multiple catch blocks with the same exception type or with a parent exception type before a child exception type.
The finally block must always come last after all catch blocks if they are present
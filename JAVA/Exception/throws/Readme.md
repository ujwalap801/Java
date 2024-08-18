## `throws` Keyword in Java

The `throws` keyword is used to declare an exception in a method. It provides information to the caller method that an exception may occur, suggesting that the caller method should implement exception handling code to maintain the normal flow of the program.

### Key Points:
- **Purpose**: The `throws` keyword indicates that a method might throw exceptions during its execution. It alerts the caller method to handle the potential exceptions properly.
  
- **Checked Exceptions**: The `throws` keyword is primarily used to declare checked exceptions. Checked exceptions are exceptions that must be either caught or declared in the method signature.
  
- **Unchecked Exceptions**: The `throws` keyword is not typically used to declare unchecked exceptions (such as `NullPointerException`). Unchecked exceptions are often the result of programming errors, such as failing to check for `null` before using an object.

### Example:

```java
public void someMethod() throws IOException {
    // code that might throw an IOException
}

In the example above, the someMethod declares that it may throw an IOException, and the caller method needs to handle it to avoid disrupting the program's flow.
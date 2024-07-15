# Interfaces in Java

Interfaces in Java are similar to abstract classes but with some key differences. They define a contract that classes can implement, specifying what methods a class must provide without specifying how they should be implemented.

## Key Characteristics of Interfaces:

1. **Abstraction:** Interfaces are used to achieve abstraction by defining a contract for behavior.
   
2. **Multiple Inheritance:** Java interfaces support multiple inheritance of type, allowing a class to implement multiple interfaces.

3. **Loose Coupling:** Interfaces promote loose coupling by enabling interactions between objects through contracts rather than direct implementations.

## Interface Structure:

```java
public interface InterfaceName {
    // Abstract method declaration
    void methodName();
    
    // Fields (constants)
    public static final int CONSTANT_NAME = 10;
}



In Java, interfaces provide a way to specify methods that a class must implement without specifying the details of how these methods are implemented. Here are some key points about interfaces in Java:

- All methods declared in an interface are by default `public` and `abstract`.
- All fields declared in an interface are by default `public`, `static`, and `final`, making them constants.

These properties of interfaces are fundamental to their role in Java programming, allowing for abstraction and ensuring consistency in method signatures across implementing classes.
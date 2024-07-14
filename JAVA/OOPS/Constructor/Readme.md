## Constructor

- It is a block (similar to a method) having the same name as that of the class name.
- It does not have any return type, not even `void`.
- The only modifiers applicable for constructors are `public`, `protected`, default, and `private` (`static`, `int`, `synchronized`, etc., cannot be used with constructors).
- It executes automatically when we create an object.



## Types of Constructors

### Default Constructor (No-Arg Constructor) Created by the Compiler

```java
class Test {
    Test() {
        super();
    }
    public static void main(String[] args) {
        Test t = new Test();
    }
}



## No-Arg Constructor (User-Defined)

```java
class Test {
    Test() {
        // constructor body
    }
    public static void main(String[] args) {
        Test t = new Test();
    }
}



## Parameterized Constructor

```java
class Test {
    Test(String name) {
        // constructor body
    }
    public static void main(String[] args) {
        Test t = new Test("uju");
    }
}

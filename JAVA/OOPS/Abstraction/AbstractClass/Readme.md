
# Abstract Methods and Abstract Classes in Java

1. A method without a body (no implementation) is known as an abstract method.

2. A method must always be declared in an abstract class, or we can say that if a class has an abstract method, it should be declared abstract as well.

    ```java
    abstract class Vehicle {
        int numberOfTypes;
        abstract void show();
    }
    ```

    If a method is declared in an abstract class, it is not necessary for all methods to be abstract.

3. If a regular class extends an abstract class, then the class must implement all the abstract methods of the abstract parent class or it has to be declared abstract as well.

    ```java
    class Car extends Vehicle {
        void show() {
            System.out.println("Starts with a key");
        }
    }
    ```

4. Abstract methods in an abstract class are meant to be overridden in derived concrete classes, otherwise a compile-time error will be thrown.

5. Abstract classes cannot be instantiated, meaning we can't create an object of an abstract class.

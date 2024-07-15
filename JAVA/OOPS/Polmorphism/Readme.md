# Polymorphism in Java

## Types of Polymorphism

1. **Compile-Time Polymorphism (Static Polymorphism)**
   - Achieved through method overloading.

2. **Run-Time Polymorphism (Dynamic Polymorphism)**
   - Achieved through method overriding.

## Method Overloading

1. Methods having the same name.
2. Same class.
3. Different arguments:
   - Number of arguments.
   - Sequence of arguments.
   - Type of arguments.

## Method Overriding

1. Methods having the same name.
2. Different class.
3. Same arguments:
   - Number of arguments.
   - Sequence of arguments.
   - Type of arguments.

## FAQs

1. **Can we achieve method overloading by changing the return type of the method only?**
   - In Java, method overloading is not possible by changing the return type of the method only because of ambiguity.

2. **Can we overload the Java main() method?**
   - Yes, we can have any number of main methods in a class by method overloading. This is because the main() method which receives a string array as arguments is only a convention.

### Example:

```java
public class Type {

    public static void main(String[] args) {
        System.out.println("1");
        Type t = new Type();
        t.main(20);
    }

    public static void main(int a) {
        System.out.println("2");
    }
}

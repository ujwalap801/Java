# Type Casting in Java

Type casting can be defined as:

"The process of converting a value of one data type into a value of another data type, usually to match the required data type of a variable, function, or expression."

There are two main types of type casting:

1. **Implicit Type Casting**: Automatic conversion without explicit casting syntax.
2. **Explicit Type Casting**: Manual conversion using casting syntax, such as (type) value.

In Java, type casting can be done implicitly or explicitly.

## Implicit Type Casting

Implicit type casting, also known as automatic type casting, occurs when the compiler automatically converts one data type to another without the need for an explicit cast. This happens when the types are compatible, and the conversion is safe.

### Examples:

- byte to short, int, long, or double
- short to int, long, or double
- char to int, long, or double
- int to long, or double

### Example code:

int x = 10;
double y = x; // implicit cast from int to double


## Explicit Type Casting

Explicit type casting, also known as manual type casting, occurs when the programmer explicitly uses a cast operator to convert one data type to another. This is necessary when the types are not compatible, or the conversion is not safe.

### Examples:

- **Double to Int (loses precision)**

```java
double myDouble = 10.5;
int myInt = (int) myDouble; // Explicit cast from double to int (loses precision)
System.out.println("Double value: " + myDouble); // Output: 10.5
System.out.println("Int value: " + myInt);       // Output: 10


# String in Java

- **String** is a non-primitive data type because it references a memory location where data is stored in heap memory.
- **String** is a sequence of characters.
- **String** is implemented as a class in Java.
- We can create a **String** class object using:
  ```java
  String s = new String();


Strings are immutable objects in Java.
There are three classes to create strings:
String: Immutable and thread-safe.
StringBuffer: Mutable (thread-safe).
StringBuilder: Mutable (not thread-safe).


# Immutability Concept in Java Strings

Strings in Java are immutable, which means once a String object is created, its data or state cannot be changed. Any operation that seems to modify a String actually creates a new String object.

## Why Strings are Immutable?

Strings are immutable in Java because string objects are cached in a string pool. Since cached string literals are shared among multiple references, any modification could potentially affect other parts of the program.

For example, if one reference changes its value from "mohali" to "delhi", all other references to "mohali" would reflect this change, impacting the consistency and reliability of the program.


# Why is the String Class Final?

The `String` class in Java is declared as `final`. This means that no other class can extend it. The `String` class has special features that are not available to other Java classes, and making the `String` class `final` prevents subclasses from breaking these assumptions.

**Final** is a keyword used with classes, methods, and variables. However, **immutability** is a concept used for objects in which the object's state and content cannot be changed.

## Key Points
- **Final Class:** The `String` class is declared as `final` to prevent any subclassing.
- **Special Features:** The `String` class has unique features that need to be preserved, and making it `final` helps in maintaining its integrity.
- **Immutability:** Although `final` prevents inheritance, immutability ensures that the state and content of the `String` objects cannot be changed once created.

By understanding these concepts, we can appreciate why the `String` class is designed in this manner in Java.

# Equals Method

- **Equals Method in Object Class:** Performs address or reference comparison.
- **Equals Method in String Class:** Performs content comparison.

# Why is a char array preferred over a String for storing passwords?

When storing passwords, a `char` array is often preferred over a `String` for several reasons:

1. **Immutability of String:** `String` objects are immutable, meaning once created, they cannot be modified. This immutability can pose a security risk since the password remains in memory until the garbage collector clears it. During this period, the password could be exposed through memory dumps or other means.

2. **Mutable Nature of char array:** `char` arrays are mutable, allowing for modification of the array content. After processing the password, the `char` array can be explicitly filled with zeros or other data to erase the password from memory, reducing the risk of exposure.

3. **Less Time in Memory:** With `char` arrays, the password data can be overwritten and disposed of more quickly, ensuring it doesn't linger in memory longer than necessary.

Using a `char` array for passwords enhances security by providing better control over sensitive data and minimizing the risk of unauthorized access.


## String Methods in Java

### `length()`

The `length()` method counts the number of characters in the string and returns it as an integer. This method returns the length of any string, which is equal to the number of 16-bit Unicode characters in the string.

### `isEmpty()`

The `isEmpty()` method of the String class is included in Java String. This method returns `true` if the given string is empty, else it returns `false`.

### `trim()`

The `trim()` method of the String class eliminates only leading and trailing spaces.


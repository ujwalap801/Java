

## Method Overriding Details

Method overriding allows a subclass or child class to provide a specific implementation of a method that is already provided by one of its superclasses or parent classes. The implementation in the subclass overrides (replaces) the implementation in the superclass by providing a method that has the same name, same parameters or signature, and same return type as the method in the parent class.

### Case 1: Do Overriding Methods Must Have the Same Return Type (or Subtype)?
After Java 5.0, it is possible to have a different return type for an overriding method in the child class, but the child's return type should be a subtype of the parent's return type. This phenomenon is known as covariant return type.

### Case 2: Overriding and Access Modifiers
The access modifier for an overriding method can allow more, but not less, access than the overridden method. For example, a protected instance method in the superclass can be made public, but not private, in the subclass. Doing otherwise will generate a compile-time error.

### Case 3: Overriding and Abstract Methods
Abstract methods in an interface or abstract class are meant to be overridden in derived concrete classes, otherwise a compile-time error will be thrown.

### Case 4: Invoking Overridden Method from Subclass
We can call the parent class method in an overriding method using the `super` keyword.


# Invoking Overridden Method from Subclass

In Java, we can call a parent class method in an overriding method using the `super` keyword. This is useful when we want to extend the functionality of the parent class method in the subclass.

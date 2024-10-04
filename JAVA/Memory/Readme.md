# Java Memory Management

This document provides an overview of memory management in Java, focusing on heap memory, stack memory, and the method area where static variables and methods are stored.

## Heap Memory

- **Definition**: Heap memory is the runtime data area from which memory for all class instances (objects) and arrays is allocated.
- **Thread Sharing**: Heap memory is shared among all threads in the application.
- **Garbage Collection**: Objects in the heap are managed by the garbage collector, which automatically removes objects that are no longer referenced.

## Stack Memory

- **Definition**: Stack memory is used for the execution of threads.
- **Local Variables**: It stores local variables and method call information.
- **Thread Isolation**: Each thread has its own stack memory, which is not shared with other threads.

## Method Area

Static variables and static methods are stored in a special memory area known as the **Method Area** (or **Static Area**) of the Java Virtual Machine (JVM). Below are the details:

- **Memory Structure**:
  - The Method Area is part of the heap memory where class-level data is stored.
  - It contains metadata about classes, including static variables and static methods, along with constants, and the code for methods.
  
- **Static Variables**: Unlike instance variables, which are tied to specific instances of a class, static variables belong to the class itself. This means that there is only one copy of a static variable, regardless of how many instances of the class are created.

# Class-Level Association: Static variables are shared across all instances of a class, so they need a single, consistent storage location. Storing them in static memory ensures that all instances reference the same data.
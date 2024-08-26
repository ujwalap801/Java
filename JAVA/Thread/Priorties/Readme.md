# Thread Priorities in JVM

## Overview
The Java Virtual Machine (JVM) provides a mechanism to assign priorities to threads. Based on these priorities, the JVM allocates processing time to each thread. The priority of a thread is represented by an integer value ranging from 1 to 10.

- **1**: Minimum Priority
- **5**: Normal Priority
- **10**: Maximum Priority

## Methods
- `public final void setPriority(int value)`: Sets the priority of the thread.
- `public final int getPriority()`: Returns the current priority of the thread.

## Default Behavior
- **Inheritance**: Priorities are inherited from the parent thread. By default, the main thread has a priority of 5.
- **Exception Handling**: If a priority value outside the range of 1 to 10 is set, a runtime exception (`IllegalArgumentException`) is thrown.

## Platform Dependency
- Thread priorities are platform-dependent. For example, Windows does not fully support thread priorities.

## JVM Behavior
- In cases where multiple threads have the same priority, the scheduling behavior is dependent on the JVM implementation.

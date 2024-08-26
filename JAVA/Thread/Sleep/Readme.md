# Java Thread Sleep Example

This program demonstrates the usage of the `Thread.sleep()` method in Java. The `Thread.sleep()` method is used to pause the execution of a thread for a specified period of time.

## Classes

### `Thread` Class

The `Thread` class contains the following methods:

- **`public static native void sleep(long millis) throws InterruptedException`**:  
  This method pauses the execution of the current thread for the specified number of milliseconds. The `native` keyword indicates that this method is implemented in another language, typically C or C++.

- **`public static void sleep(long millis, int nanos) throws InterruptedException`**:  
  This method pauses the execution of the current thread for the specified number of milliseconds plus an additional number of nanoseconds.

### `Test` Class

The `Test` class contains the `main` method that drives the program. It uses a loop to print numbers from 1 to 5 with a delay between each number.

```java
class Test {
    public static void main(String[] args) {
        for (int i = 1; i <= 5; i++) {
            System.out.println(i);
            try {
                // Pausing execution for 1 second (1000 milliseconds)
                Thread.sleep(1000);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }
}

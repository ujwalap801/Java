# Threads in Java

A **Thread** in Java is a lightweight process that provides the capability to execute multiple tasks concurrently within a program. Essentially, it is a sequence of execution within a program, allowing multiple operations to run in parallel rather than sequentially.

## Key Concepts of Threads

### Single-Threaded vs. Multi-Threaded

- A **single-threaded** program has only one thread, which means it can execute one task at a time.
- A **multi-threaded** program can have multiple threads, allowing it to perform several tasks simultaneously.

### Main Thread

Every Java program has at least one thread, known as the **main thread**. This thread is created automatically by the Java Virtual Machine (JVM) when the program starts. The main thread is responsible for executing the `main` method of a program.

### Thread Lifecycle

A thread in Java goes through several stages in its lifecycle:

1. **New:** The thread is created but not yet started.
2. **Runnable:** The thread is ready to run and is waiting for CPU time.
3. **Running:** The thread is actively executing.
4. **Blocked/Waiting:** The thread is waiting for a resource to become available or for another thread to complete.
5. **Terminated:** The thread has finished executing.

### Creating Threads

Threads can be created in Java by:

1. **Extending the `Thread` class** and overriding its `run()` method.
2. **Implementing the `Runnable` interface** and passing it to a `Thread` object.

### Thread Class

The `Thread` class in Java provides methods for creating and managing threads. It belongs to the `java.lang` package, so it is automatically available in any Java program without needing to import it.

## Example

Here’s a simple example demonstrating a thread in Java:

```java
public class MyThread extends Thread {
    @Override
    public void run() {
        System.out.println("Thread is running...");
    }

    public static void main(String[] args) {
        MyThread thread = new MyThread();  // Creating a new thread
        thread.start();  // Starting the thread
    }
}


# Multithreading in Java

Multithreading is a feature of Java that allows multiple threads to run concurrently. It can be used to perform several tasks simultaneously, making it a useful feature in many programming scenarios.

## Java Multithreading Basics

In Java, multithreading is implemented using the `Thread` class and the `Runnable` interface. The `Thread` class is part of the `java.lang` package.

### Creating Threads in Java

There are two primary ways to create a thread in Java:

1. **Extending the `Thread` class**
2. **Implementing the `Runnable` interface**

#### 1. Using the `Thread` Class

To create a thread by extending the `Thread` class, follow these steps:

1. **Extend the `Thread` class**
2. **Override the `run()` method**
3. **Create an object of the extended class**
4. **Start the thread**

Here's an example of how to create a thread by extending the `Thread` class:

```java
public class Test extends Thread {
    // Override the run method
    @Override
    public void run() {
        // Task to be performed by the thread
        System.out.println("Thread is running.");
    }

    public static void main(String[] args) {
        // Create an object of the class
        Test t = new Test();
        // Start the thread
        t.start();
    }
}




# Java Thread Example

In Java, you can create and manage threads using the `Runnable` interface and the `Thread` class. Below is an example demonstrating how to implement the `Runnable` interface to define a thread task and then create and start a thread.

## Runnable Interface

The `Runnable` interface is a functional interface in the `java.lang` package, which contains a single method:

```java
public interface Runnable {
    // Method to be implemented
    void run();
}


Thread Class
The Thread class, which also implements the Runnable interface, provides methods for creating and managing threads

package java.lang;

public class Thread implements Runnable {
    // Constructors
    // Methods
    void run();
    void start();
}


Example
Here's an example of how to use the Runnable interface and Thread class to create and start a thread

public class Test implements Runnable {
    // Override the run method to define the thread task
    @Override
    public void run() {
        System.out.println("Thread task");
    }

    public static void main(String[] args) {
        // Create an object of the class
        Test t = new Test();
        // Create a Thread class object and pass the Runnable instance
        Thread th = new Thread(t);
        // Start the thread
        th.start();
    }
}



Here's how you can format the provided text into a README.md file:

markdown
Copy code
# Java Thread Example

In Java, you can create and manage threads using the `Runnable` interface and the `Thread` class. Below is an example demonstrating how to implement the `Runnable` interface to define a thread task and then create and start a thread.

## Runnable Interface

The `Runnable` interface is a functional interface in the `java.lang` package, which contains a single method:

```java
public interface Runnable {
    // Method to be implemented
    void run();
}
Thread Class
The Thread class, which also implements the Runnable interface, provides methods for creating and managing threads:

java
Copy code
package java.lang;

public class Thread implements Runnable {
    // Constructors
    // Methods
    void run();
    void start();
}
Example
Here's an example of how to use the Runnable interface and Thread class to create and start a thread:

java
Copy code
public class Test implements Runnable {
    // Override the run method to define the thread task
    @Override
    public void run() {
        System.out.println("Thread task");
    }

    public static void main(String[] args) {
        // Create an object of the class
        Test t = new Test();
        // Create a Thread class object and pass the Runnable instance
        Thread th = new Thread(t);
        // Start the thread
        th.start();
    }
}


Why Use Runnable Interface?
Using the Runnable interface is often preferred over directly extending the Thread class because it allows your class to extend another class while still being able to use threading. It provides better flexibility and supports separation of concerns.


public class Test  extends Thread{
    //Override the run method
    public void run()
    {
        //thread
        //task
        System.out.println("thread task");
    }
    public static void main(String[] args) {
        //Create an object of the class
        Test t = new Test();
        t.start(); //start the thread
        t.start();//runtime exception
    }
}

output is: runtime exception
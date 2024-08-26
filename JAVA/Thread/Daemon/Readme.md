# Daemon Thread in Java

A **Daemon Thread** is a thread that runs in the background to support other non-daemon threads. These threads typically provide services to user threads.

### Use Cases
Daemon threads are used to perform background tasks such as:
- Garbage Collection
- Attach Listeners
- Signal Dispatch
- Spell Checker in Word Processors

### Methods
Java provides two key methods related to daemon threads:
1. `public final void setDaemon(boolean b)`: This method marks the thread as a daemon thread if the argument `b` is `true`.
2. `public final boolean isDaemon()`: This method returns `true` if the thread is a daemon thread.

### Important Cases
- **Case 1**: A thread must be set as a daemon before it is started. If you try to set a thread as a daemon after it has started, a `RuntimeException` will be thrown (`IllegalThreadStateException`).
- **Case 2**: The main thread cannot be set as a daemon thread.

### Life Cycle
The life of a daemon thread depends on the life of the user threads it is supporting. If all user threads die, the JVM will terminate the daemon threads as well.

### Daemon Nature
A daemon thread inherits the nature or properties of its parent thread.

### Priority
Daemon threads generally have lower priorities compared to user threads, but this priority can be changed as needed.


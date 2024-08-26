### `join()` Method

If a thread wants to wait for another thread to complete its task, it should use the `join()` method.

#### Method Signatures:

```java
public final void join() throws InterruptedException


public final synchronized void join(long ms)

public final synchronized void join(long ms, int ns)

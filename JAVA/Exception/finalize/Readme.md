finalize() Method
Description:
The finalize() method is used to perform cleanup operations before an object is deleted by the garbage collector. It is a method that can be overridden to provide custom cleanup logic for an object.

protected void finalize() throws Throwable {
    // Cleanup code
}


Key Points:

The finalize() method is invoked just before an object is garbage collected.
It is useful for closing resources like file streams, database connections, or any other resources that need to be released before the object is removed from memory.
The method is protected and can be overridden in a class to define custom cleanup actions.


public class ResourceHandler {
    
    // Some resource initialization code
    public void openResource() {
        // Open a connection or resource
    }
    
    @Override
    protected void finalize() throws Throwable {
        try {
            // Cleanup code to close the resource
            closeResource();
        } finally {
            super.finalize();
        }
    }

    public void closeResource() {
        // Code to close the resource
    }
}


Note:

It is recommended to avoid relying on finalize() for critical resource management because there is no guarantee on the timing of its execution.
Consider using try-with-resources or finally blocks for more reliable resource management.
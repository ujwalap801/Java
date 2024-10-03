## Explanation of `public static void main(String[] args)`


we can have many java class 
we can have only one public class in  a java program


### public
**Access Modifier**: `public` is an access modifier that means this method is accessible from anywhere. In the context of the main method, it means that the Java runtime can call this method from outside the class when the program starts.

### static
**Static Method**: `static` means that this method belongs to the class itself, rather than an instance of the class. This allows the Java runtime to call the main method without needing to create an instance of the class. The main method is the entry point of the program, so it must be accessible without creating an object.

### void
**Return Type**: `void` means that this method does not return any value. The main method is designed to perform actions (like running the application) rather than compute and return a value.

### main
**Method Name**: `main` is the name of the method that the Java runtime looks for when it starts a program. It is a special method in Java that serves as the entry point of any Java application.

### String[] args
**Parameter**: This is an array of `String` objects, named `args`. It represents the command-line arguments that are passed to the program when it is run. Each element of the array is one of the arguments provided on the command line.

- **String**: The type of the array elements, which are strings.
- **[]**: Indicates that `args` is an array.
- **args**: The name of the array variable that holds the command-line arguments.


## Can a program be excuted without main method?
# Before JDK 7:
The main method was not mandatory.
You could write code in a static block, and it would run when the class was loaded, since the static block gets executed before the main() method.
If a main method was not present, the program could still execute the static block, but it would result in an exception after the block executed, as no main method would be found.
You could avoid the exception by using System.exit(0) at the end of the static block.

# From JDK 7 onwards:
The main method is mandatory.
When running a program, the JVM looks for the main method to begin execution. If it does not find the main method, an error occurs: "main method not found in the class".
This is not an exception, but a verification error since the bytecode doesn't contain the main method needed to execute the program.
The program will still compile without the main method, but it will fail during execution.
In summary, from JDK 7 and later, the main method is compulsory for program execution.


# Example Before JDK 7 (No main() method, using a static block):
public class Test {
    // Static block
    static {
        System.out.println("Static block executed.");
        System.exit(0);  // This prevents the program from looking for a main method.
    }
}

# Explanation:

In this code, the static block is executed as soon as the class is loaded. Since System.exit(0) is called, the program exits gracefully before the JVM can complain about the missing main() method.


# Example After JDK 7 (Mandatory main() method):
public class Test {
    // Static block
    static {
        System.out.println("Static block executed.");
    }

    // main method
    public static void main(String[] args) {
        System.out.println("Main method executed.");
    }
}


# Explanation:

In this code, both the static block and the main() method are present. When you run the program, the static block will execute first, followed by the main() method.
Output:

Static block executed.
Main method executed.



## If no main() method is provided after JDK 7:

public class Test {
    static {
        System.out.println("Static block executed.");
    }
}

# Explanation:

In JDK 7 or later, if you run this program, you'll get an error:

Error: Main method not found in class Test, please define the main method as:
public static void main(String[] args)
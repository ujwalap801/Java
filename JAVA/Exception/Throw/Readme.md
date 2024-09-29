throw keyword in Java is used to explicitly throw an exception, including user-defined or custom exceptions. This allows you to create and handle exceptions specific to your application's needs. When you use the throw keyword, you must also specify an exception object (which can be an instance of any subclass of Throwable).


Ex:
// Define a custom exception by extending the Exception class
class MyCustomException extends Exception {
    public MyCustomException(String message) {
        super(message);
    }
}

public class CustomExceptionDemo {
    public static void main(String[] args) {
        try {
            // Call a method that might throw a custom exception
            validateAge(15);
        } catch (MyCustomException e) {
            // Handle the custom exception
            System.out.println("Caught the custom exception: " + e.getMessage());
        }
    }

    // Method to validate age, throwing a custom exception if age is invalid
    static void validateAge(int age) throws MyCustomException {
        if (age < 18) {
            // Throw the custom exception with a custom message
            throw new MyCustomException("Age must be at least 18 to proceed.");
        } else {
            System.out.println("Age is valid.");
        }
    }
}


Explanation:
Custom Exception: MyCustomException extends the Exception class, allowing it to be treated like any other exception.
Throwing the Exception: The validateAge method checks the age and uses the throw keyword to throw a MyCustomException if the age is less than 18.
Handling the Exception: In the main method, the exception is caught using a try-catch block, and the custom message is printed.
This approach helps you create meaningful and specific exceptions that make your code easier to debug and maintain.
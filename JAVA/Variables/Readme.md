# Java Variables

A Java variable is a piece of memory that can contain a data value. A variable thus has a data type. Variables are typically used to store information which your Java program needs to do its job. A variable's value can be changed.

## Types of Variables
1. **Local Variables**
2. **Instance (Global) Variables**
3. **Static Variables**

### Local Variables
Definition: Variables declared inside a method, constructor, or block.

Scope: Available only within the block or method in which they are declared.

No Default Value: Local variables must be initialized before use.


#Example
public class LocalVariableExample {
    public void display() {
        int localVar = 10; // Local variable
        System.out.println("Local variable value: " + localVar);
    }

    public static void main(String[] args) {
        LocalVariableExample obj = new LocalVariableExample();
        obj.display();
    }
}

# Explanation:
localVar is a local variable, declared and initialized inside the display() method. It is only accessible within that method.

# output :
Local variable value: 10

### Instance (Global) Variables
Definition: Variables declared inside a class but outside of any method or constructor. Each instance of the class has its own copy.

Scope: Accessible within the whole class, but each instance of the class has its own copy.

Default Values: If not initialized, they get default values (e.g., 0 for numbers, null for objects, etc.).


# Example
 public class InstanceVariableExample {
    int instanceVar; // Instance variable

    public void display() {
        System.out.println("Instance variable value: " + instanceVar);
    }

    public static void main(String[] args) {
        InstanceVariableExample obj1 = new InstanceVariableExample();
        obj1.instanceVar = 5;
        obj1.display();

        InstanceVariableExample obj2 = new InstanceVariableExample();
        obj2.instanceVar = 10;
        obj2.display();
    }
}

# Explanation:
instanceVar is an instance variable. Each object (obj1 and obj2) has its own copy of this variable.
obj1.instanceVar is set to 5, while obj2.instanceVar is set to 10.


# output:
Instance variable value: 5
Instance variable value: 10

### Static Variables
Definition: Variables declared with the static keyword inside a class. They are shared among all instances of the class.

Scope: Accessible across all instances of the class.

Default Values: Like instance variables, they are initialized to default values if not explicitly initialized.


# Example:
public class StaticVariableExample {
    static int staticVar = 100; // Static variable

    public void display() {
        System.out.println("Static variable value: " + staticVar);
    }

    public static void main(String[] args) {
        StaticVariableExample obj1 = new StaticVariableExample();
        obj1.display();

        StaticVariableExample obj2 = new StaticVariableExample();
        obj2.staticVar = 200; // Modifies the static variable
        obj2.display();
        
        obj1.display(); // Reflects the change in static variable
    }
}


# Explanation:
staticVar is a static variable. It is shared across all instances (obj1 and obj2) of the class.
When obj2.staticVar is set to 200, this change is reflected across all objects. obj1.display() will now print 200, showing the change.

# output:
Static variable value: 100
Static variable value: 200
Static variable value: 200

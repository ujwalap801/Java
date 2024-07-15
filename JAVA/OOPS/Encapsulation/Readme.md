# Encapsulation in Java

Encapsulation in Java is a mechanism of wrapping the data (variables) and code acting on the data (methods) together as a single unit.

## Steps to Achieve Encapsulation

1. Declare the variables of a class as private.
2. Provide public setter and getter methods to modify and view the variables' values.

In encapsulation, the variables of a class will be hidden from other classes and can be accessed only through the methods of their current class. This concept is known as data hiding.

```java
class Employee {
    private int emp_id; // Data hiding

    public void setEmpId(int emp_id1) {
        emp_id = emp_id1;
    }

    public int getEmpId() {
        return emp_id;
    }
}

# In Java, a wrapper class is an object representation of a primitive data type. It allows primitive types (such as int, char, float, etc.) to be treated as objects. Each primitive data type has a corresponding wrapper class in the java.lang package. 


# Example :For instance, int is a primitive type, but Integer is its wrapper class that allows int values to be used as objects.

int primitiveValue = 10;
Integer wrapperObject = Integer.valueof(primitiveValue); // Autoboxing
int unboxedValue = wrapperObject; // Unboxing


# Autoboxing:
 Autoboxing is the automatic conversion of a primitive data type (e.g., int, char, double, etc.) into its corresponding wrapper class object (e.g., Integer, Character, Double, etc.).

 Ex :
 int num = 5;
Integer obj = num; // Autoboxing: Primitive 'int' to 'Integer'



# Unboxing:
 Unboxing is the reverse of autoboxing, where a wrapper class object is automatically converted back into its corresponding primitive data type.


 Ex :
 Integer obj = 10;
int num = obj; // Unboxing: 'Integer' object to primitive 'int'

# In Java, you cannot directly check the type of a primitive data type using something like instanceof because primitives (int, char, boolean, etc.) are not objects. 

##  1. Checking Types for Objects using instanceof


class HelloWorld {
    public static void main(String[] args) {
       
       Object a =10; // Autoboxing int to Integer
     
       if(a instanceof Integer)
       {
           System.out.println("a is of type, Integer");
       }
       else{
            System.out.println("a is not integer");
       }
       
       
       String b ="Hello"; //string is not a primitive data type
       if (b instanceof String) {
            System.out.println("b is a String.");
        }else {
            System.out.println("b is a not  String.");
        }
 
    }
}


# output:
a is of type, Integer
b is a String.

## Type Identification for Primitives



class HelloWorld {
    public static void main(String[] args) {
       
       int a =5;
      double b =4.5;
       
    //   Using wrapper class
    Integer wrapInt = Integer.valueOf(a);
    Double wrapDouble =  Double.valueOf(b);
    
    if(wrapInt instanceof Integer)
    {
        System.out.println("wrapInt is of type Integer");
    }

    
    if (wrapDouble instanceof Double)
    {
           System.out.println("wrappedDouble is of type Double.");
    }
       
    }
}


# output
wrapInt is of type Integer
wrappedDouble is of type Double.
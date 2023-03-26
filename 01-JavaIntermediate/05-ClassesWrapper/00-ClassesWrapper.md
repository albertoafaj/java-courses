# Classes Wrapper

In Java, a wrapper class is used to convert a primitive data type into an object. Wrapper classes provide a way to use primitive data types as objects. Each primitive data type has a corresponding wrapper class in Java. The eight primitive data types are: byte, short, int, long, float, double, boolean and char. The corresponding wrapper classes are Byte, Short, Integer, Long, Float, Double, Boolean and Character.

Wrapper classes are often used when working with collections such as ArrayList or when passing arguments to methods that require objects rather than primitive data types.

Here's an example of using a wrapper class in Java:

```
// primitive data type
int i = 10;

// wrapper class
Integer integer = Integer.valueOf(i);

// printing the value of the wrapper class
System.out.println(integer);
```

In this example, we first declare a primitive data type int with a value of 10. We then create an instance of the wrapper class Integer and pass in the value of i using the valueOf() method. Finally, we print out the value of the wrapper class integer. The output will be 10.
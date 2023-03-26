# Collections

In Java, the Collections framework provides a set of interfaces and classes for working with groups of objects, such as lists, sets, and maps. These classes and interfaces provide a variety of methods for sorting, searching, and manipulating collections of objects.

Here's an example of how to use the ArrayList class from the Collections framework:

```
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        
        list.add("apple");
        list.add("banana");
        list.add("cherry");
        
        for (String fruit : list) {
            System.out.println(fruit);
        }
        
        System.out.println("The list contains " + list.size() + " elements.");
    }
}
```
In this example, we import the ArrayList class from the Collections framework and create a new ArrayList object called list. We then use the add method to add three elements (strings) to the list. Finally, we use a for-each loop to iterate over the elements of the list and print them to the console, and we use the size method to print the number of elements in the list.

The output of this program is:

```
apple
banana
cherry

```
The list contains 3 elements.

The Collections framework provides many other classes and interfaces for working with different types of collections, such as HashSet, TreeMap, and LinkedList. Each class and interface provides a different set of methods and behaviors that are optimized for specific use cases. By using the appropriate collection class or interface for your needs, you can simplify your code and improve its performance.
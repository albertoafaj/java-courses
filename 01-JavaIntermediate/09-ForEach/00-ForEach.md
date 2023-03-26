# ForEach

In Java, forEach is a method that can be used to iterate over the elements of a collection or an array. It allows you to perform an action on each element of the collection, without the need for a traditional for loop.

Here's an example of using forEach in Java:

``` 
// creating an array
int[] numbers = {1, 2, 3, 4, 5};


// using forEach to iterate over the array
Arrays.stream(numbers)
      .forEach(n -> System.out.println(n));

      ```
      
In this example, we first create an array of integers numbers. We then use the Arrays.stream() method to convert the array into a stream. We can then use the forEach() method on the stream to print out each element of the array.

The forEach() method takes a lambda expression as its parameter, which defines the action to be performed on each element of the collection. In this case, we use a lambda expression to print out each element of the array.

The forEach() method can also be used with collections, such as List and Set, in a similar way.

Using forEach in Java can make code more concise and readable, by removing the need for a traditional for loop. It can also be used in conjunction with other stream methods to perform complex operations on collections or arrays.
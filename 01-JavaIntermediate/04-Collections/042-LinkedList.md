# LinkedList 

LinkedList is a class in Java that implements the List interface and provides a linked list data structure. Here's an example of how to create a LinkedList in Java:

```
LinkedList<String> linkedList = new LinkedList<>();
linkedList.add("apple");
linkedList.add("banana");
linkedList.add("cherry");
```

This creates a new LinkedList of strings, adds three elements to it, and stores it in the linkedList variable.

Here are some of the commonly used methods of the LinkedList class in Java:

1. add(E element): adds the specified element to the end of the list.
2. add(int index, E element): inserts the specified element at the specified position in the list.
3. addAll(Collection<? extends E> c): appends all of the elements in the specified collection to the end of the list, in the order that they are returned by the collection's iterator.
4. clear(): removes all of the elements from the list.
5. contains(Object o): returns true if the list contains the specified element.
6. get(int index): returns the element at the specified position in the list.
7. indexOf(Object o): returns the index of the first occurrence of the specified element in the list, or -1 if the list does not contain the element.
8. remove(int index): removes the element at the specified position in the list.
9. remove(Object o): removes the first occurrence of the specified element from the list, if it is present.
10. set(int index, E element): replaces the element at the specified position in the list with the specified element.
11. size(): returns the number of elements in the list.
12. 
These are just a few of the methods provided by the LinkedList class in Java. There are many more methods available for manipulating and accessing elements in the list.
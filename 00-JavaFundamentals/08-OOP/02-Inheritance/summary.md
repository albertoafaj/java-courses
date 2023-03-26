# Inheritance 

Inherfeat: exemplify class in java fundamentalsitance is a fundamental concept in object-oriented programming that allows one class to inherit the properties and methods of another class. In Java, a class can inherit from another class using the extends keyword. Here's an example of inheritance in Java:

```
public class Animal {
    public void eat() {
        System.out.println("The animal is eating.");
    }
}

public class Dog extends Animal {
    public void bark() {
        System.out.println("The dog is barking.");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog myDog = new Dog();
        myDog.eat(); // outputs "The animal is eating."
        myDog.bark(); // outputs "The dog is barking."
    }
}
```

In this example, we have defined two classes Animal and Dog, where Dog extends Animal. The Animal class has a single method eat, which outputs a message indicating that the animal is eating. The Dog class has an additional method bark, which outputs a message indicating that the dog is barking.

We then create an instance of the Dog class and call the eat and bark methods on it. Since Dog extends Animal, it inherits the eat method from the Animal class and can also access its own bark method.

By using inheritance, we can reuse code and avoid duplication by defining common properties and methods in a parent class and allowing child classes to inherit them. This helps to make our code more modular, maintainable, and extensible.
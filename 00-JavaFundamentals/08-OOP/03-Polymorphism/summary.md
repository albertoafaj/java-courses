# Polymorphism
Polymorphism is a fundamental concept in object-oriented programming that allows objects of different classes to be treated as if they are objects of the same class. In Java, polymorphism can be achieved through two mechanisms: method overloading and method overriding.

Method overloading occurs when two or more methods in the same class have the same name but different parameters. When a method is called with a certain set of parameters, the compiler determines which version of the method to call based on the type and number of the parameters.

Method overriding occurs when a subclass provides its own implementation of a method that is already defined in its parent class. The signature of the overridden method must match that of the parent method, but the implementation can be different.

Here's an example of polymorphism in Java using method overriding:

```
public class Animal {
    public void makeSound() {
        System.out.println("The animal makes a sound.");
    }
}

public class Dog extends Animal {
    public void makeSound() {
        System.out.println("The dog barks.");
    }
}

public class Cat extends Animal {
    public void makeSound() {
        System.out.println("The cat meows.");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal myAnimal = new Animal();
        Animal myDog = new Dog();
        Animal myCat = new Cat();
        
        myAnimal.makeSound(); // outputs "The animal makes a sound."
        myDog.makeSound(); // outputs "The dog barks."
        myCat.makeSound(); // outputs "The cat meows."
    }
}

```
In this example, we have defined a parent class Animal and two subclasses Dog and Cat. Each class has its own implementation of the makeSound method. We then create instances of each class and call the makeSound method on them. Since the Dog and Cat classes override the makeSound method from the Animal class, their own implementation of the method is called when the method is invoked on their instances.

By using polymorphism, we can write more flexible and reusable code by treating objects of different classes as if they are objects of the same class. This helps to make our code more modular, maintainable, and extensible.
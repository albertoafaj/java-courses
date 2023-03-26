# Interfaces

In Java, an interface is a collection of abstract methods and constants that define a set of actions or behaviors that can be implemented by classes.

Interfaces serve as a contract between a class that implements the interface and the code that uses the interface. The implementing class must provide concrete implementations for all the abstract methods declared in the interface.

Interfaces can also define default methods, which provide an implementation that can be used by implementing classes. In addition, interfaces can contain static methods and nested types.

Java supports multiple inheritance of interfaces, which means that a class can implement multiple interfaces. Interfaces are also used extensively in Java to achieve abstraction and decoupling between components.

Here's an example of an interface in Java:

``` 
// Define an interface for a vehicle that can accelerate and brake
public interface Vehicle {
    // Method for accelerating the vehicle
    void accelerate(int speed);

    // Method for braking the vehicle
    void brake();
}
```
In this example, we've defined an interface called Vehicle that includes two methods: accelerate and brake. Any class that implements this interface must provide a concrete implementation for these methods. For example, here's how we could define a class Car that implements the Vehicle interface:

```
public class Car implements Vehicle {
    private int speed;

    public void accelerate(int speed) {
        this.speed += speed;
    }

    public void brake() {
        this.speed = 0;
    }

    // Other methods specific to the Car class
}
```

In this example, we've defined a Car class that implements the Vehicle interface. The accelerate method increases the car's speed by the specified amount, while the brake method sets the speed to zero. Because we've implemented the Vehicle interface, we can use this Car object anywhere that a Vehicle object is expected, without having to worry about the specific implementation details of the Car class.
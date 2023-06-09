---
title: "#JavaBeginnerToAdvanced: Inheritance, Interface and Polymorphism!"
date: 2023-03-31T23:23:00-03:00
draft: false
cover: 
    image: img/javaBeginerToAdvanced.jpg
    alt: 'This is a post image'
    caption: 'this is the caption'
---

---
#  Inheritance, Interface and Polymorphism!
### Understand the concepts and the differences!

Inheritance:

In Java, inheritance is a fundamental object-oriented programming concept that allows you to create new classes (known as subclasses or derived classes)
based on existing classes (known as superclasses or base classes). The inheritance relationship establishes an "is-a" relationship between classes,
 where the subclass inherits the properties and behaviors of the superclass.

To define a subclass and establish inheritance, you use the extends keyword. Here's the syntax: 



       class Subclass extends Superclass {
        // subclass members and methods
        }


In this syntax, Subclass is the name of the new class you want to create, and Superclass is the name of the existing class you want to inherit from.

The subclass inherits all the non-private members (fields and methods) of the superclass. This includes instance variables, instance methods, and nested classes. However, constructors, private members, and static members are not inherited.

You can override inherited methods in the subclass to provide a specialized implementation. This is known as method overriding. To override a method, you define a method with the same signature (name, return type, and parameters) in the subclass. You can use the @Override annotation to indicate that you intend to override a method (optional but recommended for clarity).

Here's an example that demonstrates inheritance and method overriding:

       class Vehicle {
            void start() {
                System.out.println("Vehicle started.");
            }
        }

        class Car extends Vehicle {
            @Override
            void start() {
                System.out.println("Car started.");
            }
        }

        public class Main {
            public static void main(String[] args) {
                Vehicle vehicle = new Vehicle();
                vehicle.start();  // Output: Vehicle started.

                Car car = new Car();
                car.start();      // Output: Car started.
            }
        }

In this example, the Car class extends the Vehicle class. It overrides the start() method to provide a different implementation specific to cars. When the start() method is called on a Car object, it prints "Car started." If the start() method is called on a Vehicle object, it prints "Vehicle started."

Inheritance allows code reuse, promotes code organization, and supports the concept of polymorphism, where objects of different classes can be treated as instances of a common superclass.


Interface:

An interface defines a contract of methods that a class must implement. It specifies a set of abstract methods that define the behavior expected from implementing classes. Interfaces provide a way to achieve multiple inheritance, as a class can implement multiple interfaces.

Example:

        interface Flyable {
            void fly();
        }

        class Bird implements Flyable {
            @Override
            void fly() {
                System.out.println("Bird flies");
            }
        }

In this example, Flyable is an interface that declares the fly() method. The Bird class implements the Flyable interface and provides an implementation for the fly() method.



Polymorphism:

Polymorphism is the ability of an object to take on many forms. In Java, polymorphism is achieved through inheritance and interfaces. It allows you to treat objects of different classes that share a common superclass or interface as instances of that superclass or interface.

Example:

            Animal animal1 = new Animal();
            Animal animal2 = new Dog();

In this example, both animal1 and animal2 are of type Animal. However, animal1 is an instance of the Animal class, while animal2 is an instance of the Dog class, which is a subclass of Animal. Since Dog inherits from Animal, it can be treated as an Animal object. This is polymorphism in action.


In summary, inheritance allows classes to inherit properties and behaviors from other classes, interfaces define contracts for implementing classes, and polymorphism enables objects to be treated as instances of their superclass or interface, allowing for flexibility and extensibility in object-oriented programming.
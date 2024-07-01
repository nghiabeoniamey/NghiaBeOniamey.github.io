---
title: "Java OOP"
date: 2024-07-02 08:00:00 - 0500
categories: [ OOP, Java, Java OOP ]
tags: [ OOP, Java, Java OOP ]
image:
  path: /assets/img/headers/java/java-oop.png
  # I don't have lqip: data:image/webp;base64,iVBORw0KGgoAAAANSUhEUgAAAAoAAAAGCAMAAADNLv/0AAAAmVBMVEW6wsiOnqmNnKqNnaqNnKmwucJjeIoMLkoIK0QHK0QHLEQGKkQEJ0IEJkMAIkBIXnFkeYsaOVMUNk0PMUoNMEoKLUgGKEQAIT9GXHBfdIcPM0gQNUgQM0wPMEwJK0YFJkQBI0AAID5fdIYKMEMJMUMJLkUGLUUDKEEHKEUFJ0RFW2+gq7RmeYVleYVleIVkdoZldoZjdYWNmaMIZDnWAAAAR0lEQVQIHWNgYGQCAWYWVgY2dg5OLm4eXj5+BgFBIWERUTFecQkGSSlpGVk5eQVFCQYlZRVVNXUNTUUtBm0dHV09fX0DQyMAdocFpbQkwGsAAAAASUVORK5CYII=
---

# Object Oriented Programming In Java Specialization, Java OOP

## Java - What is OOP?

Object Oriented Programming in Java is the use of real-world objects containing different methods and functions inside
classes. It is used to implement inheritance, encapsulation, polymorphism, and abstraction with the help of Java. It
simplifies the programming by providing easier modification and reusability.

Object-oriented programming has several advantages over procedural programming:

- OOP is faster and easier to execute
- OOP provides a clear structure for the programs
- OOP helps to keep the Java code DRY "Don't Repeat Yourself", and makes the code easier to maintain, modify and debug
- OOP makes it possible to create full reusable applications with less code and shorter development time

1. [ ] Tip: The "Don't Repeat Yourself" (DRY) principle is about reducing the repetition of code. You should extract out
   the codes that are common for the application, and place them at a single place and reuse them instead of repeating
   it.

## Java - What are Classes and Objects?

Classes and objects are the two main aspects of object-oriented programming.

Look at the following illustration to see the difference between class and objects:

| class  | object            |
|--------|-------------------|
| Animal | Dog - Cat - Panda | 

Another example:

| class  | object                    |
|--------|---------------------------|
| Family | Father - Mother - Oniamey | 

So, a class is a template for objects, and an object is an instance of a class.

When the individual objects are created, they inherit all the variables and methods from the class.

## Association in OOPs

Association in oops is used to represent the relationship between various objects. There are many ways in which one
object can be associated with one or many other objects. Let us know about four major types of associations in OOPs.

* One to One
* One to Many
* Many to One
* Many to Many

## Aggregation in OOPs

Aggregation is a relationship that shows ‘has-a’ connection between one or many entities. One class contains the
reference to another. In associations, deleting one class does not affect the other class object.

```java
 class Dress {

    private String name;

    public Dress(String name) {

        this.name = name;

    }

    public String setName() {

        return name;

    }

}

class Girl {

    private String name;

    public Girl(String name) {

        this.name = name;

    }

    public void wear(Dress dress) {
    
      Dress herDress = new Dress('Sundress');
      Girl her = new Girl('Nguyễn Thu Phương');

       System.out.println(her + ” is wearing a ” + herDress);

    }

}

public class AggregationExample {

    public static void main(String[] args) {

        Car myCar = new Car(“Toyota”);

        Driver me = new Driver(“John”);

        me.drive(myCar);

    }

} 
 ```

## Composition in OOPs

Composition in Java oops is a type of relationship which represents strong relationship between objects. It refers to
the “Belong to association”. The objects in composition cannot exist independently.

```java
class Engine {

    public void start() {

        System.out.println(“Engine started”);

    }

}

class Car {

    // using contructor injection
    private Engine engine;

    public Car() {

        this.engine = new Engine();

    }

    public void start() {

        System.out.println(“Car started”);

        engine.start();

    }

}

public class CompositionExample {

    public static void main(String[] args) {

        Car myCar = new Car();

        myCar.start();

    }

}
 ```

Inheritance and Interfaces
Java OO Tutorial (review Object and Class, read the rest)
Object-Oriented Programming Concepts
*This lesson will introduce you to objects, classes, inheritance, interfaces, and packages.

What Is an Object?
* objects share two characteristics: They all have state(fileds) and behavior(methods)
benefits of Bundling code into individual software objects
- Modularity
- Information-hiding
- Code re-use
- Pluggability and debugging ease

What Is a Class?
A class is a blueprint or prototype from which objects are created.

What Is Inheritance?
* Object-oriented programming allows classes to inherit commonly used state and behavior from other classes
*  In the Java programming language, each class is allowed to have one direct superclass, and each superclass has the potential for an unlimited number of subclasses:
```
class MountainBike extends Bicycle {

    // new fields and methods defining 
    // a mountain bike would go here

}

```
What Is an Interface?
 interface is a group of related methods with empty bodies.
What Is a Package?
A package is a namespace that organizes a set of related classes and interfaces
* The Java platform provides an enormous class library (a set of packages) suitable for use in your own applications
* This library is known as the "Application Programming Interface", or "API" for short
* The Java Platform API Specification contains the complete listing for all packages, interfaces, classes, fields, and methods supplied by the Java SE platform.

##Java Inheritance & Interfaces Tutorial
*  A class that is derived from another class is called a subclass (
*  The class from which the subclass is derived is called a superclass (
* Constructors are not members, so they are not inherited by subclasses, but the constructor of the superclass can be invoked from the subclass.
* A subclass inherits all of the public and protected members of its parent, 
* You can declare a field in the subclass with the same name as the one in the superclass, thus hiding it (not recommended).
* You can declare new fields in the subclass that are not in the superclass.
* You can declare new methods in the subclass that are not in the superclass.
* You can write a subclass constructor that invokes the constructor of the superclass, either implicitly or by using the keyword super.
* A subclass does not inherit the private members of its parent class.
* You can make a logical test as to the type of a particular object using the instanceof operator













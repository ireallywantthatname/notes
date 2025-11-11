---
title: Classes and Objects
summary: "Object-oriented programming basics in C# including class templates, object instantiation, attributes, and methods with practical examples"
---

## Classes and Objects in C\#

1. **What is a class?**

- Is a template from which objects are created.

2. **What is an object?**

- Objects are instances of classes which creates unique entities in a defined structure.

**Syntax for creating an object out of a class**

```cs
class_name object_name = new class_name();
```

## Class members in C\#

- Class members refers to attributes and methods in a class.

  - **Attribute** - Refers to in-class variables which defines distinct characteristics of a class.
  - **Methods** - These define the behavior of the class.

- The definition of a class simply requires the **class** keyword and the _class_name_.

Ex:

```cs
class class_name {
	//define a class
}
```

**Example of a class**

```cs
class Dog {
	int numOfHair; //attribute
	void bark (); //method
}
```

**Task 01**

- Create a program which has a class called "Vehicle". Vehicle has 3 members.
  1.  Brand
  2.  No. of wheels
  3.  Sound ()
      Implement the class vehicle and print out the sound ()

```cs
class Vehicle {
	string brand;
	int noOfWheels;
	void Sound ();
}

Console.WriteLine(Vehicle.Sound());
```

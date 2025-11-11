---
title: Getters Setters and Inheritance
summary: "Property getters and setters for encapsulation, plus inheritance concepts with base classes, derived classes, and code reusability"
---

**Task 01**

- Create a class called EncapData and create two private variables to store radius value and pi value.
- Inside the main class you have to get the radius value from the user and pass it to EncapData Class.
- Inside EncapData.cs class create getters and setters to find the Area of the circle and to find the circumference of the circle.

* Return the answers from the EncapData Class
* Display the answers inside Main class (program).

```cs
class EncapData
{
    private double radius;
    private double pi = Math.PI;
    public double Radius
    {
        get { return radius; }
        set { radius = value; }
    }
    public double Area()
    {
        return pi * Math.Pow(radius, 2);
    }
}

public class Program
{
    public static void Main(string[] args)
    {
        EncapData newEncapData = new EncapData();
        Console.Write("Enter the radius: ");
        newEncapData.Radius = Convert.ToDouble(Console.ReadLine());
        Console.WriteLine($"The area is: {newEncapData.Area()}");
    }
}
```

## Inheritance

- Inheritance allows a derived class _(child class, sub class)_ to inherit, extend or modify the behavior of the base class _(parent class, super class)_

#### Advantages of inheritance

- Code organization.
- **Syntax of inheritance**

```cs
Class A { //parent class
	// ...
}
Class B : A { //child class (B is inherited from A)
	// ...
}
```

**Example**

```cs
public class Person {
	public name;
	public age;
	public nic;
}
public class Lecturer : Person {
	public empNo;
}
public class Student : Person {
	public sId;
}
```

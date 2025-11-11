---
title: Polymorphism Method Overloading and Overriding
summary: "Polymorphism in C# including compile-time method overloading with different parameter lists and runtime method overriding in derived classes"
---

**TASK 01**

- Imagine you are designing a system for vehicles.
- Create two C# classes:
- A base abstract class called Vehicle with a property string Make that should be initialized through a constructor.
- A derived class called Car that inherits from Vehicle and has an additional property int NumberOfDoors.
- The Car class should have a constructor that takes arguments to initialize both its own NumberOfDoors property and the Make property of the Vehicle class.• Provide the C# code for both the Vehicle and Car classes.
- Print "My Car is a Ferarri with 2 doors." in the main function.

```cs
public abstract class Vehicle
{
    public string Make { get; set; }
    public Vehicle(string make)
    {
        Make = make;
    }
}

public class Car : Vehicle
{
    public int NumOfDoors { get; set; }
    public Car(string make, int numOfDoors) : base(make)
    {
        NumOfDoors = numOfDoors;
    }
    public void StartEngine()
    {
        Console.WriteLine("BRR...");
    }
    public void Main(string[] args)
    {
        Car car1 = new("Akash", 4);
        car1.StartEngine();
    }
}
```

## Polymorphism

- Polymorphism is when a single action is capable of being executed in different ways.

- There are 2 main types of polymorphism,

  1.  Compile-time polymorphism
  2.  Runtime polymorphism

#### 1. Method overloading (Compile-time polymorphism)

- In a single class having multiple methods in the same name but with different parameter lists is known as _method overloading_.

```cs
    public void display(int a)
    {
        Console.WriteLine($"Parameter is {a}");
    }
    public void display(int a, int b)
    {
        Console.WriteLine($"Parameters are {a} and {b}");
    }
    public void display(int a, int b, int c)
    {
        Console.WriteLine($"Parameters are {a}, {b} and {c}");
	}
```

**Question**

- Create a method called calculator and try adding method overloading.

```cs
public class Calculator
{
    int Add(int a, int b)
    {
        return a + b;
    }
    int Add(int a, int b, int c)
    {
        return a + b + c;
    }
    double Add(double a, double b)
    {
        return a + b;
    }
    int Add(int[] numbers)
    {
        int sum = 0;
        foreach (int number in numbers)
        {
            sum += number;
        }
        return sum;
    }
```

#### 2. Method overriding (Runtime polymorphism)

- Method overriding happens in inherited classes.
- Method in the parent class being overridden in the derived class is known as method overriding.

**Task 02**
You're building a drawing application and need to represent various shapes like circles, squares, and triangles. Each shape should have properties like color and position, and methods like draw() and calculateArea().

1. Design a class hierarchy using C#t concepts like abstraction and inheritance. Consider a base class Shape and derived classes for specific shapes.
2. Assume you are creating two new classes for circle and rectangle. Implement method overloading in the draw() method.
3. Implement method overriding in the calculateArea() method.

```cs
public abstract class Shape()
{
    public string color;
    public string position;
    public virtual void Draw()
    {
    }
    public virtual void CalculateArea()
    {
    }
}
public class Circle : Shape
{
    public override void Draw()
    {
    }
    public override void CalculateArea()
    {
        Console.WriteLine("Calculating area of the circle.");
    }
}
public class Rectangle : Shape
{
    public override void Draw()
    {
        Console.WriteLine("Drawing a rectangle...");
    }
    public override void CalculateArea()
    {
        Console.WriteLine("Calculating are of the triangle.");
    }
}
```

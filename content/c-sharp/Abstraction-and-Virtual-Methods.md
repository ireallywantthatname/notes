---
title: Abstraction and Virtual Methods
summary: "Abstract classes and virtual methods in C# for defining contracts and implementing polymorphism through method overriding"
---

```cs
public abstract class Shape
{
    public string color;
    public double[] position;
    public static string password;

    public virtual void Draw(string password)
    {
    }
    public virtual void CalculateArea(string password)
    {
    }
    protected Shape(string password)
    {
        Shape.password = password;
    }
}

public class Circle : Shape
{
    public Circle(string password) : base(password)
    {
    }
    public override void Draw(string password)
    {
        if (password == Shape.password) Console.WriteLine("Drawing a circle...");
    }
    public override void CalculateArea(string password)
    {
        if (password == Shape.password) Console.WriteLine("Calculating area of the circle.");
    }
}

public class Rectangle : Shape
{
    public Rectangle(string password) : base(password)
    {
    }
    public override void Draw(string password)
    {
        if (password == Shape.password) Console.WriteLine("Drawing a rectangle...");
    }
    public override void CalculateArea(string password)
    {
        if (password == Shape.password) Console.WriteLine("Calculating are of the triangle.");
    }
}
```

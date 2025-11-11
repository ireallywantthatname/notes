---
title: Constructors
summary: "Understanding constructors in C# including default and parameterized constructors for object initialization and state management"
---

**Task 01**

- Create an instance of the "Product" class, representing a product with an ID of 101, name "Laptop", price 800 LKR and quantity in stock 10

```cs
using System;

namespace App
{
    class Akash
    {
        public static void Main(string[] args)
        {
            Product product1 = new Product();
            product1.productID = 101;
            product1.productName = "Laptop";
            product1.price = 800.00;
            product1.quantityInStock = 10;
        }
    }
    class Product
    {
        private int productID;
        private string productName;
        private double price;
        private int quantityInStock;
        public void AddProduct(int quantity);
        public void BuyProduct(int quantity);
    }
}
```

**Task 02**

- Create a function which takes in user parameters and then display the following.

parameter1 - string name
parameter2 - int age
parameter3 - double income

display : "{name} is {age} years old. Their income is {income}."

```cs
public static void DisplayInfo(string name, int age, double income)
{
	Console.WriteLine($"{name} is {age} years old. Their income is {income}.");
}
```

#### Constructors in C\#

**Creating an object out of a class**

```cs
class_name object_name = new class_name ();
```

- Constructors are called when creating objects out of a class.

- There are two main types of constructors

  1.  Default Constructor
  2.  Parameterized Constructor

###### 1. Default Constructor

- Default constructor are created automatically. We are manually overriding the default constructor.

**Ex:**

```cs
class Vehicle {
	string model;
	int wheels;
	public Vehicle () {
		model = "AE91";
	}
}
```

###### 2. Parameterized Constructor

- Default constructors and parameterized constructors can co-exist within the same class.
- When creating an object different constructors can be used based on the scenario.

**Ex:**

```cs
class Vehicle {
	string model;
	int wheels;
	public Vehicle () {
		model = "AE91";
	}
	public Vehicle (int noWheels) {
		wheels = noWheels;
	}
}
```

- A constructor should have the _same name_ as the class.
- Constructors _do not_ have a return type.

**Task 03**
A program can store details about student details that they
have got for the 3 subjects in their exam.

1. Create a student class to store the student's name and their grades for the 3 subjects.

2. Max got 54, 65, 75 as his final marks while Amasha got 72, 49, 55. Represent the student details by using 0OP concepts.

```cs
using System;

namespace App
{
    class Akash
    {
        public static void Main(string[] args)
        {
            Student student1 = new("Max", [54, 65, 75]);
            Student student2 = new("Amasha", [72, 49, 55]);
            Console.WriteLine($"Student1: {student1.name}");
            Console.WriteLine($"Student2: {student2.name}");
        }
    }
    public class Student(string name, int[] marks)
    {
        public string name = name;
        public int[] marks = marks;
    }
}
```

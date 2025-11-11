---
title: Functions and Methods
summary: "Creating reusable code blocks in C# with function definitions, parameters, return types, and practical calculator application examples"
---

**Question**
Assume that you're building a calculator application in C#.

1. Create a function to multiply 2 numbers (user inputs).

```cs
using System;

namespace App
{
    class Akash
    {
        static int Multiply(int num1, int num2)
        {
            return num1 * num2;
        }
        public static void Main(string[] args)
        {
            Console.Write("Enter number 01: ");
            int num1 = Convert.ToInt32(Console.ReadLine());
            Console.Write("Enter number 02: ");
            int num2 = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine(Multiply(num1, num2));
        }
    }
}
```

2. If a user enters a list of values create a function which will display the sum of products.

**Method I**

```cs
using System;

namespace App
{
    class Akash
    {
        static int ArrayProduct(int[] intArray)
        {
            int product = 1;
            for (int i = 0; i < intArray.Length; i++)
            {
                product *= intArray[i];
            }
            return product;
        }
        public static void Main(string[] args)
        {
            Console.Write("Enter the number of elements: ");
            int arraySize = Convert.ToInt32(Console.ReadLine());
            int[] myArray = new int[arraySize];
            for (int i = 0; i < arraySize; i++)
            {
                Console.Write($"Enter the {i + 1} number: ");
                int num = Convert.ToInt32(Console.ReadLine());
                myArray[i] = num;
            }
            Console.WriteLine(ArrayProduct(myArray));
        }
    }
}
```

**Method II**

```cs
using System;

namespace App
{
    class Akash
    {
        static int ArrayProduct()
        {
            Console.Write("Enter integers separated by a single space: ");
            string numString = Console.ReadLine();
            string[] numbersStr = numString.Split(' ');
            int[] numbersInt = numbersStr.Select(int.Parse).ToArray();
            int product = 1;
            for (int i = 0; i < numbersInt.Length; i++)
            {
                product *= numbersInt[i];
            }
            return product;
        }
        public static void Main(string[] args)
        {
            Console.WriteLine($"Product: {ArrayProduct()}");
        }
    }
}
```

## Functions in C\#

**Syntax**

```cs
access_modifier return_type function_name (parameter1, parameter2);
```

1. **What are functions?**

- A function is a block of code that can be reused in a program.

1. **What is the difference between functions and methods?**

- Methods are usually functions defined in a class.

#### Return types in C#

- There are different types of return values (return types).

  1. all data types
  2. void (when a function does not return any value)
  3. operational return values (when a function returns a simple operation **Ex: return x \* y;** the return type should be the data type of the answer)

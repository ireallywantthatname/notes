---
title: Lab 01 Exercises
summary: "Hands-on programming exercises covering basic C# concepts including functions, arrays, and control structures"
---

![[Pasted image 20250224204132.png]]

```cs
using System;

namespace App
{

    class Akash
    {
        static double Area(double length, double width)
        {
            return length * width;
        }
        public static void Main(string[] args)
        {
           Console.WriteLine(Area(32.4, 65.3));
           Console.WriteLine(Area(32.6, 33.1));
        }
    }
}
```

![[Pasted image 20250224204148.png]]

```cs
using System;

namespace App
{
    class Akash
    {
        static void OddAndEven(double num)
        {
            Console.WriteLine(num % 2 == 0 ? "Even" : "Odd");
        }
        public static void Main(string[] args)
        {
            for (int i = 0; i < 10; i++)
            {
                Console.Write("Enter a number: ");
                double num = Convert.ToDouble(Console.ReadLine());
                OddAndEven(num);
            }
        }
    }
}
```

![[Pasted image 20250224204212.png]]

```cs
using System;

namespace App
{
    class Akash
    {
        static int Sum(int num)
        {
            if (num == 0) return 0;
            return num + Sum(num - 1);
        }
        public static void Main(string[] args)
        {
            Console.Write("Enter a number: ");
            int num = Convert.ToInt32(Console.ReadLine());
            if (num < 0)
            {
                Console.WriteLine("ERROR:");
                return;
            }
            int sum = Sum(num);
            Console.WriteLine($"Sum: {sum}");
        }
    }
}
```

![[Pasted image 20250224204229.png]]

```cs
using System;

namespace App
{
    class Akash
    {
        static int Fibb(int num)
        {
            if (num == 0) return 0;
            if (num == 1) return 1;
            return Fibb(num - 1) + Fibb(num - 2);
        }
        public static void Main(string[] args)
        {
            Console.Write("Enter a number: ");
            int num = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine(Fibb(num));
        }
    }
}
```

![[Pasted image 20250303093404.png]]

```cs
using System;

namespace App
{
    class Akash
    {
        public static void Main(string[] args)
        {
            Console.Write("Enter a number: ");
            int number = int.Parse(Console.ReadLine());
            for (int i = 0; i < 11; i++)
            {
                Console.WriteLine($"{number} * {i} = {number * i}");
            }
        }
    }
```

![[Pasted image 20250303102459.png]]

```cs
using System;

namespace App
{
    class Akash
    {
        public static void Main(string[] args)
        {
            Console.Write("Enter your name: ");
            string name = Console.ReadLine();
            Console.Write("Enter your marks: ");

            try
            {
                int marks = Convert.ToInt32(Console.ReadLine());
                char grade = ' ';

                if (marks > 100 || marks < 0)
                {
                    Console.WriteLine("Invalid marks");
                }
                else
                {
                    if (75 <= marks && marks <= 100) grade = 'A';
                    else if (60 <= marks && marks <= 74) grade = 'B';
                    else if (50 <= marks && marks <= 59) grade = 'C';
                    else if (40 <= marks && marks <= 49) grade = 'D';
                    else if (0 <= marks && marks <= 39) grade = 'F';

                    Console.WriteLine($"Name: {name}\nGrade: {grade}");
                }
            }
            catch (FormatException)
            {
                Console.WriteLine("Invalid marks");
            }
        }
    }
}
```

![[Pasted image 20250224204212.png]]

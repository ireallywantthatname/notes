---
title: Lab Recap Exercises
summary: "Review exercises covering prime number detection, arrays, loops, and comprehensive C# programming fundamentals"
---

![[Pasted image 20250324105300.png]]

```cs
namespace App
{
    class Akash
    {
        static bool Prime(int number)
        {
            if (number < 2) return false;

            for (int i = 2; i * i <= number; i++)
            {
                if (number % i == 0) return false;
            }

            return true;
        }
        static void Main(String[] args)
        {
            Console.Write("Enter a number: ");
            int number = Convert.ToInt32(Console.ReadLine());
            if (Prime(number)) Console.WriteLine("Is a prime number.");
            else Console.WriteLine("Not a prime number.");
        }
    }
}
```

![[Pasted image 20250324105342.png]]

```cs
namespace App
{
    class Akash
    {
        static int Factorial(int num)
        {
            if (num == 0 || num == 1) return 0;
            return num + Factorial(num - 1);
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
            int sum = Factorial(num);
            Console.WriteLine($"Factorial: {sum}");
        }
    }
}
```

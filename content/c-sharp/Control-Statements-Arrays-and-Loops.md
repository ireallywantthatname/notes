---
title: Control Statements Arrays and Loops
summary: "Control flow in C# with if-else statements, array declaration and manipulation, and iteration using while, for, and foreach loops"
---

## Control Statements in C\#

- If - else / If - else if - else are conditional statements that is used in C#.

**Syntax**

```cs
if (a > b) {
	\\code block; (if true)
}
else {
	\\code block; (if false)
}
```

## Arrays in C\#

Create a program to take in 5 user numerical inputs and store it inside an array. Display the array and calculate the sum of the array.

```cs
using System;

namespace App
{
    class Akash
    {
        public static void Main(string[] args)
        {
            int[] numArray = new int[5];
            for (int i = 0; i < 5; i++)
            {
                Console.Write("Enter an integer: ");
                int num = Convert.ToInt32(Console.ReadLine());
                numArray[i] = num;
            }
            for (int i = 0; i < 5; i++)
            {
                Console.Write($"{numArray[i]} ");
            }
        }
    }
}
```

## Loops in C\#

- There are 3 main loops in C#,

  1. while and do-while loop
  2. for loop
  3. for each loop

- These 3 types of loops are used depending on the scenarios in a program.

#### 1. While Loop

**Syntax**

```cs
int x = 0;
while (x == 0) {
	// this is an infinite loop --while(true)--
	Console.WriteLine("Akash");
	// while the condition is met the loop runs
}
```

#### 2. For Loop

**Syntax**

```cs
string[] animals = {"cat", "dog", "elephant"};
// for (int i = 0; i < animals.Length; i++) -- if you know the length
for (int i = 0; i < 3; i++) { // if you know the length
	Console.WriteLine(animals[i]);
}
```

#### 3. For-each Loop

**Syntax**

```cs
string[] animals = {"cat", "dog", "elephant"};
foreach(string animal in animals) {
	Console.WriteLine(animal);
}
```

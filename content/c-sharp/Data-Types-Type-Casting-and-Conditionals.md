---
title: Data Types Type Casting and Conditionals
summary: "C# fundamentals covering data types (string, int, double, char, bool), type casting with Parse and Convert methods, string concatenation, and conditional statements"
---

## Fundamentals of C\#

- C# is a case sensitive language.
- The curly bracket pairs define a code block in C#.

## Data types in C\#

- Data types identify the type of a value a variable can hold.

Ex:

```cs
string module = "Object Oriented Programming";
int age = 23;
double batch = 18.1;
char x = 'A';
bool result = true;
```

- Keywords are reserved words in C sharp.

Ex:

```cs
class
int
public
```

## Print statements and inputs in C\#

-

```cs
Console.WriteLine("Hi");
```

-

```cs
Console.ReadLine();
```

## String concatenation

- In a print statement, strings, variables and outputs of functions can be joined by using '+'.

## Type casting

- They're are 2 main methods that is used for type casting.

1. Parsing

Ex:

```cs
int age = int.Parse(Console.ReadLine());
```

2. Converting

Ex:

```cs
double amount = Convert.ToDouble(Console.ReadLine());
```

---

## Questions

1. Write a C# program to check whether the user is eligible for voting.

**Input** - User should input age and name to the program.
**Output** - User's name and the eligibility of voting.

```cs
using System;

namespace BioVarApp
{
	class Akash
	{
		public static void Main(string[] args)
		{
			Console.Write("Enter your name: ");
			string name = Convert.ToString(Console.ReadLine());
			Console.Write("Enter your age: ");
			int age = Convert.ToInt32(Console.ReadLine());
			string state = age >= 18 ? "eligible" : "not eligible";
			Console.WriteLine($"{name} you are {state}");
		}
	}
}
```

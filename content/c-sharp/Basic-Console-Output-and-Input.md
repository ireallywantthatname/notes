---
title: Basic Console Output and Input
summary: "Introduction to C# programming with Console.WriteLine, Console.ReadLine, variables, and user input examples"
---

1. Create a C# application to display your name.

```cs
namespace NameApp {

    class Akash {

        public static void Main (string[] args) {

            System.Console.WriteLine("Akash");
        }
    }
}
```

2. Create a C# program to display your name, age, degree and address.

```cs
using System;

namespace BioApp {

	class Akash {

		public static void Main (string[] args) {
			Console.WriteLine("Akash");
			Console.WriteLine("20");
			Console.WriteLine("Computer Security");
			Console.WriteLine("Kahathuduwa");

		}
	}
}
```

3. Create a program to store your name, age and last medical bill (in LKR). Use them to display a brief description about you.

```cs
using System;

namespace BioVarApp
{
	class Akash {
		public static void Main (string[] args) {
			string name = "Akash";
			int age = 20;
			double bill = 2500.00D;
			Console.WriteLine($"My name is {name} and I am {age} years old also my last medical bill cost me {bill} LKR.");

		}
	}
}
```

4. Create a C# application to take in users' response for the below questionnaire, display the answers along with the questionnaire at the end.

i. What is your name?
ii. What is your college?
iii. What is your mothers' name?
iv. Your best friends' name?

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

			Console.Write("Enter your college: ");
			string college = Convert.ToString(Console.ReadLine());

			Console.Write("Enter your mother\'s name: ");
			string motherName = Convert.ToString(Console.ReadLine());

			Console.Write("Enter your friend\'s name: ");
			string friend = Convert.ToString(Console.ReadLine());

			Console.WriteLine($"My name is {name}, I went to {college} and my mother\'s name is {motherName} and my best friend\'s name is {friend}.");
		}
	}
}
```

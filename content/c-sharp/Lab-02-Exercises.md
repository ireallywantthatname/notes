---
title: Lab 02 Exercises
summary: "Practice problems focusing on classes, objects, constructors, and object-oriented programming concepts in C#"
---

1.

```cs
using System;

namespace App
{
    class Akash
    {
        public static void Main(string[] args)
        {
            Book book_new = new("Dune", "Frank Herbert");
            Console.WriteLine(book_new.Title);
            Console.WriteLine(book_new.Author);
        }
    }
    class Book(string title, string author)
    {
        public string Title { get; } = title;
        public string Author { get; } = author;
    }
}
```

2.

```cs
using System;

namespace App
{
    class Akash
    {
        public static void Main(string[] args)
        {
            BankAccount account1 = new(80115423, 25000.25F);
            account1.Deposit(5000.25F);
            Console.WriteLine($"Account Number: {account1.AccountNumber}");
            Console.WriteLine($"Balance: {account1.Balance}");
        }
    }
    class BankAccount(int accountNumber, float balance)
    {
        public int AccountNumber { get; } = accountNumber;
        public float Balance { get; set; } = balance;
        public void Deposit(float amount)
        {
            Balance += amount;
        }
    }
}
```

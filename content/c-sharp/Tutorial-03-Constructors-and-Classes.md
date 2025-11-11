---
title: Tutorial 03 Constructors and Classes
summary: "Tutorial on constructors vs methods, designing Meeting class with setters and getters, and practical OOP implementation"
---

1. **Describe the role and purpose of constructors in C# classes. Explain the differences between a parameterized constructor and a parameterized method.**

- Constructors are a special type of method used to create objects from classes.
- The role of a constructor is to assign values to object's attributes when they are created.

| **Parameterized Method**                          | **Parameterized Constructor**                                                     |
| ------------------------------------------------- | --------------------------------------------------------------------------------- |
| A primitive data type is used as the return type. | No return type as such all constructors return an object from the selected class. |
| Can have any identifier as it's name              | The name has to be the same as the class it's defined in.                         |

2. **Design a class called Meeting to represent meetings in a diary. The Meeting class has the following fields:**

- time of the meeting represented as string in hours and minutes,
- location of the meeting (such as "room 205"),
- subject to represent the meeting's subject (such as"Examiner's meeting") - Time, location and subject are stored as strings.
  - The class should include a constructor and the following methods:
    - setTime: to set the time.
    - setlocation: to set the location.
    - setSubject: to set the subject.
    - getSubject: to return the subject of the meeting.
    - printDetails: to print all information of a meeting in the following form:
      _Meeting in room 205 at 12:30; Subject: Examiner's meeting._

```cs
namespace Diary
{
    class Meeting(string time, string location, string subject)
    {
        string Time { get; set; } = time;
        string Location { get; set; } = location;
        string Subject { get; set; } = subject;
        void PrintDetails()
        {
            Console.WriteLine($"Time: {Time}\nLocation: {Location}\nSubject: {Subject}");
        }
		static void Main (string[] args) {
			Meeting meeting1 = new ("205", "12:30", "Examiner\'s meeting");
			meeting1.PrintDetails();
		}
    }
}
```

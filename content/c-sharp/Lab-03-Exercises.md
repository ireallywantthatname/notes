---
title: Lab 03 Exercises
summary: "Advanced lab exercises on employee management systems, encapsulation, properties, and class interactions"
---

1.

```cs
using System;
namespace App
{
    public class Employee
    {
        public int EmployeeId { get; }
        public string EmployeeName { get; set; }
        public double EmployeeSalary { get; set; }

        public Employee(int employeeId, string employeeName, double employeeSalary)
        {
            EmployeeId = employeeId;
            EmployeeName = employeeName;
            EmployeeSalary = employeeSalary;
        }
        public void EmployeeData()
        {

        }
        public void DisplayEmployeeInfo()
        {

        }
    }

    public class Akash
    {
        public static void Main(string[] args)
        {
            Employee employee1 = new Employee(101, "John Doe", 50000);
            Console.WriteLine(employee1.EmployeeId);
        }
    }
}
```

2.

```cs
using System;

public class Course
{
    private string courseName;
    private string instructorName;
    private double grade;

    public Course(string courseName, double grade)
    {
        if (string.IsNullOrWhiteSpace(courseName))
            throw new ArgumentException("Course name cannot be empty.");
        if (grade < 0 || grade > 100)
            throw new ArgumentOutOfRangeException("Grade must be between 0 and 100.");

        this.courseName = courseName;
        this.grade = grade;
    }

    public string CourseName
    {
        get { return courseName; }
    }
    public string InstructorName
    {
        get { return instructorName; }
        set
        {
            if (string.IsNullOrWhiteSpace(value))
                throw new ArgumentException("Instructor name cannot be empty.");
            instructorName = value;
        }
    }
    public double Grade
    {
        get { return grade; }
    }

}

public class Akash
{
    public static void Main()
    {
        Course course1 = new Course();
    }
}
```

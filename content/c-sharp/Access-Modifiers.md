---
title: Access Modifiers
summary: "Access specifiers in C# including public, private, and protected modifiers that control visibility and accessibility of classes and members"
---

**Question**

- Compare and contrast functions and constructors.

| **Functions**                                                                     | **Constructors**                                                                                             |
| --------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| A block of code that initializes a newly created object.                          | Group of statements that can be called at any time in the program using its name to perform a specific task. |
| Has the same name as the class name.                                              | Has a different name than the class name.                                                                    |
| Has no return type not even void.                                                 | Requires a valid return type.                                                                                |
| A constructor is invoked when the when a object is created using the keyword new. | A method is invoked through method calls.                                                                    |
| Can be called multiple times.                                                     | Called only once when creating an object.                                                                    |

**Question**
What are access specifiers/modifier in C\#?

- They are keywords that define the scope, visibility and accessibility of classes and it's members.

#### 1. Public Access Modifier

- Accessibility - inside the class, derived classes, from the assembly, and different assemblies.

#### 2. Private Access Modifier

- Accessibility - only accessible within the same class.

#### 3. Protected Access Modifier

- Accessibility - accessible within the class or it's derived classes.

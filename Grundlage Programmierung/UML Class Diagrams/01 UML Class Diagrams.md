---
topic: 01 UML Class Diagrams
category: Graphical_Notation
status: completed
date_learned: 2025-02-22
tags:
  - UML
  - Class_Diagrams
  - Basics
---
---

## Table of Contents
- [[## 1. Introduction to UML Class Diagrams|1. Introduction to UML Class Diagrams]]
  - [[### 1.1 What is a UML Class Diagram?|1.1 What is a UML Class Diagram?]]
  - [[### 1.2 Purpose and Uses|1.2 Purpose and Uses]]
- [[## 2. Basic Building Blocks of a Class Diagram|2. Basic Building Blocks of a Class Diagram]]
  - [[### 2.1 Classes|2.1 Classes]]
    - [[#### 2.1.1 Class Name|2.1.1 Class Name]]
    - [[#### 2.1.2 Class Structure (Three Compartments)|2.1.2 Class Structure (Three Compartments)]]
  - [[### 2.2 Attributes (Properties, Fields)|2.2 Attributes (Properties, Fields)]]
    - [[#### 2.2.1 Access Modifiers (Public-Private-Protected)|2.2.1 Access Modifiers (Public-Private-Protected)]]
  - [[### 2.3 Operations (Methods)|2.3 Operations (Methods)]]
    - [[#### 2.3.1 Method Parameters and Return Types|2.3.1 Method Parameters and Return Types]]
    - [[#### 2.3.2 Access Modifiers in Methods|2.3.2 Access Modifiers in Methods]]

---

## 1. Introduction to UML Class Diagrams

### 1.1 What is a UML Class Diagram?
A **UML Class Diagram** is a key tool in software engineering that helps visualize and document the structure of a system. It shows the classes, their attributes and methods, and how these classes interact with each other.

Specifically a class diagram describes the structure of a system by showing its:
- Classes
- their attributes
- Operations (Methods)
- and the relationships among objects

#### What is a Class?

A class is a ==blueprint== for an object.
It describes ==**what an object will be**==, but it isn't the object itself.

![[Pasted image 20250222153251.png]]

==Classes describe the type of Object.==  - *Blueprint*

==Objects are useable instances of classes.== - *Building*

---

## 2. Basic Building Blocks of a Class Diagram

### 2.1 Classes
A **class** is the fundamental building block, representing a blueprint for objects. It is typically drawn as a rectangle split into compartments for the class name, attributes, and methods.

![[Pasted image 20250222213813.png|500]]
#### 2.1.1 Class Name
This is the identifier for the class (e.g., `Person`, `Car`, `Account`).

#### 2.1.2 Class Structure (Three Compartments)
1. **Name** (top)  
2. **Attributes** (middle)  
3. **Operations (Methods)** (bottom)

### 2.2 Attributes (Properties, Fields)
Attributes represent the data or state of a class (e.g., `name`, `age`, `balance`). They are often listed with a notation for visibility and type.

#### 2.2.1 Access Modifiers (Public-Private-Protected)
- `+` **public** - Visible to all classes and objects.
- `-` **private**  - Visible only within the same class.
- `#` **protected**  - Visible to the class itself and its subclasses.

### 2.3 Operations (Methods)
Operations define the behaviours of a class (e.g., `talk()`, `walk()`, `deposit(amount)`, `withdraw(amount)`).

#### 2.3.1 Method Parameters and Return Types
Operations can accept parameters (with types) and have a return type (e.g., `: void`, `: int`).

#### 2.3.2 Access Modifiers in Methods
Just like attributes, methods can be `public (+)`, `private (-)`, or `protected (#)`.

---
## 📚 Additional Resources

- [UML Class diagrams explained]([https://docs.python.org/3/](https://blog.algomaster.io/p/uml-class-diagram-explained-with-examples))

---
topic: 02 UML Class Diagrams
category: ""
status: in-progress
date_learned: 2025-02-22
tags:
  - Python
---
# 02 UML Class Diagrams

## Table of Contents
- [[## 3. Relationships Between Classes|3. Relationships Between Classes]]
  - [[### 3.1 Association|3.1 Association]]
    - [[#### 3.1.1 Bidirectional vs. Unidirectional|3.1.1 Bidirectional vs. Unidirectional]]
    - [[#### 3.1.2 Multiplicity (Cardinality)|3.1.2 Multiplicity (Cardinality)]]
  - [[### 3.2 Aggregation (Weak Ownership)|3.2 Aggregation (Weak Ownership)]]
  - [[### 3.3 Composition (Strong Ownership)|3.3 Composition (Strong Ownership)]]
  - [[### 3.4 Inheritance (Generalization)|3.4 Inheritance (Generalization)]]
  - [[### 3.5 Realization (Implements)|3.5 Realization (Implements)]]
  - [[### 3.6 Dependency|3.6 Dependency]]

---

## 3. Relationships Between Classes

When building UML Class Diagrams, showing how classes **interconnect** is crucial. Below are the most common relationships, each serving a different conceptual purpose in object-oriented design.

---

### 3.1 Association
An **association** indicates that two classes are connected in some way—one class needs to “know about” or communicate with the other.

#### 3.1.1 Bidirectional vs. Unidirectional
- **Unidirectional**: Only one class holds a reference to the other. For example, a `Person` class might hold a reference to a `Car`, but the `Car` class does not necessarily reference `Person`.

  **Textual UML Example**:
  ```
  Person --> Car
  ```
  This reads as: “A `Person` knows about (or references) a `Car`.”

- **Bidirectional**: Both classes reference each other. For example, a `Husband` and `Wife` might both hold references to one another.

  **Textual UML Example**:
  ```
  Husband <--> Wife
  ```
  This reads as: “`Husband` knows about `Wife`, and `Wife` knows about `Husband`.”

#### 3.1.2 Multiplicity (Cardinality)
Multiplicity describes *how many* instances of one class can be associated with a single instance of another class.

Common notations:
- `1` (exactly one)
- `0..1` (zero or one)
- `*` or `0..*` (zero to many)
- `1..*` (one to many)

**Example**:
```
Person "1" --> "0..*" Car
```
- This means “One `Person` can have zero or many `Car` objects.”

---

### 3.2 Aggregation (Weak Ownership)
Aggregation is a specialized form of association denoting a “**has-a**” relationship where one class (the “whole”) can contain multiple other classes (the “parts”), but those parts can also exist independently.

- **Key Point**: If the “whole” object is destroyed, the “parts” can still exist on their own.

**Textual UML Example**:
```
Team --(open diamond)--> Player
```
Reads:  
- `Team` **aggregates** multiple `Player` objects.  
- `Player` can still exist even if the `Team` disbands (e.g., a `Player` could join another team).

---

### 3.3 Composition (Strong Ownership)
Composition is another “**has-a**” relationship, but with strong ownership. This means the “parts” cannot exist independently of the “whole.”

- **Key Point**: If the “whole” is destroyed, the “parts” **must** be destroyed as well.

**Textual UML Example**:
```
House --(filled diamond)--> Room
```
Reads:  
- A `House` is composed of `Room` objects.  
- Without the `House`, the `Room` instances have no reason to exist; they are part of the house.

---

### 3.4 Inheritance (Generalization)
Inheritance (also called **Generalization**) indicates an “**is-a**” relationship between a more general class (the superclass) and a more specialized class (the subclass).

- The subclass (child) inherits attributes and methods from the superclass (parent).

**Textual UML Example**:
```
   Person
     ^
     |
   Student
```
Reads:  
- `Student` **is-a** `Person`.  
- `Student` inherits characteristics from `Person` but can also have additional attributes/methods (e.g., `studentId`, `enrollInCourse()`).

---

### 3.5 Realization (Implements)
Realization is used when a **class implements an interface**. The class must provide the concrete methods defined by the interface’s abstract specifications.

**Textual UML Example**:
```
   <<interface>> Drivable
         ^
         |
       Car
```
Reads:  
- `Car` **realizes** (implements) `Drivable`, meaning `Car` provides the methods promised by the interface (e.g., `startEngine()`, `stopEngine()`).

---

### 3.6 Dependency
A dependency indicates a “**uses**” relationship, where one class depends on another. If the dependent class changes, it can affect the code that uses it.

- **Loose Coupling**: Typically, a dependency is a **weaker** relationship than an association, meaning a class might just need to **call** or **reference** another class temporarily.

**Textual UML Example**:
```
Order --- (dashed arrow) ---> PaymentService
```
Reads:
- `Order` **depends** on `PaymentService`.  
- `Order` might call `paymentService.processPayment()` but doesn’t store a long-term reference to it.

---

## Additional Examples & Explanations

1. **Person and Address**  
   - If we decide that `Person` simply *knows* an `Address`, it’s usually an **association**.  
   - If we treat `Address` as strongly bound (the `Address` cannot realistically exist alone without being linked to `Person` data), we might consider **composition**. However, in many real-world designs, an address can outlive a person or can be shared with multiple people (like family members), so composition might not be correct here.  

2. **Library and Book**  
   - If a **Library** holds many **Book** objects but those books can exist on their own or belong to another library or even a personal collection, that’s **aggregation**.  
   - If, however, the design states that a **Chapter** cannot exist without the **Book**, that’s typically **composition**.  

3. **Shapes**  
   - A base class `Shape` could be **generalized** by `Circle`, `Rectangle`, etc. This is a classic example of **inheritance**.  

4. **Service and Logger**  
   - A `UserService` class might just call methods in a `Logger` utility but does not necessarily hold it as a field. That can be shown as a **dependency**—`UserService` uses `Logger` but doesn’t strongly associate or own it.

---

## Summary

- **Association**: A generic connection—classes know about each other.  
- **Aggregation**: “Has-a” relationship with **independent lifecycle**.  
- **Composition**: “Has-a” relationship with **dependent lifecycle**.  
- **Inheritance (Generalization)**: “Is-a” relationship—subclass inherits from superclass.  
- **Realization**: Class implements the operations of an interface.  
- **Dependency**: A class temporarily **uses** or **depends** on another class.

By understanding these relationships, you can more accurately represent your system’s design and communicate it to others through UML Class Diagrams.
```



## 📚 Additional Resources
- [Official Python Docs](https://docs.python.org/3/)

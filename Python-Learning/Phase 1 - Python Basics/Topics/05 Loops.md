---
topic: 05 Loops
category: Phase 1
status: completed
date_learned: 2025-02-21
tags:
  - Python
  - loops
  - while
  - for
  - nested_loops
  - head_controlled
  - tail_controlled
  - counter_controlled
  - Basics
---
- [[###What is a loop?|What is a loop?]]
- [[###Types of loops in Python|Types of loops in Python]]
  - [[####Head-controlled loops (Kopfgesteuerte Schleife)|Head-controlled loops]]
  - [[####Tail-controlled loops (Fußgesteuerte Schleife)|Tail-controlled loops]]
  - [[####Counter-controlled loops (Zählergesteuerte Schleife)|Counter-controlled loops]]
- [[###Basic for loop|Basic for loop]]
  - [[####Using range() with for loops|for and range()]]
  - [[####Looping through lists|for and lists]]
  - [[####Looping through dictionaries|for and dictionaries]]
- [[###Basic while loop|Basic while loop]]
  - [[####Using conditions in while loops|while conditions]]
  - [[####Infinite loops and how to avoid them|Avoiding infinite loops]]
- [[###Loop Control Statements|Loop control statements]]
  - [[####Using break|Using break]]
  - [[####Using continue|Using continue]]
  - [[####Using pass|Using pass]]
- [[###Nested loops|Nested loops]]
- [[###Practical examples of loops|Practical examples]]
  - [[####Building a guessing game|Guessing game example]]
  - [[####Filtering data with loops|Filtering data]]
  - [[####Reading files with loops|Reading files]]

---

### What is a loop?
A loop is a programming construct that allows executing a block of code multiple times. Loops are useful for repetitive tasks, iterating over sequences, and automating processes.

---

### Types of loops in Python

#### Head-controlled loops (Kopfgesteuerte Schleife)
These loops check the condition **before** executing the loop body.

Examples:
```python
# for loop
for i in range(3):
    print(i)

# while loop
x = 3
while x > 0:
    print(x)
    x -= 1
```

#### Tail-controlled loops (Fußgesteuerte Schleife)
Python does not have built-in tail-controlled loops (like `do-while` in other languages), but we can simulate them using `while True` with a `break` statement.

Example:
```python
while True:
    user_input = input("Enter 'yes' to continue: ")
    if user_input.lower() != "yes":
        break
    print("You entered 'yes'. Loop continues...")
```

#### Counter-controlled loops (Zählergesteuerte Schleife)
A counter-controlled loop runs for a **fixed number of times**.

Example:
```python
for i in range(5):
    print("Iteration", i)
```

---

### Basic for loop

#### Using range() with for loops
```python
for i in range(1, 6):
    print(i) # Output
```

==**Note:**==`range(1, 6)` generates numbers starting from 1 **up to but not including** 6.

#### Looping through lists
```python
numbers = [10, 20, 30]
for num in numbers:
    print(num)
```

#### Looping through dictionaries
```python
person = {"name": "Alice", "age": 25}
for key, value in person.items():
    print(f"{key}: {value}")
```

---

### Basic while loop

```python
count = 1
while count <= 5:
    print(count)
    count += 1
```

#### Using conditions in while loops
```python
x = 10
while x > 0:
    print(x)
    x -= 2
```

#### Infinite loops and how to avoid them
```python
while True:
    response = input("Type 'exit' to stop: ")
    if response == "exit":
        break
```

---

### Loop Control Statements

#### Using break
```python
for i in range(1, 10):
    if i == 5:
        break
    print(i)
```

**`break`**: Exits the loop immediately, stopping further iterations.
#### Using continue
```python
for i in range(1, 6):
    if i == 3:
        continue
    print(i)
```

**`continue`**: Skips the current iteration and moves to the next one.
#### Using pass
```python
for i in range(1, 6):
    if i == 3:
        pass
    print(i)
```

**`pass`**: Acts as a placeholder, doing nothing and allowing the loop to continue as normal.

---

### Nested loops
```python
for i in range(1, 4):
    for j in range(1, 4):
        print(f"i={i}, j={j}")
```

---

### Practical examples of loops

#### Building a guessing game
```python
import random

number_to_guess = random.randint(1, 10)
while True:
    guess = int(input("Guess a number: "))
    if guess == number_to_guess:
        print("Correct!")
        break
    print("Try again!")
```

#### Filtering data with loops
```python
numbers = [10, 15, 20, 25, 30]
even_numbers = [num for num in numbers if num % 2 == 0]
print(even_numbers)
```

#### Reading files with loops
```python
with open("example.txt", "r") as file:
    for line in file:
        print(line.strip())  # Removes extra whitespace
```


## 📚 Additional Resources
- [Official Python Docs](https://docs.python.org/3/)

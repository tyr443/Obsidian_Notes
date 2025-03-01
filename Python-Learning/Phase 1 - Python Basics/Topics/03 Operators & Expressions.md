---
topic: 03 Operators & Expressions
category: Phase 1
status: completed
date_learned: 2025-02-20
tags:
  - Python
  - Basics
  - Arithmetic_Ops
  - Comparison_Ops
  - Bitwise/Logical_Ops
  - Identity_Ops
  - Membership_Ops
---
- [[### <u>What are operators and expressions?</u>|What are operators and expressions?]]
- [[### <u>Arithmetic Operators</u>|Arithmetic Operators]]
- [[### <u>Comparison Operators</u>|Comparison Operators]]
- [[### <u>Bitwise Operators</u>|Bitwise Operators]]
- [[### <u>Identity Operators</u>|Identity Operators]]
- [[### <u>Membership Operators</u>|Membership Operators]]

### <u>What are operators and expressions?</u>

###### <u>**Operators:**</u> Special symbols that perform computations on values.

###### <u>**Expressions:**</u> Combinations of values, variables and operators that evaluate to a single value.

```python
result = 10 + 5  # Expression: 10 + 5 (evaluates to 15)
print(result)  # Output: 15
```

### <u>Arithmetic Operators</u>

| Operator | Description         |
| -------- | ------------------- |
| \+       | Addition            |
| \-       | Subtraction         |
| \*       | Multiplication      |
| \/       | Division (Float)    |
| \//      | Floor Division      |
| \%       | Modulus (Remainder) |
| \**      | Exponentiation      |

##### Example Usage:
```python
a = 10
b = 3

print(a + b)   # Output: 13
print(a - b)   # Output: 7
print(a * b)   # Output: 30
print(a / b)   # Output: 3.3333
print(a // b)  # Output: 3
print(a % b)   # Output: 1
print(a ** b)  # Output: 1000
```

### <u>Comparison Operators</u>

Comparison operators compare two values and return a Boolean (`True` or `False`).

| Operator | Description           |
|----------|----------------------|
| \==     | Equal to             |
| \!=     | Not equal to         |
| \>      | Greater than         |
| \<      | Less than            |
| \>=     | Greater than or equal to |
| \<=     | Less than or equal to   |

##### Example Usage:
```python
a = 10
b = 5

print(a == b)  # Output: False
print(a != b)  # Output: True
print(a > b)   # Output: True
print(a < b)   # Output: False
print(a >= b)  # Output: True
print(a <= b)  # Output: False
```


### <u>Bitwise Operators</u>

Bitwise operators perform operations on numbers at the **binary level** (bitwise operations). They manipulate bits directly.

| Operator | Description |
|----------|------------|
| \&      | AND - Performs bitwise AND, keeping bits that are `1` in both numbers. |
| \|      | OR - Performs bitwise OR, keeping bits that are `1` in either number. |
| \^      | XOR (Exclusive OR) - Keeps bits that are `1` in only one of the numbers. |
| \~      | NOT (Bitwise Inversion) - Flips all bits (negative representation in Python). |
| \<<     | Left Shift - Moves bits **left**, effectively multiplying by 2 for each shift. |
| \>>     | Right Shift - Moves bits **right**, effectively dividing by 2 for each shift. |

##### Example Usage
```python
a = 5  # Binary: 101
b = 3  # Binary: 011

print(a & b)   # Output: 1   (Binary: 001)
print(a | b)   # Output: 7   (Binary: 111)
print(a ^ b)   # Output: 6   (Binary: 110)
print(~a)      # Output: -6  (Binary: ...11111010)
print(a << 1)  # Output: 10  (Binary: 1010)
print(a >> 1)  # Output: 2   (Binary: 010)
```

### <u>Identity Operators</u>

Identity operators are used to compare the **memory locations** of two objects to determine if they refer to the same object.

| Operator | Description |
|----------|------------|
| `is`     | Returns `True` if both variables refer to the same object in memory. |
| `is not` | Returns `True` if both variables do **not** refer to the same object in memory. |

##### Example Usage
```python
a = [1, 2, 3]
b = [1, 2, 3]
c = a  # c now refers to the same object as a

print(a is c)   # Output: True (Same object)
print(a is b)   # Output: False (Different objects)
print(a is not b) # Output: True
```

### <u>Membership Operators</u>

Membership operators are used to check whether a value is present in a **sequence** (e.g., lists, tuples, sets, strings).

| Operator | Description |
|----------|------------|
| `in`     | Returns `True` if the specified value exists in the given sequence. |
| `not in` | Returns `True` if the specified value does **not** exist in the given sequence. |

##### Example Usage
```python
numbers = [1, 2, 3, 4, 5]
word = "Python"

print(3 in numbers)    # Output: True (3 exists in the list)
print(10 in numbers)   # Output: False (10 is not in the list)
print("y" in word)     # Output: True ("y" is in "Python")
print("z" not in word) # Output: True ("z" is not in "Python")
```



## 📚 Additional Resources
- [Official Python Docs](https://docs.python.org/3/)

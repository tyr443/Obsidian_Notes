---
topic: 02 Variables & Data Types
category: Phase 1
status: completed
date_learned: 2025-02-19
tags:
  - Python
  - Basics
  - Variables
  - Data_Types
  - Type_Checking
  - Type_Conversion
---

- [[### Assigning variables|Assigning Variable]]
- [[### Datatypes|Datatypes]]
  - [[##### 1. Integers (int) - Whole numbers|int]]
  - [[##### 2. Floating-Point Numbers (float) - Numbers with a decimal point|float]]
  - [[##### 3. Complex Numbers (complex) - Numbers with a real and imaginary part|complex]]
  - [[##### 1. Boolean (True *or* False) - Internally stored as 1 or 0|boolean]]
  - [[##### 1. Strings can be enclosed with " " or ' ' |string]]
  - [[##### 1. Lists - Ordered mutable collections|list]]
  - [[##### 2. Tuples - Ordered immutable collections|tuples]]
  - [[##### 3. Ranges - Generates a sequence of numbers|range]]
  - [[##### 1. Sets - Unordered unique elements|set]]
  - [[##### 2. Frozen Sets - Immutable set (Cannot add or remove elements)|frozenset]]
  - [[##### 1. Dictionaries - Key-value pairs|dict]]
  - [[##### 1. None - Represents the absence of a value|None]]
- [[#### <u> Type Checking and Conversion</u>| Type Checking and Conversion]]

### Assigning variables

**Variable:** A location in memory with a name or handle.
**Datatype:** The form of value associated with the variable e.g. *int, string, float, double, char, etc.*

Python is ==dynamically types==, meaning type of variable is determined at runtime based on the value assigned to it.

*note: this means you can reassign a variable with a datatype :*

```python
age = 5 
age = "Five"
```


### Datatypes

#### <u>Numeric types</u>

##### 1. Integers (int) - Whole numbers

```python
age = 35 # The age variable will be determined as a int.
print(type(age)) # Output: int
```

##### 2. Floating-Point Numbers (float) - Numbers with a decimal point

```python
pi = 3.14159 # This will be determined as a float
print(type(pi)) # Output: float
```

**Python does not have a specific "double" data type** like some other programming languages. Instead it's float uses double precision, essentially making it equivalent to a double in Java.

##### 3. Complex Numbers (complex) - Numbers with a real and imaginary part

```python
c = 3 + 4j
print(type(c)) # Output: complex
```

#### <u>Boolean Type</u>

##### 1. Boolean (True *or* False) - Internally stored as 1 or 0

```python
is_alive = True

print(type(is_alive)) # Output: bool
```

#### <u>String Type</u>

##### 1. Strings can be enclosed with " " or ' ' 

```python
first_Name = 'John'
last_Name = "Smith"

print(type(first_Name)) # Output: str

```

###### - Strings support indexing

```python

country = "Germany"

print(country[0]) # Output: G

```

#### <u>Sequence Types</u>

##### 1. Lists - Ordered mutable collections

```python
numbers = [1, 2, 3, 4, 5]
print(type(numbers)) # Output: list
numbers.append(6) # List now has 6 on the end.
```

##### 2. Tuples - Ordered immutable collections

```python
num_Set = (10, 20)
print(type(num_set)) # Output: tuple
```

##### 3. Ranges - Generates a sequence of numbers

```python
num_Range = range(5)
print(list(num_Range)) # Output: 1, 2, 3, 4, 5
```

#### <u>Set Types</u>

##### 1. Sets - Unordered unique elements

```python
nums = {1, 1, 2, 3, 3, 3, 4}
print(nums)
```

##### 2. Frozen Sets - Immutable set (Cannot add or remove elements)

```python
frozen_Set = ([1, 2, 3])

print(frozen_Set) # 
```

#### <u>Mapping Types</u>

##### 1. Dictionaries - Key-value pairs

```python
student = {
"name": "Tom"
"age": 20
}

print(student) #{'name': 'Tom', 'age': 20}
print(["name"]) # Tom

```

#### <u>None Type</u>

##### 1. None - Represents the absence of a value

###### Used as a placeholder:

```python
result = None # Placeholder
# Some logic later
result = 42
print(result) # Output: 42
```

##### "No Result" or "Nothing found"

```python
def find_user(username):
    users = {"Jane": 1, "Jane": 2}
    return users.get(username)  # Returns None if username is not found

user_id = find_user("Charlie")
print(user_id)  # Output: None

```
##### Resetting a Variable

```python
user_input = "Yes"
print(user_input)  # Output: Yes

# Reset the variable
user_input = None
print(user_input)  # Output: None
```

#### <u> Type Checking and Conversion</u>

Check variable type:

```python
x = 5
print(type(x))  # Output: <class 'int'>
```

Convert between variables using:

```python
int("10")  # String to integer
float(5)  # Integer to float
str(3.14)  # Float to string
list((1, 2, 3))  # Tuple to list
```

## 📚 Additional Resources
- [Official Python Docs](https://docs.python.org/3/)
 
---
topic: "06 Functions & Scope"
category: ""
status: "in-progress"
date_learned: "2025-02-22"
tags: ["Python"]
---

- [[###What is a Function?|What is a Function?]]
- [[###Defining Functions|Defining Functions]]
  - [[#### Parameters & Arguments|Parameters & Arguments]]
    - [[##### Keyword vs Positional Arguments|Keyword vs Positional Arguments]]
  - [[#### Return Values|Return Values]]
- [[###Calling Functions|Calling Functions]]
- [[###Scope in Python|Scope in Python]]
  - [[#### Local Scope|Local Scope]]
  - [[#### Global Scope|Global Scope]]
  - [[#### Nonlocal Keyword|Nonlocal Keyword]]
- [[###Lambda Functions|Lambda Functions]]

---

### What is a Function?
A **function** is a reusable block of code that performs a specific task. Functions help break programs into smaller, modular pieces that are easier to understand and maintain. They can accept inputs (parameters) and optionally return an output.

**Example:**
```python
def greet():
    print("Hello, world!")

greet()  # This calls the function and prints "Hello, world!"
```

### Defining Functions
In Python, functions are defined using the `def` keyword followed by the function name and a set of parentheses. Inside the parentheses, you can specify parameters. The function’s code block is indented.

**Example:**
```python
def add(a, b):
    return a + b

result = add(3, 5)
print(result)  # This will print 8
```

#### Parameters & Arguments
- **Parameters** are the variables listed in the function definition.
- **Arguments** are the actual values you pass to the function when calling it.

**Example:**
```python
def multiply(x, y):
    return x * y

# Here, 4 and 5 are arguments corresponding to the parameters x and y.
product = multiply(4, 5)
print(product)  # Prints 20
```

##### Keyword vs Positional Arguments
- **Positional arguments** (nonkeyword arguments) are passed to a function based solely on their order.
- **Keyword arguments** are passed by explicitly naming each parameter, which can improve readability and allow you to pass them in any order.

**Example:**
```python
def introduce(name, age):
    print(f"My name is {name} and I am {age} years old.")

# Using positional arguments:
introduce("Alice", 30)  # "Alice" is assigned to name, 30 to age

# Using keyword arguments:
introduce(age=30, name="Alice")  # Order doesn't matter when using keywords
```

#### Return Values
Functions can return a value using the `return` statement. If no `return` statement is used, the function returns `None` by default.

**Example:**
```python
def subtract(a, b):
    return a - b

difference = subtract(10, 3)
print(difference)  # Prints 7
```

### Calling Functions
Calling a function means executing the code within it. This is done by writing the function’s name followed by parentheses. If the function requires arguments, pass them inside the parentheses.

**Example:**
```python
def greet(name):
    return f"Hello, {name}!"

message = greet("Alice")
print(message)  # Prints "Hello, Alice!"
```

### Scope in Python
**Scope** determines the accessibility of variables in different parts of your code. Python has different scopes, primarily **local** and **global**. The `nonlocal` keyword is used in nested functions to work with variables from an enclosing scope (but not the global scope).

#### Local Scope
Variables defined inside a function are local to that function and cannot be accessed outside it.

**Example:**
```python
def my_function():
    local_var = "I'm local"
    print(local_var)

my_function()
# Uncommenting the line below will cause an error because local_var is not accessible outside the function.
# print(local_var)
```

#### Global Scope
Variables defined outside any function are in the global scope and can be accessed anywhere in the module.

**Example:**
```python
global_var = "I'm global"

def show_global():
    print(global_var)

show_global()      # This will print "I'm global"
print(global_var)  # This also prints "I'm global"
```

#### Nonlocal Keyword
When dealing with nested functions, the `nonlocal` keyword allows you to modify a variable defined in an outer (but not global) scope.

**Example:**
```python
def outer_function():
    count = 0
    def inner_function():
        nonlocal count  # This tells Python to use the 'count' from the outer function
        count += 1
        print("Inner count:", count)
    inner_function()
    print("Outer count:", count)

outer_function()
```

### Lambda Functions
Lambda functions are small, anonymous functions defined with the `lambda` keyword. They are useful for short, simple operations where a full function definition would be unnecessarily verbose.

**Example:**
```python
# A lambda function that squares a number
square = lambda x: x * x
print(square(5))  # Prints 25
```

## 📚 Additional Resources
- [Official Python Docs](https://docs.python.org/3/)

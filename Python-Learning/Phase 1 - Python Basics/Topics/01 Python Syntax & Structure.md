---
topic: 01 Python Syntax & Structure
category: Phase 1
status: completed
date_learned: 2025-02-16
tags:
  - Python
  - Basics
  - Indentation
  - Best_Practices
  - Commenting
  - Libraries
  - Syntax
---

- [[## 📝 Running Python Scripts|Downloading & Running Python]]
- [[## ⚙️Python Versions|Version control]]
  - [[#### Reasons for version specific requirements|Why?]]
  - [[#### Running Python Scripts]]
- [[##📚Libraries|Libraries]]
  - [[#Importing Libraries|Importing Libraries]]
- [[## 💬Commenting in Python|Commenting]]
  - [[#### Inline comments]]
  - [[#### Multi-line comments]]
  - [[#### Docstrings ]]
- [[## 📜Python Syntax Rules|Syntax]]
  - [[#### Case Sensitivity]]
  - [[#### Indentation & Whitespace]]
  - [[#### Line Termination]]
  - [[#### Naming conventions]]
  - [[#### Strings]]
  - [[#### Colon (:) Usage]]
  - [[#### Exception Handling]]

### 📝 Running Python Scripts

**Requirements**

1. Download Python before any scripts can be run: [python.org](www.python.org)

2. Download an IDE (Integrated Development Environment) e.g. VSCode or PyCharm

3. Python files use the extension **.py**

A Python script runs in straightforward linear fashion, anything written in the script is executed when it is run, *with the exception of conditionally executed code such as functions or classes*.

``` py
print("Hello, World!")
```

This is a valid Python code.

### ⚙️Python Versions

Python aims to maintain backwards compatibility within the same major versions e.g. Python 3.x.
*However it is not guaranteed some libraries may be inaccessible in newer versions or changes in the same major version*

#### Reasons for version specific requirements

* ***Depreciation of Features***: Things are removed or changed between versions.

* ***Changes in Libraries or Syntax***: Python libraries can also be updated and a specific library could be dependant on a feature from an older version of Python.

* ***Bug Fixes and Optimizations***: Changes that can cause things to be moved within a version of Python.

#### Running Python Scripts

in command line:

```
python script.py
```

or with python 3

```
python3 script.py
```


==**note**: script.py is the name of the script.==
### 📚Libraries

Library: Prewritten collections of code that contain functions, classes and modules for performing tasks.

| Library  | Usage             |
| -------- | ----------------- |
| pandas   | Working with data |
| requests | Handling requests |
| Flask    | Web applications  |
| Django   | Web applications  |

### Importing Libraries

``` python
import pandas as pd
```

+ *pandas*: is the name of the library being imported
+ *pd*: is the alias

#### Calling with the library:
```
pandas.DataFrame
```
#### Calling with the alias:
```
pd.DataFrame
```
#### Selective import
``` python
from pandas import DataFrame, Series
```

This would import only specific parts of the pandas library, making code shorter.

### 💬Commenting in Python

#### Inline comments

``` python
# This is a sing line comment
print("Hello, World!") # This is a print statement
```

#### Multi-line comments

``` python
#This
#greets
#people
print("Hello, World!")
```
#### Docstrings 
For multi-line comments for document explanations "Docstrings" are used """ or ''' surrounding the comment.

``` python
def greet():

"""
This is a
print function
"""

print("Hello, World!")

```

### 📜Python Syntax Rules

#### Case Sensitivity

**Rule**: Python is case sensitive

```python

num = 10
Num = 33
print(num) #Output: 10
print(Num) #Output: 33 

```

#### Indentation & Whitespace

**Rule:** Indentation defines code blocks in Python.

```python

if True:
	print("This is part of the if block")
print("This is outside of the if block")

```

==*Don't mix tabs with spaces*==
#### Line Termination

**Rule:** New lines end statements

```python

a = 1 #New line new variable
b = 2
# Or (uncommon)
c = 3; d = 4 
#Instead of new line, semi-colon termination

```
#### Naming conventions

**Rule:** Variable names must start with a letter or underscore. 
==Cannot start with numbers or contain hyphens.==

```python

valid_name = "Hi"
_validName = "World"
# invalid-name = "!"
# 2invalidName = 1

```

#### Strings

**Rule:** Strings can be defined using:

+ Single quotes:
```python
string1 = 'Hello, World!'
```

+ Double quotes
```python
string2 = "Hello, World!"
```

+ Triple quotes (multi-line string)
```python
string3 = """Hello,
...
...
World"""
```
#### Colon (:) Usage

**Rule:** A colon is used to start an indented block following a statement.

```python
if a > 5:
	print("a is greater than 5")
```

#### Exception Handling

**Rule:** *try* and *except* blocks handle exceptions

```python
try:
	result = 10/0
except ZeroDivisionError:
	print("Cannot divide by zero")
```

[Python docs - Exception Handling](https://docs.python.org/3/tutorial/errors.html)


## 📚 Additional Resources
- [Official Python Docs](https://docs.python.org/3/)

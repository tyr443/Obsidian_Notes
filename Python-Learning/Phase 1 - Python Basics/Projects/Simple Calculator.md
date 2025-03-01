 
# 🖩 Python Project: Simple CLI Calculator

## 🎯 **Project Goal**
Create a **command-line calculator** in Python that allows users to perform basic arithmetic operations and continues running until they choose to exit.

## 📌 **Features & Requirements**

### 1️⃣ **Basic Functionality**
- Perform **addition +, subtraction -, multiplication \*, and division /**.
- Ask the user for two numbers and an operation.
- Display the result.
- Ask the user if they want to **perform another calculation or exit**.

### 2️⃣ **Control Flow & Error Handling**
- Use a **loop** to allow continuous calculations until the user exits.
- Use **match case or if/elif** to determine which operation to perform.
- Handle **invalid inputs** (letters instead of numbers).
- Prevent **division by zero**.

### 3️⃣ **Example Interaction**
```
Welcome to the Simple Calculator!
Enter first number: 5
Enter second number: 2
Choose operation: (+, -, *, /)
> *
Result: 10
Do you want to calculate again? (yes/no)
> yes

Enter first number: 8
Enter second number: 0
Choose operation: (/)
> /
Error: Division by zero is not allowed!
Do you want to calculate again? (yes/no)
> no

Goodbye!
```

## 🏗 **Suggested Steps to Implement**

### 1️⃣ **Define Functions**
- `add(a, b)`, `subtract(a, b)`, `multiply(a, b)`, `divide(a, b)`
- A function to handle **user input validation**
- A function for the **main loop**

### 2️⃣ **Implement Control Flow**
- Use a **while loop** to allow multiple calculations.
- Use **match case or if/elif** to choose the operation.
- Implement **error handling** for invalid input and division by zero.

## 🌟 **Bonus Challenges (Optional)**
- **Memory Feature**: Store the last result and allow the user to use it.
- **Exponentiation**: Allow calculations like `2^3 = 8`.
- **Square Root Function**.
- **GUI Version**: Implement with Tkinter later.


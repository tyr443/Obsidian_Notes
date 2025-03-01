 
## 🎯 **Project Goal**
Create a **command-line unit converter** in Python that allows users to convert between different units of measurement and continues running until they choose to exit.

## 📌 **Features & Requirements**

### 1️⃣ **Basic Functionality**
- Convert between **length (meters, kilometers, miles, feet)**.
- Convert between **weight (grams, kilograms, pounds, ounces)**.
- Convert between **temperature (Celsius, Fahrenheit, Kelvin)**.
- Ask the user for a value, the original unit, and the target unit.
- Display the converted result.
- Ask the user if they want to **perform another conversion or exit**.

### 2️⃣ **Control Flow & Error Handling**
- Use a **loop** to allow continuous conversions until the user exits.
- Use **match case or if/elif** to determine the correct conversion formula.
- Handle **invalid inputs** (non-numeric values, unsupported units).

### 3️⃣ **Example Interaction**
```
Welcome to the Unit Converter!
Enter value: 100
Enter original unit (m, km, mi, ft): m
Enter target unit (m, km, mi, ft): km
Converted result: 0.1 km
Do you want to convert another value? (yes/no)
> yes

Enter value: 32
Enter original unit (C, F, K): C
Enter target unit (F, K): F
Converted result: 89.6°F
Do you want to convert another value? (yes/no)
> no

Goodbye!
```

## 🏗 **Suggested Steps to Implement**

### 1️⃣ **Define Functions**
- Functions for conversion: `convert_length()`, `convert_weight()`, `convert_temperature()`
- A function to handle **user input validation**
- A function for the **main loop**

### 2️⃣ **Implement Control Flow**
- Use a **while loop** to allow multiple conversions.
- Use **match case or if/elif** to choose the correct conversion function.
- Implement **error handling** for invalid input.

## 🌟 **Bonus Challenges (Optional)**
- **Expand to More Units**: Add speed (km/h, mph), volume (liters, gallons), etc.
- **Memory Feature**: Store the last conversion and allow the user to reuse it.
- **GUI Version**: Implement with Tkinter later.


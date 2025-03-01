---
topic: 04 Control Flow
category: Phase 1
status: completed
date_learned: 2025-02-21
tags:
  - Python
  - if_statement
  - elif_statement
  - else_statement
  - and
  - or
  - not
  - match_case
  - if_nested
---

- [[### <u>*if* Statement (Condition checking)</u>|if (Condition checking)]]
- [[### <u>*if-else* Statement (Two-way decision making)</u>|if-else (Two-way decision making)]]
- [[### <u>*if-elif-else* Statement (Multiple conditions)</u>|if-elif-else (Multiple conditions)]]
- [[### <u>Nested *if* Statements (Multi-layer conditions)</u>|Nested if (Multi-layer conditions)]]
- [[### <u>*if* with Boolean Variables (Simplified conditions)</u>|if with Boolean Variables (Simplified conditions)]]
- [[### <u>*if* with logical operators</u>|if with logical operators]]
  - [[##### <u>*if-and* (Both conditions must be true)</u>|if-and (Both conditions must be true)]]
  - [[##### <u>*if-or*(At least one condition must be true)</u>|if-or (At least one condition must be true)]]
  - [[##### <u>*if-not* (Negating a condition)</u>|if-not (Negating a condition)]]
- [[### <u>Ternary operators (Assigning conditions with *if* )</u>|Ternary operators (Assigning conditions with if )]]
- [[### <u>*match* Statement (Pattern matching)</u>|match (Pattern matching)]]
  - [[##### <u>*match* multiple statements</u>|match multiple statements]]
  - [[##### <u>*match* Tuples</u>|match Tuples]]


### <u>*if* Statement (Condition checking)</u>

```python
temperature = 30

if temperature >= 25
print("It's a hot day.")
```

*if* the temperature is 25 or above the statement will be evaluated as ==**true**== and print "It's a hot day".

*if* the temperature is below 25 the statement will be evaluated as ==**false**== and skipped.

### <u>*if-else* Statement (Two-way decision making)</u>
```python
temperature = 20

if temperature >= 25:
	print("It's a hot day")
else:
	print("It's not too hot today")
```

`if` the temperature is 25 or above the statement will  be evaluated as `True` and print "It's a hot day"

`else` it will print "It's not too hot today" in all other cases.

### <u>*if-elif-else* Statement (Multiple conditions)</u>
```python
temperature = 25

if temperature >= 25:
	print("It's a hot day.")
elif temperature > 15:
	print("It's a warm day.")
else:
	print("It's a cold day.")
```

*if* the temperature is 25 or above the statement will  be evaluated as ==**true**== and print "It's a hot day"

*elif* - else if the temperature is more than 15 but less than 25 the statement will be evaluated as ==**true**== and print "It's a warm day"

==**else**== it will print "It's a cold day" in all other cases.

### <u>Nested *if* Statements (Multi-layer conditions)</u>

```python
temperature = 30
humidity = 80

if temperature >= 25:
	print("It's a hot day")
	if humidity > 75:
		print("It's also very humid.")
		
```

*if* the temperature is 25 or above the statement will  be evaluated as ==**true**== and print "It's a hot day" and it will begin to evaluate the inner statement. 
*if* humidity is more than 75 then it will also print "It's also very humid."

==**NOTE:** It will enter the nested statement if the first statement is evaluated as true.==

### <u>*if* with Boolean Variables (Simplified conditions)</u>

```python
is_Sunny = True

if is_Sunny:
	print("It's a sunny day!")
else:
	print("It's cloudy.")

```

Instead of explicitly comparing values, we can use boolean variables directly.

### <u>*if* with logical operators</u>

==**NOTE:**  The logical operation functions below evaluate two variables directly, [[03 Operators & Expressions#<u>Bitwise Operators</u>|the other functions]] evaluate the bits (Binary).==

##### <u>*if-and* (Both conditions must be true)</u>

```python
temperature = 30
humidity = 85

if temperature > 25 and humidity > 80:
	print("It's hot and humid.")
```


##### <u>*if-or*(At least one condition must be true)</u>

```python
temperature = 30
wind_speed = 10

if temperature > 25 or wind_speed > 20:
    print("Weather is either hot or windy.")
```



##### <u>*if-not* (Negating a condition)</u>

```python
raining = False

if not raining:
    print("No need for an umbrella!")

```


### <u>Ternary operators (Assigning conditions with *if* )</u>

```python
temperature = 22
weather = "Hot" if temperature > 25 else "Cool"
print(weather)
```

### <u>*match* Statement (Pattern matching)</u>

```python
status_code = 404

match status_code:
    case 200:
        print("OK: Request was successful.")
    case 404:
        print("Error: Not Found.")
    case 500:
        print("Server Error.")
    case _:
        print("Unknown Status Code.")

```

Evaluates a variable comparatively based on cases, each case having its own output.

##### <u>*match* multiple statements</u>

```python
http_status = 201

match http_status:
    case 200 | 201 | 202:
        print("Success.")
    case 400 | 401 | 403:
        print("Client Error.")
    case 500 | 503:
        print("Server Error.")
    case _:
        print("Unknown Status.")
```


##### <u>*match* Tuples</u>

```python
point = (0, 5)

match point:
    case (0, 0):
        print("Origin")
    case (0, y):
        print(f"On the Y-axis at y={y}")
    case (x, 0):
        print(f"On the X-axis at x={x}")
    case (x, y):
        print(f"Point at ({x}, {y})")

```

## 📚 Additional Resources
- [Official Python Docs](https://docs.python.org/3/)

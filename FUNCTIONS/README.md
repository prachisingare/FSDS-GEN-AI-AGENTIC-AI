
# 📘 Python Functions and Function Arguments

This repository provides a comprehensive overview of **functions in Python**, along with detailed explanations and examples of **function arguments**, including default, keyword, variable-length, and more.

---

## 🔹 What is a Function?

A **function** is a reusable block of code that performs a specific task. Functions help reduce repetition, improve code clarity, and make programs more modular and easier to manage.

### ✅ Why Use Functions?
- **Reusability**
- **Modularity**
- **Maintainability**
- **Improved Readability**

---

## 🔹 Defining a Function

```python
def function_name(parameters):
    # body of the function
    return result  # optional
```

### 🧪 Example

```python
def greet():
    print("Hello!")
    print("Good Morning")

greet()
```

---

## 🔹 Function with Arguments

```python
def add(x, y):
    result = x + y
    return result

print(add(3, 4))
```

---

## 🔹 Types of Function Arguments

### 1. **Positional Arguments**

```python
def person(name, age):
    print(name, age)

person("Alice", 25)
```

### 2. **Keyword Arguments**

```python
person(age=25, name="Alice")
```

### 3. **Default Arguments**

```python
def person(name, age=18):
    print(name, age)

person("Bob")
```

### 4. **Variable-Length Positional Arguments (*args)**

```python
def total(*numbers):
    print(sum(numbers))

total(1, 2, 3, 4)
```

### 5. **Variable-Length Keyword Arguments (**kwargs)**

```python
def details(**info):
    print(info)

details(name="Alice", age=25, city="Pune")
```

---

## 🔹 Returning Multiple Values

```python
def calc(a, b):
    return a + b, a - b, a * b

x, y, z = calc(5, 2)
```

---

## 🔹 Local vs Global Variables

```python
x = 10

def show():
    x = 5
    print("Inside:", x)

show()
print("Outside:", x)
```

```python
x = 10

def update():
    global x
    x += 5

update()
print(x)  # Output: 15
```

---

## 🔹 Type Hinting

```python
def even_or_odd(x: int) -> str:
    return "Even" if x % 2 == 0 else "Odd"
```

---

## ✅ Summary

| Type                  | Example                              | Description                          |
|-----------------------|--------------------------------------|--------------------------------------|
| Positional Args       | `func(1, 2)`                         | Based on position                    |
| Keyword Args          | `func(x=1, y=2)`                     | Based on parameter names             |
| Default Args          | `def f(x=0)`                         | Defaults if no value is passed       |
| Variable-Length Args  | `*args`                              | Multiple positional arguments        |
| Variable Keyword Args | `**kwargs`                           | Multiple keyword arguments           |
| Return Multiple       | `return x, y`                        | Returns a tuple                      |
| Global Keyword        | `global var_name`                    | Access/modify global variables       |

| Type              | Syntax Example             | Notes                                |
| ----------------- | -------------------------- | ------------------------------------ |
| Basic Function    | `def greet():`             | No input, no return                  |
| With Arguments    | `def add(x, y):`           | Requires positional arguments        |
| Default Arguments | `def greet(name='Guest'):` | Provides fallback if no value given  |
| `*args`           | `def sum(*nums):`          | Accepts variable number of arguments |
| `**kwargs`        | `def person(**info):`      | Accepts variable keyword arguments   |
| Return Values     | `return x, y`              | Can return multiple values           |
| Global vs Local   | `global x`                 | Global used to access outer variable |






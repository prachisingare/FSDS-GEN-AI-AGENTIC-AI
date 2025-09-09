
# Exception Handling in Python

## 📌 Introduction

Exception handling in Python allows developers to manage runtime errors
gracefully without abruptly stopping the execution of a program. Instead
of crashing, programs can catch exceptions, display meaningful error
messages, and continue execution.

---

## ⚡ Why Use Exception Handling?

- Prevents unexpected program crashes.\
- Provides user-friendly error messages.\
- Ensures resources (files, databases, etc.) are properly closed.\
- Improves program reliability and debugging.

---

## 🔑 Basic Syntax

```python
try:
    # Code that might cause an exception
    risky_operation()
except ExceptionType:
    # Code to handle the exception
    handle_error()
else:
    # Executes if no exception occurs
    success_block()
finally:
    # Executes no matter what (optional)
    cleanup_block()
```

---

## 📝 Examples

### 1. Division without error

```python
a = 5
b = 2
print(a / b)   # Output: 2.5
print("bye")
```

### 2. Division by zero (without handling)

```python
c = 5
d = 0
print(c / d)   # ZeroDivisionError
```

### 3. Handling ZeroDivisionError

```python
c = 3
d = 0

try:
    print(c / d)
except Exception as e:
    print("You cannot divide number by zero:", e)

print("bye")
```

✅ Output:

    You cannot divide number by zero: division by zero
    bye

---

## 🎯 Handling Multiple Exceptions

```python
try:
    n = 0
    res = 100 / n
except ZeroDivisionError:
    print("You can't divide by zero!")
except ValueError:
    print("Enter a valid number!")
else:
    print("Result is", res)
finally:
    print("Execution complete.")
```

✅ Output:

    You can't divide by zero!
    Execution complete.

---

## 🛠️ Key Points

- **try block** → Code that might cause an error.\
- **except block** → Handles the error gracefully.\
- **else block** → Runs only if no exception occurs.\
- **finally block** → Always runs (used for cleanup).\
- Use `Exception as e` to capture the actual error message.

---

## 📚 Conclusion

Exception handling is a powerful mechanism in Python that ensures smooth
execution even when errors occur. By using `try-except-else-finally`,
developers can create robust and user-friendly applications.

# 5. Debugging

## 5.1 Types of Errors

Errors in Python can be categorized into different types based on when and why they occur:

### 1. **Syntax Error**
   Occurs when the code is not written in accordance with the rules of Python syntax. The interpreter cannot understand it.
   ```python
   # Example: Missing closing parenthesis
   print("Hello, World!"  # This will raise a SyntaxError
   ```

### 2. **Indentation Error**
   Happens when the indentation of the code blocks is not consistent. Python relies on indentation to define the structure of the code.
   ```python
   # Example: Incorrect indentation
   def my_function():
   print("Hello, World!")  # This will raise an IndentationError
   ```

### 3. **Name Error**
   Occurs when the code refers to a variable or function that is not defined or is out of scope.
   ```python
   # Example: Using an undefined variable
   print(x)  # This will raise a NameError if 'x' has not been defined
   ```

### 4. **Type Error**
   Happens when an operation or function is applied to an object of inappropriate type.
   ```python
   # Example: Trying to add an integer to a string
   x = "Hello"
   y = 5
   print(x + y)  # This will raise a TypeError
   ```

### 5. **Value Error**
   Raised when a built-in operation or function receives an argument that has the right type but an inappropriate value.
   ```python
   # Example: Converting a string that cannot be converted to an integer
   num = int("Hello")  # This will raise a ValueError
   ```

### 6. **Index Error**
   Occurs when trying to access an element from a list or tuple using an index that is out of range.
   ```python
   # Example: Accessing an index that doesn't exist
   my_list = [1, 2, 3]
   print(my_list[5])  # This will raise an IndexError
   ```

### 7. **Key Error**
   Happens when trying to access a dictionary with a key that does not exist.
   ```python
   # Example: Accessing a non-existent key
   my_dict = {'a': 1, 'b': 2}
   print(my_dict['c'])  # This will raise a KeyError
   ```

### 8. **Attribute Error**
   Occurs when an invalid attribute reference is made. This can happen when trying to access an attribute that an object does not possess.
   ```python
   # Example: Accessing a non-existent method
   my_list = [1, 2, 3]
   my_list.add(4)  # This will raise an AttributeError
   ```

### 9. **ZeroDivisionError**
   Raised when attempting to divide by zero.
   ```python
   # Example: Division by zero
   x = 10
   y = 0
   print(x / y)  # This will raise a ZeroDivisionError
   ```

### 10. **File Not Found Error**
   Occurs when trying to open a file that does not exist.
   ```python
   # Example: Attempting to read a non-existent file
   with open("non_existent_file.txt") as f:
       content = f.read()  # This will raise a FileNotFoundError
   ```

---

## 5.2 Locating and Resolving Errors

To identify and troubleshoot errors, follow these steps:

- **Read error messages carefully**: Python usually provides helpful error messages indicating the type and location of the error.
- **Check the stack trace**: The stack trace (the traceback message) shows where the error occurred, which is useful for debugging.
- **Use a step-by-step approach**: Isolate parts of the code and test them independently to narrow down the problem.
- **Check for common mistakes**: Misspellings, incorrect indentation, and improper variable usage are frequent sources of errors.

---

## 5.3 Introduction to Exception Handling

Python provides an `exception handling` mechanism to catch and handle errors gracefully without crashing the program. This involves using the `try`, `except`, `else`, and `finally` blocks.

| Block      | Description                                                                                       |
|------------|---------------------------------------------------------------------------------------------------|
| **try**    | Contains the code that may raise an exception.                                                    |
| **except** | Contains the code to handle the exception if one occurs.                                          |
| **else**   | Contains code that runs only if no exception occurs in the `try` block.                           |
| **finally**| Contains code that will run regardless of whether an exception was raised or not. Often used for cleanup. |

### Example:

```python
try:
    x = 10 / 0  # This will raise a ZeroDivisionError
except ZeroDivisionError:
    print("Cannot divide by zero!")
else:
    print("Division was successful")
finally:
    print("Execution completed.")
```

- `except` block handles the error.
- `else` block is skipped when an error occurs.
- `finally` block always runs, regardless of whether there was an error.

---

## 5.4 Common Debugging Techniques

### Using Print Statements

One simple way to debug your code is by adding print statements to track the flow of execution and values of variables.

```python
x = 5
y = 0

print(f"Before division: x = {x}, y = {y}")
result = x / y  # This will cause an error
print(f"After division: {result}")  # This line will not execute
```

By checking the output of print statements, you can narrow down where the issue occurs.

### Using a Debugger (`pdb`)

Python’s built-in debugger (`pdb`) allows you to step through your code line by line, inspect variables, and understand the flow.

```python
import pdb

x = 5
y = 0

pdb.set_trace()  # Set a breakpoint here

result = x / y  # Error will be raised here
print(result)
```

Once the breakpoint is reached, you can enter commands like `n` (next), `s` (step), `c` (continue), and others to interact with the code.

### IDE Debugging Tools

Most modern IDEs (e.g., PyCharm, VS Code) offer built-in debugging tools, allowing you to:
- Set breakpoints
- Step through code
- Inspect variable values in real-time
- Watch expressions

These tools can make the debugging process much easier and more efficient.

---

## 5.5 Best Practices for Debugging

### Writing Clean Code to Minimize Errors

To avoid errors in the first place, follow these best practices:
- **Use meaningful variable names**: Choose descriptive names that reflect their purpose.
- **Follow PEP 8**: Python’s official style guide helps maintain readability and consistency.
- **Keep functions small and focused**: Each function should do one thing well, making it easier to spot errors.

### Using Logging for Better Error Tracking

Instead of using print statements for debugging, you can use Python's `logging` module to record the execution flow, errors, and other important information.

```python
import logging

logging.basicConfig(level=logging.DEBUG)

def divide(x, y):
    logging.debug(f"Dividing {x} by {y}")
    if y == 0:
        logging.error("Cannot divide by zero")
        return None
    return x / y

result = divide(10, 0)
```

- Use `logging.debug()`, `logging.info()`, `logging.warning()`, `logging.error()`, and `logging.critical()` to categorize log messages.
- Logging provides better control over the level of output and can be configured to write to files or other external systems.

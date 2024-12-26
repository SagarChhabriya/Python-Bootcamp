# Types of Errors in Python

1. **Syntax Error**  
   Occurs when the code is not written in accordance with the rules of Python syntax. The interpreter cannot understand it.
   ```python
   # Example: Missing closing parenthesis
   print("Hello, World!"  # This will raise a SyntaxError
   ```

2. **Indentation Error**
   Happens when the indentation of the code blocks is not consistent. Python relies on indentation to define the structure of the code
   ```python
   # Example: Incorrect indentation
   def my_function():
   print("Hello, World!")  # This will raise an IndentationError
   ```
3. **Name Error**
   Occurs when the code refers to a variable or function that is not defined or is out of scope.<br>
   ```python
   # Example: Using an undefined variable
   print(x)  # This will raise a NameError if 'x' has not been defined
   ```

4. **Type Error**
   Happens when an operation or function is applied to an object of inappropriate type.
   ```python
   # Example: Trying to add an integer to a string
   x = "Hello"
   y = 5
   print(x + y)  # This will raise a TypeError

   ```
5. **Value Error**
   Raised when a built-in operation or function receives an argument that has the right type but an inappropriate value.
   ```python
   # Example: Converting a string that cannot be converted to an integer
   num = int("Hello")  # This will raise a ValueError

   ```

6. **Index Error**
   Occurs when trying to access an element from a list or tuple using an index that is out of range.
   ```python
   # Example: Accessing an index that doesn't exist
   my_list = [1, 2, 3]
   print(my_list[5])  # This will raise an IndexError
   ```

7. **Key Error**
   Happens when trying to access a dictionary with a key that does not exist.
   ```python
   # Example: Accessing a non-existent key
   my_dict = {'a': 1, 'b': 2}
   print(my_dict['c'])  # This will raise a KeyError

   ```

8. **Attribute Error**
   Occurs when an invalid attribute reference is made. This can happen when trying to access an attribute that an object does not possess.
   ```python
   # Example: Accessing a non-existent method
   my_list = [1, 2, 3]
   my_list.add(4)  # This will raise an AttributeError

   ```
9. **ZeroDivisionError**
   Raised when attempting to divide by zero.
   ```python
   # Example: Division by zero
   x = 10
   y = 0
   print(x / y)  # This will raise a ZeroDivisionError

   ```

10. **File Not Found Error**
   Occurs when trying to open a file that does not exist.
   
   ```python
   # Example: Attempting to read a non-existent file
   with open("non_existent_file.txt") as f:
   content = f.read()  # This will raise a FileNotFoundError
   ```


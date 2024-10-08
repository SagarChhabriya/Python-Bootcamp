# Labs tasks will be added soon

1. Create Valid Identifiers:
  - Define three valid identifiers in your program. For example:
  ```python
    my_variable = 5
    userName = "Alice"
    _privateData = 100
  ```

2. Experiment with Invalid Identifiers:
   - Try to create three invalid identifiers (e.g., using `$`, starting with a digit) and observe the errors.
  ```python
  # Uncommenting the following will result in syntax errors
  # 1stVariable = 10
  # invalid$name = "test"
  # my-variable = 20

  ```

3. Case Sensitivity Test:
  - Define two identifiers that differ only by case, then print both values.
    ```python
    value = 10
    Value = 20
    print(value)  # Output: 10
    print(Value)  # Output: 20

    ```
4. Check Length of Identifiers:
   - Create an identifier that is excessively long and print its value.
     ```python
     a_very_long_identifier_name_that_is_not_recommended = 42
     print(a_very_long_identifier_name_that_is_not_recommended)
     ```
5. Reserved Word Usage:
   - Attempt to create a variable using a reserved word (e.g., `def`) and observe the error.
    ```python
    # Uncommenting the following will result in a syntax error
    # def = 20
    ```
6. List Reserved Words:
   ```python
   import keyword
   print(keyword.kwlist)
   ```

## Basic Commands

7. Print Python Version:
  - Write a program to print the current version of Python you are using.
    ```python
    import sys
    print("Python version:", sys.version)
    ```
8. Check Current Working Directory(Current Folder):
   - Use the `os` module to print the current working directory.
    ```python
    import os
    print("Current Working Directory:", os.getcwd())
    ```
9. List Files in Directory:
   - Write a program to list all files in the current directory.
     ```python
     import os
     print("Files in current directory:", os.listdir())
     ```
10. Print Help for a Module:
    - Use the `help()` function to get information about a built-in function (e.g., `print`).
    ```python
    help(print)
    ```

11. Using dir()
    - Use the `dir()` function to list all the attributes and methods of a module (e.g., `math`).
    ```python
    import math
    print("Attributes and methods of math module:", dir(math))
    ```
## Additions 
1. **Single-Line Comments** Write a program that includes a single-line comment explaining what the code does.
  ```python
  # This program prints my name
  print("Sagar Chhabriya")
  ```

2. **Multi-Line Comments** Use multi-line comments to describe a program that calculates the area of a rectangle.
  ```python
  """
  This program calculates the area of a rectangle.
  The formula for the area is width * height.
  """
  width = 5
  height = 10
  area = width * height
  print("Area of the rectangle:", area)

  ```

3. **Commenting Out Code** Write a code snippet and comment out one line to prevent it from executing.
  ```python
  # This will print a greeting
  print("Hello, World!")
  # print("This line is commented out and won't run.")

  ```


4. **Descriptive Comments** Create a program that uses descriptive comments for each step in the code.
  ```python
  # Step 1: Define the radius
  radius = 7
  
  # Step 2: Calculate the area of the circle
  area = 3.14 * (radius ** 2)
  
  # Step 3: Print the result
  print("Area of the circle:", area)

  ```

5. **Using Comments for To-Do Notes** Write a program and add comments to indicate tasks that need to be completed.
  ```python
  # TODO: Add input for the user's name
  name = "Sagar Chhabriya"
  
  # TODO: Change the greeting message
  print("Hello,", name)

  ```

6. **Commenting Best Practices** Create a simple program and apply best practices for commenting, including clarity and conciseness.
  ```python
  # Calculate the total price after tax
  price = 100  # Original price in dollars
  tax_rate = 0.05  # Tax rate of 5%
  total_price = price + (price * tax_rate)  # Total price calculation
  print("Total price after tax:", total_price)


  ```

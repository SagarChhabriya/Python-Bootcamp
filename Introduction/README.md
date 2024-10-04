# Introduction to Programming Fundamentals Using Python

1. **What is Computer?**  
   An electronic device that accepts data as input, processes it, and produces output.
```python
# Example: Simple addition using a computer
x = 5
y = 10
result = x + y
print(result)  # Output: 15
```


2. **Are Computers More Intelligent than Humans?**  
   No, computers lack consciousness and understanding; they perform tasks based on programmed instructions.


4. **How to teach/train computers?**  
   By providing algorithms, data sets, and using techniques like machine learning to enable them to learn from data.

```python
# Example: Simple machine learning concept
from sklearn.linear_model import LinearRegression
import numpy as np

X = np.array([[1], [2], [3]])  # Input data
y = np.array([1, 2, 3])          # Output data
model = LinearRegression().fit(X, y)

```


5. **What is a program?**  
   A set of instructions written in a programming language that tells a computer how to perform specific tasks.
```python
# Example: A simple program to greet the user
def greet(name):
    return f"Hello, {name}!"

print(greet("Alice"))  # Output: Hello, Alice!

```


6. **Why was programming developed?**  
   To automate tasks, solve problems, and allow humans to interact with computers in a structured way.

7. **Why learning programming?**  
   It enhances problem-solving skills, provides career opportunities, and allows for creative expression through technology.

8. **What is software?**  
   A collection of programs and data that instructs a computer on how to perform tasks.

9. **Languages to Write programs**  
   Common languages include Python, Java, C++, JavaScript, and Ruby.

10. **Compiler VS Interpreter**  
   A compiler translates the entire program into machine code before execution, while an interpreter translates and executes the code line-by-line.

11. **What happens when things go wrong?**  
    Errors or bugs occur, which can be syntax errors, runtime errors, or logical errors, requiring debugging to fix.
```python
# Example: Syntax error
print("Hello, World!"  # Missing closing parenthesis

```


12. **History of Python**  
    Python was created by Guido van Rossum and first released in 1991, designed for readability and simplicity.

13. **IDE**  
    An Integrated Development Environment (IDE) is software that provides tools for writing, testing, and debugging code.

14. **Polya's 4 Steps of Problem Solving**  
    1. Understand the problem  
    2. Devise a plan  
    3. Carry out the plan  
    4. Review/extend the solution

15. **Algorithm**  
    A step-by-step procedure or formula for solving a problem.
```python
Algorithm to find the maximum of two numbers:
1. Input two numbers, a and b.
2. If a > b, then max = a.
3. Else, max = b.
4. Output max.

```


16. **First programming in Python**  
    A simple "Hello, World!" program: `print("Hello, World!")`.

17. **Structure of a python program**  
    Typically includes imports, function definitions, and the main execution block.
```python
# Example structure
import math

def main():
    print(math.sqrt(16))  # Output: 4.0

if __name__ == "__main__":
    main()

```


18. **Features of Python**  
    Easy to read, dynamically typed, supports multiple programming paradigms, extensive libraries.

19. **Statements, Variable declarations, Calling of Functions, Comments**  
    Statements perform actions, variables store data, functions encapsulate code, and comments explain the code.

```python
# Example of each
x = 10  # Variable declaration
def add(a, b):  # Function definition
    return a + b

print(add(x, 5))  # Calling the function

```


20. **Variables**  
    Named storage locations in memory that hold data.
```python
# Example
age = 25  # 'age' is a variable holding the value 25

```


21. **Three actions for variables**  
    Declaration, assignment, and usage.
```python
# Example
count = 0  # Declaration and assignment
count += 1  # Usage

```


22. **Characteristics of variable**  
    Must have a name, hold a value, and can change over time.

23. **Variable and its values in memory**  
    A variable points to a memory location that stores its value.

```python
# Example
a = 10  # 'a' points to a memory location containing 10

```

24. **Rules for defining a variable name**  
    Must start with a letter or underscore, followed by letters, digits, or underscores; case-sensitive.
```python
# Valid variable names
_variable = 5
variable2 = 10
variableName = "example"  # Camel case
VariableName = "example"  # Pascal case
variable_name = "example"  # Snake case

  
```    

26. **Reserved words**  
    Keywords in Python that have special meanings and cannot be used as variable names (e.g., `if`, `while`, `def`).

27. **Constants**  
    Values that do not change during the execution of a program.

```python
# Example
PI = 3.14159  # Constant
```    

29. **Whitespaces**  
    Spaces, tabs, and newlines used for readability and structure; significant in Python for indentation.

```python
# Example of indentation
def example():
    print("This is indented")  # Correct indentation

```

30. **Data Types**  
    Categories of data that determine the type of value a variable can hold (e.g., int, float, str).

```python
count = 10  # Example of an integer
weight = 65.5  # Example of a float
char = 'A'  # Example of a character
name = "Alice"  # Example of a string

```
    

32. **Why different data types?**  
    To handle various kinds of data efficiently and optimize memory usage.

33. **Data Types: Countable, Measureable, Character, String**  
    - Countable: Integers (e.g., `int`)  
    - Measurable: Floating-point numbers (e.g., `float`)  
    - Character: Single characters (e.g., `char`)  
    - String: Sequences of characters (e.g., `str`)  

---
## Topics that will be covered later as well.

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


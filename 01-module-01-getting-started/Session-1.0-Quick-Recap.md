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



16. **Variables**  
    Named storage locations in memory that hold data.
      ```python
      # Example
      age = 25  # 'age' is a variable holding the value 25
      
      ```


17. **Three actions for variables**  
    Declaration, assignment, and usage.
      ```python
      # Example
      count = 0  # Declaration and assignment
      count += 1  # Usage
      
      ```


18. **Characteristics of variable**  
    Must have a name, hold a value, and can change over time.

19. **Variable and its values in memory**  
    A variable points to a memory location that stores its value.

      ```python
      # Example
      a = 10  # 'a' points to a memory location containing 10
      
      ```

20. **Rules for defining a variable name**  
    Must start with a letter or underscore, followed by letters, digits, or underscores; case-sensitive.
      ```python
      # Valid variable names
      _variable = 5
      variable2 = 10
      variableName = "example"  # Camel case
      VariableName = "example"  # Pascal case
      variable_name = "example"  # Snake case
      
        
      ```    

21. **Reserved words**  
    Keywords in Python that have special meanings and cannot be used as variable names (e.g., `if`, `while`, `def`).

22. **Constants**  
    Values that do not change during the execution of a program.

      ```python
      # Example
      PI = 3.14159  # Constant
      ```    

23. **Whitespaces**  
    Spaces, tabs, and newlines used for readability and structure; significant in Python for indentation.

      ```python
      # Example of indentation
      def example():
          print("This is indented")  # Correct indentation
      
      ```

24. **Data Types**  
    Categories of data that determine the type of value a variable can hold (e.g., int, float, str).

      ```python
      count = 10  # Example of an integer
      weight = 65.5  # Example of a float
      char = 'A'  # Example of a character
      name = "Alice"  # Example of a string
      
      ```
    

25. **Why different data types?**  
    To handle various kinds of data efficiently and optimize memory usage.

26. **Data Types: Countable, Measureable, Character, String**  
    - Countable: Integers (e.g., `int`)  
    - Measurable: Floating-point numbers (e.g., `float`)  
    - Character: Single characters (e.g., `char`)  
    - String: Sequences of characters (e.g., `str`)  

---

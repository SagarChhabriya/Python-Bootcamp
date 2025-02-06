# 12. Program Control Flow

Program control flow refers to the order in which statements and instructions are executed in a program. Python provides several tools for controlling the flow of a program, including **conditional statements** and **loops**.



<span style="display: flex; justify-content: space-between; width: 100%; align-items: center;">
    <a href="../11-module-11-nested-data-structures/README.md">
        <img src="https://img.shields.io/badge/Previous-Python_Dictionaries-blue" width="250" height="35">
    </a>
    <a href="../12-module-12-program-control-flow/session-12.1.md">
        <img src="https://img.shields.io/badge/Next-Case_Match-brightgreen" width="160" height="35">
    </a>
</span>
<br><br>

## 12.1 Introduction to Program Control Flow

- **Control Flow** refers to the way the program moves from one instruction to another.
- **Conditional Statements**: Allow decisions to be made, so different paths in the code can be followed depending on conditions.
- **Loops**: Allow repetitive execution of code until a condition is met.

---

## 12.2 Conditional Statements

Conditional statements allow us to execute different blocks of code based on whether a condition is `True` or `False`.

### 12.2.1 The `if` Statement
- **Syntax**: 
  ```python
  if condition:
      # Code to execute if condition is True
  ```
- **Example**:
  ```python
  x = 5
  if x > 3:
      print("x is greater than 3")
  ```
  Output: `x is greater than 3`

- **Explanation**: The `if` statement checks the condition (`x > 3`), and if it evaluates to `True`, it executes the block of code underneath it.


### 12.2.2 The `if-else` Statement
- **Syntax**: 
  ```python
  if condition:
      # Code to execute if condition is True
  else:
      # Code to execute if condition is False
  ```
- **Example**:
  ```python
  x = 2
  if x > 3:
      print("x is greater than 3")
  else:
      print("x is not greater than 3")
  ```
  Output: `x is not greater than 3`

- **Explanation**: If the `if` condition is `False`, the `else` block is executed.


### 12.2.3 The `if-elif` Statement
- **Syntax**: 
  ```python
  if condition1:
      # Code for condition1
  elif condition2:
      # Code for condition2
  else:
      # Code if none of the conditions are True
  ```
- **Example**:
  ```python
  x = 8
  if x > 10:
      print("x is greater than 10")
  elif x > 5:
      print("x is greater than 5 but less than or equal to 10")
  else:
      print("x is 5 or less")
  ```
  Output: `x is greater than 5 but less than or equal to 10`

- **Explanation**: `elif` stands for "else if" and allows checking multiple conditions.



### 12.2.4 Nested `if` Statements
- **Syntax**: 
  ```python
  if condition1:
      if condition2:
          # Code if both conditions are True
  ```
- **When and How to Use**: Nested `if` statements are useful when you have to check multiple conditions that depend on each other.

- **Example**:
  ```python
  x = 10
  if x > 5:
      if x < 15:
          print("x is between 5 and 15")
  ```
  Output: `x is between 5 and 15`

- **Explanation**: The second `if` is only evaluated if the first `if` is `True`.


### 12.2.5 Short Hand If
If you have only one statement to execute, you can put it on the same line as the if statement.

- **Example**
  ```python
  if a > b: print("a is greater than b")
  ```


### 12.2.6 Short Hand If-else (Ternory Operator)
If you have only one statement to execute, one for if, and one for else, you can put it all on the same line:

- **Exmaple**
  ```python
  a = 12
  b = 33
  print("A") if a > b else print("B")
  ```

### 12.2.7 If condition with and operator
The and keyword is a logical operator, and is used to combine conditional statements:
- **Example:** Test if `a` is greater than `b`, AND if `c` is greater than `a`:

  ```python
  a = 20
  b = 3
  c = 50
  if a > b and c > a:
      print("Both conditions are True")
  ```


### 12.2.8 If condition with or operator

  ```python
  a = 20
  b = 3
  c = 50
  if a > b or c > a:
      print("At least one of the conditions is True")
  ```

### 12.2.9 If condition with not operator

  ```python
  a = 3
  b = 20
  if not a > b:
      print("a is NOT greater than b")
  ```

### 12.2.10 Pass statement
if statements cannot be empty, but if you for some reason have an if statement with no content, put in the pass statement to avoid getting an error.

- **Example**

  ```python
  a = 13
  b = 20

  if b > a:
    pass
  ```


## **12.3 Python Indentation**
Python uses indentation to define blocks of code. Incorrect indentation leads to errors.


- **Example**:
  ```python
  if True:
      print("This is inside the if block")
  print("This is outside the if block")
  ```
  Output:
  ```
  This is inside the if block
  This is outside the if block
  ```

- **Explanation**: The code inside the `if` block is indented, while the code outside is not. 

- **Example:** If statement, without indentation (will raise an error):
  ```python
  a = 13
  b = 30
  if b > a:
  print("b is greater than a") # you will get an error
  ```



## 12.4 Looping and Iteration

Loops are used to execute a block of code repeatedly, either a fixed number of times or until a certain condition is met.

### 12.4.1 The `for` Loop
- **Syntax**: 
  ```python
  for variable in iterable:
      # Code to execute
  ```
- **Example**:
  ```python
  for i in range(3):
      print(i)
  ```
  Output: 
  ```
  0
  1
  2
  ```

- **Explanation**: The `for` loop iterates over each item in the iterable (`range(3)` in this case) and executes the block of code.

---

### 12.4.2 The `for in` Loop
- **Iterating Over Sequences (Lists, Strings, etc.)**:
  You can iterate over any iterable object such as lists, strings, or dictionaries.
  
- **Example** (list iteration):
  ```python
  fruits = ["apple", "banana", "cherry"]
  for fruit in fruits:
      print(fruit)
  ```
  Output:
  ```
  apple
  banana
  cherry
  ```

- **Example** (string iteration):
  ```python
  word = "hello"
  for letter in word:
      print(letter)
  ```
  Output:
  ```
  h
  e
  l
  l
  o
  ```

---

### 12.4.3 The `while` Loop
With the while loop we can execute a set of statements as long as a condition is true.

- **Syntax**: 
  ```python
  while condition:
      # Code to execute
  ```
- **Example**:
  ```python
  x = 0
  while x < 3:
      print(x)
      x += 1
  ```
  Output:
  ```
  0
  1
  2
  ```

- **Explanation**: The `while` loop keeps executing as long as the condition (`x < 3`) is `True`.

---

### 12.4.4 The `else` Statement with Loops
- **How `else` Works with Loops**: The `else` part of a loop is executed when the loop finishes without encountering a `break` statement.

- **Example**:
  ```python
  for i in range(5):
      print(i)
  else:
      print("Loop finished without break")
  ```
  Output:
  ```
  0
  1
  2
  3
  4
  Loop finished without break
  ```

- **Example with `break`**:
  ```python
  for i in range(5):
      if i == 3:
          break
      print(i)
  else:
      print("This will not print because of break")
  ```
  Output:
  ```
  0
  1
  2
  ```

- **Explanation**: The `else` block is only executed if the loop completes without hitting `break`.

---

### 12.4.5 Looping Over Lists
- **Example**: Iterating through a list of numbers and printing only even numbers.
  ```python
  numbers = [1, 2, 3, 4, 5]
  for num in numbers:
      if num % 2 == 0:
          print(num)
  ```
  Output: 
  ```
  2
  4
  ```

---

### 12.4.6 Looping Over Strings
- **Example**: Iterating through characters of a string and checking for vowels.
  ```python
  word = "programming"
  vowels = "aeiou"
  for char in word:
      if char in vowels:
          print(char)
  ```
  Output:
  ```
  o
  a
  i
  ```
  
---

### 12.4.7 Nested Loops
- **Syntax**: A loop inside another loop.
- **Example**:
  ```python
  for i in range(3):
      for j in range(2):
          print(f"i = {i}, j = {j}")
  ```
  Output:
  ```
  i = 0, j = 0
  i = 0, j = 1
  i = 1, j = 0
  i = 1, j = 1
  i = 2, j = 0
  i = 2, j = 1
  ```

- **Explanation**: The outer loop runs 3 times, and for each iteration, the inner loop runs 2 times.

---

## 12.5 Loop Control Statements

### 12.5.1 `break` Statement
- **Exiting Loops Early**: The `break` statement is used to exit the loop prematurely.
- **Example**:
  ```python
  for i in range(5):
      if i == 3:
          break
      print(i)
  ```
  Output:
  ```
  0
  1
  2
  ```

- **Explanation**: The loop breaks when `i` is 3, and no further iterations are made.

---

### 12.5.2 `continue` Statement
- **Skipping the Current Iteration**: The `continue` statement skips the current iteration of the loop and proceeds to the next one.
- **Example**:
  ```python


  for i in range(5):
      if i == 3:
          continue
      print(i)
  ```
  Output:
  ```
  0
  1
  2
  4
  ```

- **Explanation**: When `i` equals 3, the `continue` statement skips that iteration.

---

## 12.6 The `range()` Function

### 12.6.1 Introduction to `range()`
- The `range()` function generates a sequence of numbers, often used in loops.
- **Syntax**:
  ```python
  range(start, stop, step)
  ```

### 12.6.2 Types of `range()` Function
- **Basic `range()`**: Generates a sequence from `0` to `stop-1`.
  ```python
  for i in range(5):
      print(i)
  ```
  Output:
  ```
  0
  1
  2
  3
  4
  ```

- **With `start` and `stop`**:
  ```python
  for i in range(2, 7):
      print(i)
  ```
  Output:
  ```
  2
  3
  4
  5
  6
  ```

- **With `start`, `stop`, and `step`**:
  ```python
  for i in range(1, 10, 2):
      print(i)
  ```
  Output:
  ```
  1
  3
  5
  7
  9
  ```

### 12.6.3 `range()` vs `xrange()` (Python 2.x vs Python 3.x)
- In Python 2.x, `range()` returns a list, while `xrange()` returns an iterator (more memory efficient).
- In Python 3.x, `range()` behaves like `xrange()` (returns an iterator).

---

## 12.7 Switch Case (Simulated in Python)

Python does not have a built-in `switch` statement, but you can simulate it using `if-elif-else` statements or dictionaries.

- **Example using `if-elif-else`**:
  ```python
  day = 3
  if day == 1:
      print("Monday")
  elif day == 2:
      print("Tuesday")
  elif day == 3:
      print("Wednesday")
  ```

- **Example using a dictionary**:
  ```python
  days = {1: "Monday", 2: "Tuesday", 3: "Wednesday"}
  print(days.get(3, "Invalid day"))
  ```
- **Dictionary with function:**

 ```python
  def switch_case(value):
      return {
          1: "Case 1",
          2: "Case 2",
          3: "Case 3"
      }.get(value, "Default Case")

  print(switch_case(2))  # Output: Case 2
  ```  

---

## 12.8 Python Iterators

- **What Iterators Are**: An iterator is an object that represents a stream of data, and it knows how to get the next value in the sequence.
  
- **Example**:
  ```python
  my_list = [1, 2, 3]
  my_iter = iter(my_list)
  
  print(next(my_iter))  # Output: 1
  print(next(my_iter))  # Output: 2
  ```

---

## 12.9 Python Generators

- **Introduction to Generators**: Generators allow you to iterate over data without storing the entire dataset in memory. They are defined using the `yield` keyword.

- **Example**:
  ```python
  def count_up_to(max):
      count = 1
      while count <= max:
          yield count
          count += 1

  counter = count_up_to(5)
  for num in counter:
      print(num)
  ```
  Output:
  ```
  1
  2
  3
  4
  5
  ```

- **Explanation**: `yield` returns a value and pauses the function’s execution, allowing you to continue where you left off.


<span style="display: flex; justify-content: space-between; width: 100%; align-items: center;">
    <a href="../11-module-11-nested-data-structures/README.md">
        <img src="https://img.shields.io/badge/Previous-Python_Dictionaries-blue" width="250" height="35">
    </a>
    <a href="../12-module-12-program-control-flow/session-12.1.md">
        <img src="https://img.shields.io/badge/Next-Case_Match-brightgreen" width="160" height="35">
    </a>
</span>
<br><br>
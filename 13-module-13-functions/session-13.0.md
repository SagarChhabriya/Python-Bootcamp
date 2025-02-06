# 13. Introduction to Functions

Functions are reusable blocks of code that perform a specific task. They help in organizing code, improving readability, and reducing redundancy.


<span style="display: flex; justify-content: space-between; width: 100%; align-items: center;">
    <a href="../12-module-12-program-control-flow/README.md">
        <img src="https://img.shields.io/badge/Previous-Program_Control_Flow-blue" width="250" height="35">
    </a>
    <a href="../14-module-14-project-I/README.md">
        <img src="https://img.shields.io/badge/Next-Project_I-brightgreen" width="160" height="35">
    </a>
</span>
<br><br>


## 13.1 Introduction to Functions
- A function is a block of code which only runs when it is called.
- You can pass data, known as parameters, into a function.
- A function can return data as a result.

## 13.2 Creating and Calling Functions

- **Structure of Python Functions**
The basic syntax for defining a function in Python:

```python
def function_name(parameters):
    # Code block
    return value
```


### 13.2.1 Creating a Function
In Python, a function is defined using the `def` keyword:

```python
def greet_user():
  print("Greetings from the function")
```

### 13.2.2 Calling a Function
To call a function, use the function name followed by parentheses:

**Example:**

```python
def greet_user():
  print("Greetings from the function")

greet_user()
```

## 13.3 Arguments and Parameters

### 13.3.1 Arguments
- Information can be passed into functions as arguments.
- Arguments are specified after the function name, inside the parentheses. You can add as many arguments as you want, just separate them with a comma.

- The following example has a function with one argument (name). When the function is called, we pass along a first name, which is used inside the function to print the full name:

**Example:**

```python
def introduce(name):
  print(name + " Johnson")

introduce("Alice")
introduce("Bob")
introduce("Charlie")
```



### 13.3.2 Number of Arguments
By default, a function must be called with the correct number of arguments. Meaning that if your function expects 2 arguments, you have to call the function with 2 arguments, not more, and not less.

**Example:**
```python
def full_name(first, last):
  print(first + " " + last)

full_name("John", "Doe")
```

- If you call the function with too few or too many arguments, it will result in an error.


- **Example:**
This function expects 2 arguments, but gets only 1:

```python
def my_function(fname, lname):
  print(fname + " " + lname)

my_function("Emil")
```


### **Default Parameters**
- You can set a default value for a parameter. If no argument is passed, the default value will be used.

- Parameters with default values.
- **Example**:
  ```python
  def greet(name="Guest"):
      return f"Hello, {name}!"

  print(greet())  # Output: Hello, Guest!
  print(greet("Alice")) # Output: Hello, Alice!

  ```

**Example:**

  ```python
  def country_of_origin(country = "Canada"):
    print("I am from " + country)

  country_of_origin("Germany")
  country_of_origin("India")
  country_of_origin()  # Uses default value "Canada"
  country_of_origin("Brazil")
  ```


### **Non-default Parameters**
- These are parameters that must be provided when calling the function.
- **Example**:
  ```python
    def add(a, b):
        return a + b

    # add()  # Error: Missing required parameters
    print(add(2, 3))  # Output: 5    
  ```

### **Named/Keyword Parameters**
- Parameters can be passed by name, making it clearer which value corresponds to which parameter.

- **Example**:
  ```python
  def greet(name, message):
      return f"{message}, {name}!"

  print(greet(message="Hi", name="Alice"))  # Output: Hi, Alice!
  ```
- You can also send arguments with the `key = value` syntax, which allows you to pass arguments in any order.

**Example:**

  ```python
  def kids_order(child3, child2, child1):
    print("The youngest child is " + child3)

  kids_order(child1 = "Liam", child2 = "Ethan", child3 = "Lucas")
  ```

  ```python
  def greet(name, message):
      return f"{message}, {name}!"

  print(greet(message="Hi", name="Alice"))  # Output: Hi, Alice!
  ```


### **Non-keyword Arguments**
- Arguments passed by position (not by name).

- **Example**:
  ```python
  print(greet("Alice", 25))
  ```


### 13.3.3 Arbitrary Arguments (`*args`)
- **`*args`**: Allows for a variable number of positional arguments.
- If you do not know how many arguments will be passed into your function, add a `*` before the parameter name.
- This way, the function will receive a tuple of arguments.

**Example:**
If the number of arguments is unknown, add a * before the parameter name:

  ```python
  def youngest_child(*children):
    print("The youngest child is " + children[2])

  youngest_child("Liam", "Ethan", "Lucas")
  ```

  ```python
    def sum_all(*args):
        return sum(args)

    print(sum_all(1, 2, 3))  # Output: 6
  ```


### 13.3.4 Arbitrary Keyword Arguments (`**kwargs`)
- **`**kwargs`**: Allows for a variable number of keyword arguments.
  - `**kwargs`: Variable-length keyword arguments.
- If you do not know how many keyword arguments will be passed into your function, add two asterisks `**` before the parameter name.
- This way, the function will receive a dictionary of arguments.

**Example:**

  ```python
  def display_info(**person):
    print("The person's last name is " + person["surname"])

  display_info(firstname = "Ethan", surname = "Smith")
  ```

  ```python
    def print_details(**kwargs):
        for key, value in kwargs.items():
            print(f"{key}: {value}")

    print_details(name="Alice", age=25)
    # Output:
    # name: Alice
    # age: 25
  ```

#### Example: Using `*args` and `**kwargs`

  ```python
  def display_info(name, *args, **kwargs):
      print(f"Name: {name}")
      print("Additional info:", args)
      print("Keyword info:", kwargs)

  display_info("Alice", 25, "Engineer", city="New York", country="USA")
  ```

  Output:
  ```bash
  Name: Alice
  Additional info: (25, 'Engineer')
  Keyword info: {'city': 'New York', 'country': 'USA'}
  ```




## 13.4 Passing a List as an Argument
- You can send any data type as an argument to a function (e.g., string, number, list, dictionary).
- If you pass a list as an argument, it will be treated as a list inside the function.

**Example:**

  ```python
  def display_fruits(fruit_list):
    for fruit in fruit_list:
      print(fruit)

  fruits = ["apple", "orange", "grape"]

  display_fruits(fruits)
  ```

## 13.5 Return Values and pass statement

### Return Values
- To return a value from a function, use the `return` statement.
- It exits the function and returns a value.


**Example:**

  ```python
  def multiply_by_ten(number):
    return 10 * number

  print(multiply_by_ten(2))
  print(multiply_by_ten(4))
  print(multiply_by_ten(7))
  ```

  ```python
  def add(a, b):
        return a + b

  result = add(2, 3)
  print(result)  # Output: 5
  ```

- **Returning Multiple Values**:
  ```python
  def get_details():
      return "Alice", 25

  name, age = get_details()
  print(name, age)  # Output: Alice 25
  ```

### The `pass` Statement
- Function definitions cannot be empty. If you need to create a function without any code, use the `pass` statement to avoid an error.

**Example:**

  ```python
  def empty_function():
    pass
  ```

## 13.6 Positional-Only and Keyword-Only Arguments

### 13.6.1 Positional-Only Arguments
- You can specify that a function can have only positional arguments by adding a `/` after the arguments.

**Example:**

  ```python
  def show_value(value, /):
    print(value)

  show_value(42)  # Correct usage
  ```

- Without the `/`, you can use keyword arguments even if the function expects positional arguments.

**Example:**

  ```python
  def show_value(value):
    print(value)

  show_value(value = 42)  # Error
  ```

But when adding the , / you will get an error if you try to send a keyword argument:

- **Example:**

  ```python
  def my_function(x, /):
    print(x)

  my_function(x = 3)
  ```

### 13.6.2 Keyword-Only Arguments
- To specify that a function can have only keyword arguments, add a `*` before the arguments.

**Example:**

  ```python
  def show_value(*, value):
    print(value)

  show_value(value = 42)  # Correct usage
  ```

- Without the `*`, you can use positional arguments even if the function expects keyword arguments.

**Example:**

  ```python
  def show_value(value):
    print(value)

  show_value(42)  # Error
  ```

- But with the *, you will get an error if you try to send a positional argument:



### 13.6.3 Combining Positional-Only and Keyword-Only Arguments
- You can combine positional-only and keyword-only arguments in the same function. 
- Any argument before the `/` is positional-only, and any argument after the `*` is keyword-only.

**Example:**

  ```python
  def add_numbers(a, b, /, *, c, d):
    print(a + b + c + d)

  add_numbers(5, 6, c = 7, d = 8)
  ```

## 13.7 Recursion
- Python supports recursion, meaning a function can call itself.
- Recursion is useful for looping through data to reach a result but can use excess memory or processor power if not carefully managed.

**Example (Recursion):**

  ```python
  def factorial(n):
    if n == 0:  # Base case: factorial of 0 is 1
        return 1
    return n * factorial(n - 1)  # Recursive case

  print(factorial(5))  # Output: 120
  ```

## **13.8 Built-In Functions**
- Python provides many built-in functions that are always available for use.
- **Examples**:
  - `map()`: Applies a function to all items in an iterable.
    ```python
    map(callback, iterator)
    ```
    Where:
    - **`callback`**: A function (or lambda) that takes an element from the `iterator` and processes it.
    - **`iterator`**: An iterable (like a list, tuple, or string) whose elements are passed to the `callback`.

    ```python
    numbers = [1, 2, 3]
    squared = list(map(lambda x: x**2, numbers))
    print(squared)  # Output: [1, 4, 9]
    ```

  - `zip()`: Combines multiple iterables element-wise into tuples.
    
    ```python
    zip(iterable1, iterable2, ...)
    ```
    Where:
    - iterable1, iterable2, ...: Multiple iterables (like lists, tuples, etc.) to be combined element-wise.

    ```python
    names = ["Alice", "Bob"]
    ages = [25, 30]
    combined = list(zip(names, ages))
    print(combined)  # Output: [('Alice', 25), ('Bob', 30)]
    ```
  - `reduce()`(from `functools`): Applies a function of two arguments cumulatively to the items of an iterable.
    ```python
    reduce(function, iterable, [initial])
    ```
    - Applies a binary function cumulatively to the items of an iterable, from left to right, reducing it to a single value. The optional `initial` argument can be provided to start the accumulation.
    
    ```python
    from functools import reduce
    numbers = [1, 2, 3, 4]
    total = reduce(lambda x, y: x + y, numbers)
    print(total)  # Output: 10
    ```

    ```python
    from functools import reduce

    numbers = [1, 2, 3, 4]
    result = reduce(lambda x, y: x + y, numbers, 10)
    print(result)  # Output: 20
    ```

    ### Explanation:
    - The `initial` value is set to `10`. 
    - The `reduce()` function starts by using `10` as the initial value and then adds each number in the list to it.
    - First, it calculates `10 + 1 = 11`, then `11 + 2 = 13`, then `13 + 3 = 16`, and finally `16 + 4 = 20`.
    - The result is `20`. The `initial` value (`10`) is included in the accumulation.

  - `filter()`: Filters elements based on a condition.
    ```python
    filter(function, iterable)
    ```
    - Filters elements from the iterable by applying the `function`. Only elements for which the `function` returns `True` are included in the result.
    
    ```python
    numbers = [1, 2, 3, 4]
    even = list(filter(lambda x: x % 2 == 0, numbers))
    print(even)  # Output: [2, 4]
    ```
  - `any()`: Returns `True` if any element in an iterable is `True`.
    ```python
    values = [False, True, False]
    print(any(values))  # Output: True

    numbers = [0, 0, 1]
    print(any(numbers))  # Output: True
    ```
  - `all()`: Returns `True` if all elements in an iterable are `True`.
    ```python
    values = [True, True, False]
    print(all(values))  # Output: False
    ```
  - `sorted()`: Returns a sorted list.
    ```python
    numbers = [3, 1, 4, 2]
    print(sorted(numbers))  # Output: [1, 2, 3, 4]
    ```

  - `chr()` and `ord()`: Converts between character and ASCII value.
    ```python
    print(chr(65))  # Output: 'A'
    print(ord('A'))  # Output: 65
    ```

- **`globals()` and `locals()`**: Return dictionaries representing the current global and local symbol tables.
    ```python
    a = 10
    def test():
        b = 20
        print(globals())  # Contains global variables, e.g., 'a'
        print(locals())   # Contains local variables, e.g., 'b'
    test()
    ```

---


## **13.9 Lambda Functions**
- **Definition**: Anonymous functions defined using the `lambda` keyword.
  - A lambda function is a small anonymous function.  
  - A lambda function can take any number of arguments, but it can only have one expression.

- **Syntax**:
  ```python
  lambda arguments: expression
  ```
The expression is executed and the result is returned.

### Example 1:
Add 10 to argument `a`, and return the result:
```python
x = lambda a : a + 10
print(x(5))  # Output: 15
```

### Example 2:
Multiply argument `a` with argument `b` and return the result:
```python
x = lambda a, b : a * b
print(x(5, 6))  # Output: 30
```

### Example 3:
Summarize arguments `a`, `b`, and `c` and return the result:
```python
x = lambda a, b, c : a + b + c
print(x(5, 6, 2))  # Output: 13
```

## Why Use Lambda Functions?

The power of lambda is better demonstrated when used as an anonymous function inside another function.

### Example: Function that multiplies by `n`
Say you have a function definition that takes one argument, and that argument will be multiplied by an unknown number:

```python
def myfunc(n):
  return lambda a : a * n
```

Use that function definition to make a function that always doubles the number you send in:

```python
mydoubler = myfunc(2)
print(mydoubler(11))  # Output: 22
```

Or, use the same function definition to make a function that always triples the number you send in:

```python
mytripler = myfunc(3)
print(mytripler(11))  # Output: 33
```

### Example: Both Doubler and Tripler
You can create both functions in the same program:

```python
def myfunc(n):
  return lambda a : a * n

mydoubler = myfunc(2)
mytripler = myfunc(3)

print(mydoubler(11))  # Output: 22
print(mytripler(11))  # Output: 33
```

- Use lambda functions when an anonymous function is required for a short period of time.



<!-- ## **13.10 Advanced Function Concepts**

### **13.10.1 Python Closures**
- A **closure** is a function object that remembers values in its enclosing scopes, even if they are no longer in memory.
- **Example**:
  ```python
  def outer_function(x):
      def inner_function(y):
          return x + y
      return inner_function

  add_five = outer_function(5)
  print(add_five(3))  # Output: 8
  ```

### **13.10.2 Function Decorators**
- Decorators are functions that modify the behavior of other functions.
- **Example**:
  ```python
  def decorator(func):
      def wrapper():
          print("Before function call")
          func()
          print("After function call")
      return wrapper

  @decorator
  def say_hello():
      print("Hello!")

  say_hello()
  # Output:
  # Before function call
  # Hello!
  # After function call
  ```

### **13.10.3 Decorators with Parameters**
- You can pass parameters to decorators for more flexibility.
- **Example**:
  ```python
  def repeat(n):
      def decorator(func):
          def wrapper(*args, **kwargs):
              for _ in range(n):
                  func(*args, **kwargs)
          return wrapper
      return decorator

  @repeat(3)
  def greet(name):
      print(f"Hello, {name}!")

  greet("Alice")
  # Output:
  # Hello, Alice!
  # Hello, Alice!
  # Hello, Alice!
  ```

### **13.10.4 Memoization Using Decorators**
- Memoization caches the results of expensive function calls.
- **Example**:
  ```python
  from functools import lru_cache

  @lru_cache(maxsize=None)
  def fibonacci(n):
      if n < 2:
          return n
      return fibonacci(n - 1) + fibonacci(n - 2)

  print(fibonacci(10))  # Output: 55
  ```

### **13.10.5 Partial Functions**
- Partial functions allow you to pre-define some arguments for a function. Creating new functions by fixing some arguments of an existing function.
- **Example**:
  ```python
    from functools import partial

    def multiply(a, b):
        return a * b

    double = partial(multiply, 2)
    print(double(5))  # Output: 10

  
    def power(base, exp):
        return base ** exp

    square = partial(power, exp=2)
    print(square(4))  # Output: 16
  ```

---

## **13.11 Special Python Function Concepts**

### **13.11.1 `yield` Instead of `return`**
- The `yield` keyword is used to return a generator instead of a value. This allows the function to return multiple values lazily.
- **Example**:
  ```python
  def generate_numbers(n):
      for i in range(n):
          yield i

  for num in generate_numbers(3):
      print(num)
  # Output:
  # 0
  # 1
  # 2
  ```

### **13.11.2 First-Class Functions**
- Functions are treated as first-class objects in Python, meaning they can be passed as arguments, returned from functions, and assigned to variables.
- **Example**:


    ```python
    def greet(name):
        return f"Hello, {name}!"

    say_hello = greet
    print(say_hello("Alice"))  # Output: Hello, Alice!
    ```
        
    ```python
    def greet(name):
        return f"Hello, {name}!"

    def call_function(func, name):
        return func(name)

    print(call_function(greet, "Alice"))  # Output: Hello, Alice!
    ```

### **13.11.3 Precision Handling**
- Functions like `round()` help in controlling the precision of floating-point numbers.
- **Example**:
  ```python
  print(round(3.14159, 2))  # Output: 3.14
  ```

---

## **13.12 Miscellaneous Function-Related Topics**

### **13.12.1 `help()` Function**
- Provides documentation for functions and modules.
- **Example**:
  ```python
  help(print)
  ```

### **13.12.2 `__import__()` Function**
- Dynamically imports modules.
- **Example**:
  ```python
  math = __import__("math")
  print(math.sqrt(16))  # Output: 4.0
  ```

### **13.12.3 Coroutines in Python**
- Coroutines are functions that can pause and resume their execution. You can use the `async`/`await` syntax to define and call them.

- **Example**:
  ```python
  def coroutine():
      while True:
          value = yield
          print(f"Received: {value}")

  c = coroutine()
  next(c)  # Start the coroutine
  c.send(10)  # Output: Received: 10
  ```

### **13.12.4 Python Bit Functions on `int`**
- Functions like `bit_length()`, `to_bytes()`, and `from_bytes()`.
- **Example**:
  ```python
  num = 10
  print(num.bit_length())  # Output: 4
  ```

### **13.12.5 Using Collections as Function Parameters**
- Passing lists, dictionaries, etc., to functions.
- **Example**:
  ```python
  def process_list(lst):
      return [x * 2 for x in lst]

  print(process_list([1, 2, 3]))  # Output: [2, 4, 6]
  ```

---


### 13.13 **Additional Advanced Concepts in Functions**

#### 13.13.1 **Function Annotations**
Python allows function annotations, which can be used to attach metadata to function arguments and return values. These annotations don't affect the function's behavior but can help with documentation or type checking.

##### Example:
```python
def add(a: int, b: int) -> int:
    return a + b

# Here, 'a' and 'b' are expected to be integers, and the return value is also an integer.
```

- **Use with Static Type Checkers**: Tools like `mypy` can be used to check if the types are being followed.

#### 13.13.2 **Function Overloading**
Python doesn't support **function overloading** natively, like other languages (e.g., Java or C++). However, function overloading can be simulated by using default arguments, `*args`, `**kwargs`, or manually checking argument types within the function.

##### Example of Simulating Overloading:
```python
def greet(name=None, age=None):
    if name and age:
        print(f"Hello, {name}. You are {age} years old.")
    elif name:
        print(f"Hello, {name}.")
    elif age:
        print(f"Age: {age}")
    else:
        print("Hello, World!")

greet("Alice", 25)  # Output: Hello, Alice. You are 25 years old.
greet("Bob")        # Output: Hello, Bob.
greet(age=30)       # Output: Age: 30
```

#### 13.13.3 **Function Composition**
Function composition involves combining multiple functions into a single function. The result of one function is passed as the input to another function.

##### Example:
```python
def add_one(x):
    return x + 1

def square(x):
    return x * x

# Function composition: square(add_one(x))
result = square(add_one(3))
print(result)  # Output: 16
```

#### 13.13.4 **Nested Functions (Inner Functions)**
Functions can be defined inside other functions. These are called **nested functions** or **inner functions**.

##### Example:
```python
def outer():
    def inner():
        print("Inside inner function")
    inner()

outer()  # Output: Inside inner function
```

Inner functions can access variables from the enclosing scope, creating **closures** (as mentioned earlier).

#### 13.13.5 **Passing Functions as Arguments**
Because functions in Python are first-class objects, you can pass functions as arguments to other functions.

##### Example:
```python
def apply_function(func, value):
    return func(value)

def double(x):
    return x * 2

result = apply_function(double, 5)
print(result)  # Output: 10
```

#### 13.13.6 **Dynamic Function Creation (`exec()` and `eval()`)**
You can dynamically create functions or execute Python code using the `exec()` and `eval()` functions.

##### Example:
```python
code = """
def dynamic_func(x):
    return x + 5
"""

exec(code)  # This defines 'dynamic_func' dynamically
print(dynamic_func(10))  # Output: 15
```

- **`eval()`** is used to evaluate expressions, whereas **`exec()`** executes Python code dynamically.
- While powerful, these functions should be used cautiously, especially with untrusted input, as they can pose security risks.

#### 13.13.7 **Function Scoping and Variable Lifetime**
In Python, variables defined in a function are local to that function. However, you can use the **`global`** and **`nonlocal`** keywords to access variables outside the current function scope.

##### Example using `global`:
```python
x = 5

def modify_global():
    global x
    x = 10

modify_global()
print(x)  # Output: 10
```

##### Example using `nonlocal` (for nested functions):
```python
def outer():
    x = 5
    def inner():
        nonlocal x
        x = 10
    inner()
    print(x)  # Output: 10

outer()
```

#### 13.13.8 **Coroutines and `async`/`await`**
Coroutines are a powerful feature for concurrent programming in Python. They are a special type of generator that allows you to pause and resume execution, which is useful for tasks like IO-bound operations.

##### Basic Example of a Coroutine:
```python
import asyncio

async def greet():
    print("Hello")
    await asyncio.sleep(1)
    print("World!")

asyncio.run(greet())
```

- **`async def`**: Defines a coroutine.
- **`await`**: Pauses the coroutine until the awaited operation finishes (usually I/O or long-running tasks).

---

### 13.14 **Practical Function Examples**

#### 13.14.1 **Higher-Order Functions**
Higher-order functions are functions that take other functions as arguments or return functions as results.

##### Example:
```python
def apply_to_each(lst, func):
    return [func(x) for x in lst]

numbers = [1, 2, 3, 4]
squares = apply_to_each(numbers, lambda x: x**2)
print(squares)  # Output: [1, 4, 9, 16]
```

#### 13.14.2 **Memoization**
Memoization is a common technique used in dynamic programming to store the results of expensive function calls and reuse them when the same inputs occur again.

##### Example using a Dictionary for Memoization:
```python
def memoize(func):
    cache = {}
    def wrapper(n):
        if n not in cache:
            cache[n] = func(n)
        return cache[n]
    return wrapper

@memoize
def fibonacci(n):
    if n <= 1:
        return n
    return fibonacci(n-1) + fibonacci(n-2)

print(fibonacci(10))  # Output: 55
```

---

### 13.15 **Performance Considerations for Functions**
- **Function Call Overhead**: Every function call in Python has a certain overhead, and if a function is called very frequently in a tight loop, it could impact performance. In cases where performance is critical, consider optimizing the function (e.g., using built-in functions or avoiding redundant function calls).
- **Use of Built-ins**: Whenever possible, use Python's built-in functions (`map()`, `filter()`, `sum()`, etc.) instead of writing custom functions for better performance due to their internal optimization.
- **Using `functools.lru_cache`**: For functions with repeated calls, caching results using `lru_cache` can dramatically improve performance by avoiding redundant calculations.

---
 -->




<span style="display: flex; justify-content: space-between; width: 100%; align-items: center;">
    <a href="../12-module-12-program-control-flow/README.md">
        <img src="https://img.shields.io/badge/Previous-Program_Control_Flow-blue" width="250" height="35">
    </a>
    <a href="../14-module-14-project-I/README.md">
        <img src="https://img.shields.io/badge/Next-Project_I-brightgreen" width="160" height="35">
    </a>
</span>
<br><br>
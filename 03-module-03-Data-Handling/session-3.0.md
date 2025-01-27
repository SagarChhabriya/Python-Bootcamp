
## Literals


# Literals in Python

In Python, a **literal** is a fixed value that appears directly in the code. These are constant values used to represent data in a program. Python supports several types of literals that represent different data types.

### Types of Literals in Python:

1. **String Literals**:
   - A string literal is a sequence of characters enclosed in either single quotes (`'`) or double quotes (`"`).
   - Python also supports multi-line string literals using triple quotes (`'''` or `"""`).

   **Examples**:
   ```python
   single_quote_string = 'Hello, World!'
   double_quote_string = "Python Programming"
   multi_line_string = '''This is a
   multi-line string.'''
   ```

2. **Numeric Literals**:
   - Numeric literals represent numbers. Python has several types of numeric literals:
     - **Integer literals**: Whole numbers, positive or negative, without a decimal point.
     - **Float literals**: Numbers that include a decimal point.
     - **Complex literals**: Numbers with a real and imaginary part.

   **Examples**:
   ```python
   integer_literal = 10        # Integer literal
   float_literal = 10.5        # Float literal
   complex_literal = 3 + 5j    # Complex literal
   ```

3. **Boolean Literals**:
   - Boolean literals represent one of two values: `True` or `False`.
   - They are used to represent logical values in conditional expressions and control structures.

   **Examples**:
   ```python
   boolean_true = True
   boolean_false = False
   ```

4. **Special Literals**:
   - The `None` literal represents the absence of a value or a null value in Python. It is often used as a placeholder or to represent the end of a list or collection.

   **Examples**:
   ```python
   none_literal = None
   ```

5. **Collection Literals**:
   - These include lists, tuples, dictionaries, and sets.
     - **List literals** are defined with square brackets `[]`.
     - **Tuple literals** are defined with parentheses `()`.
     - **Dictionary literals** are defined with curly braces `{}`.
     - **Set literals** are also defined with curly braces `{}` (but without key-value pairs).
     
   **Examples**:
   ```python
   list_literal = [1, 2, 3, 4]            # List literal
   tuple_literal = (1, 2, 3, 4)           # Tuple literal
   dictionary_literal = {'a': 1, 'b': 2}  # Dictionary literal
   set_literal = {1, 2, 3, 4}            # Set literal
   ```

---

### Example Code Demonstrating Different Literals:

```python
# String Literals
string_literal = "Hello, World!"

# Numeric Literals
integer_literal = 100
float_literal = 45.67
complex_literal = 2 + 3j

# Boolean Literals
is_active = True
is_available = False

# Special Literal
nothing = None

# Collection Literals
list_literal = [1, 2, 3]
tuple_literal = (4, 5, 6)
dictionary_literal = {'name': 'John', 'age': 30}
set_literal = {1, 2, 3, 4}
```

### Summary:
- **String Literals**: `'Hello'`, `"World"`, `'''Multi-line'''`
- **Numeric Literals**: `10`, `3.14`, `1 + 2j`
- **Boolean Literals**: `True`, `False`
- **Special Literals**: `None`
- **Collection Literals**: `[1, 2, 3]`, `(1, 2)`, `{'key': 'value'}`, `{1, 2, 3}`

Literals are essential in representing constant values in Python programs, and understanding their types helps in writing more efficient and readable code.


This markdown content explains the different types of literals in Python and provides examples to clarify their usage.


# 3. Introduction to Data Handling
 
## 3.1 Data Types in Python

A **data type** defines the kind of data a variable can hold. In Python, you don't need to specify the type of the data explicitly. The type is assigned automatically based on the value you provide. Python is a **dynamically typed** language.

Python has the following built-in data types:

1. `int` - Integer numbers
2. `float` - Decimal numbers
3. `complex` - Complex numbers
4. `bool` - Boolean values (True or False)
5. `str` - String (text)
6. `bytes` - Immutable sequence of bytes
7. `range` - Represents a range of numbers
8. `bytearray` - Mutable sequence of bytes
9. `list` - Ordered, mutable collection of items
10. `tuple` - Ordered, immutable collection of items
11. `set` - Unordered collection of unique items
12. `frozenset` - Immutable version of set
13. `dict` - Key-value pairs
14. `None` - Represents a null or no value

> **Note**: In Python, everything is an object, including the data types.

### 1. `int` Data Type

The `int` data type represents whole numbers (integral values).

#### Example:
```python
a = 10
print(type(a))  # Output: <class 'int'>
```

> **Note**: In Python 2, there was a `long` data type for representing very large integers. In Python 3, the `int` type can handle large values, so there's no need for a separate `long` type.

### Representing `int` Values in Different Number Systems

You can represent integer values in various number systems:

1. **Decimal (Base-10)**:
   This is the default number system in Python. It includes digits from 0 to 9.
   
   ```python
   a = 10  # Decimal (base-10)
   print(a)  # Output: 10
   ```

2. **Binary (Base-2)**:
   The allowed digits are 0 and 1. Binary numbers should be prefixed with `0b` or `0B`.

   ```python
   a = 0B1111  # Binary (base-2)
   print(a)  # Output: 15

   # Error: Binary numbers can only contain 0 and 1
   # a = 0B123  # This will raise a SyntaxError

   # Error: Binary numbers need to be prefixed with 0b or 0B
   # a = b111   # This will raise a NameError
   ```

3. **Octal (Base-8)**:
   The allowed digits are 0 to 7. Octal numbers should be prefixed with `0o` or `0O`.

   ```python
   a = 0o123   # Octal (base-8)
   print(a)    # Output: 83

   # Error: Octal numbers can only contain digits from 0 to 7
   # a = 0o796  # This will raise a SyntaxError
   ```

4. **Hexadecimal (Base-16)**:
   The allowed digits are 0 to 9 and a-f (both lowercase and uppercase are allowed). Hexadecimal numbers should be prefixed with `0x` or `0X`.

   ```python
   a = 0XFACE  # Hexadecimal (base-16)
   print(a)    # Output: 64718

   # Error: Hexadecimal numbers can only contain digits 0-9 and letters a-f
   # a = 0XBeer  # This will raise a SyntaxError
   ```

### Example with All Representations:

```python
a = 10         # Decimal
b = 0o10       # Octal
c = 0x10       # Hexadecimal
d = 0b10       # Binary

print(a)  # Output: 10
print(b)  # Output: 8
print(c)  # Output: 16
print(d)  # Output: 2
```

> **Note**: Even though you can specify integer values in binary, octal, or hexadecimal form, Python will always treat them as decimal when working with the values.


## Base Conversions in Python

Python provides built-in functions for converting numbers from one base to another. These functions allow you to convert numbers from any base to binary, octal, or hexadecimal.

### 1. `bin()`
The `bin()` function converts a number from any base to binary (base-2).

#### Example:
```python
print(bin(15))        # Output: 0b1111 (Binary representation of 15)
print(bin(0o11))      # Output: 0b1011 (Binary representation of octal 11)
print(bin(0x10))      # Output: 0b10000 (Binary representation of hexadecimal 10)
```

### 2. `oct()`
The `oct()` function converts a number from any base to octal (base-8).

#### Example:
```python
print(oct(10))        # Output: 0o12 (Octal representation of 10)
print(oct(0b1111))    # Output: 0o17 (Octal representation of binary 1111)
print(oct(0x123))     # Output: 0o443 (Octal representation of hexadecimal 123)
```

### 3. `hex()`
The `hex()` function converts a number from any base to hexadecimal (base-16).

#### Example:
```python
print(hex(100))       # Output: 0x64 (Hexadecimal representation of 100)
print(hex(0b111111))  # Output: 0x3f (Hexadecimal representation of binary 111111)
print(hex(0o12345))   # Output: 0x5345 (Hexadecimal representation of octal 12345)
```

### In Short:
- **`bin()`**: Converts any number to binary.
- **`oct()`**: Converts any number to octal.
- **`hex()`**: Converts any number to hexadecimal. 

These functions are useful for converting between number systems and can be applied to numbers in decimal, binary, octal, or hexadecimal forms.


### 2. `float` Data Type

The `float` data type represents floating-point numbers, which are decimal values (values with a fractional part). 

#### Example:
```python
f = 1.234
print(type(f))  # Output: <class 'float'>
```

We can also represent floating-point numbers using **scientific notation** (exponential form), which is especially useful for large or small numbers.

#### Example:
```python
f = 1.2e3  # This is equivalent to 1.2 * 10^3, or 1200
print(f)  # Output: 1200.0

f = 2.5E4  # Equivalent to 2.5 * 10^4, or 25000
print(f)  # Output: 25000.0
```

> **Note**: While integers can be represented in decimal, binary, octal, or hexadecimal form, **floating-point values can only be represented in decimal form**.

#### Example of Invalid Floating-point Representation:
```python
f = 0B11.01  # This will raise a SyntaxError, as floating-point numbers can't be written in binary form.
```

---

### 3. `Complex` Data Type

A **complex number** has a real part and an imaginary part. It is written in the form:

```
a + bj
```

Where:
- `a` is the real part
- `b` is the imaginary part

#### Examples of Complex Numbers:
```python
a = 3 + 5j  # Real part: 3, Imaginary part: 5
b = 10 - 5.5j  # Real part: 10, Imaginary part: -5.5
c = 0.5 + 0.1j  # Real part: 0.5, Imaginary part: 0.1
```

#### Complex Number with Different Forms for Real Part:
You can use different number systems (decimal, octal, binary, hexadecimal) for the real part, but the imaginary part must always be represented in decimal form.

#### Examples:
```python
a = 0B11 + 5j  # Binary for real part, decimal for imaginary part
print(a)  # Output: (3+5j)

a = 3 + 0B11j  # Decimal for real part, binary for imaginary part (Note: imaginary part should be in decimal)
print(a)  # Output: SyntaxError: invalid syntax
```

#### Operations with Complex Numbers:
You can perform mathematical operations on complex numbers as well.

```python
a = 10 + 1.5j
b = 20 + 2.5j
c = a + b
print(c)  # Output: (30+4.0j)
print(type(c))  # Output: <class 'complex'>
```

#### Accessing Real and Imaginary Parts:
Complex numbers in Python have built-in attributes to access their real and imaginary parts.

```python
c = 10.5 + 3.6j
print(c.real)  # Output: 10.5
print(c.imag)  # Output: 3.6
```

### Applications of Complex Numbers:
Complex numbers are commonly used in fields such as:
- **Scientific computing**
- **Electrical engineering**
- **Signal processing**

They are helpful for representing phenomena involving oscillations, waveforms, and electrical circuits.


  - Static vs Dynamic Typing
  - Numbers
  - Boolean
  - Strings

- **3.2 Type Conversion**
  - Implicit and Explicit Conversion

- **3.3 Constants in Python**
  - Understanding Constants (Best practices)

- **3.4 Special Data Types**
  - `None`

- **3.5 Introduction to Python Collection/Data Structures**

  - **3.5.1 Sequences in Python**
    - Lists
    - Tuples
  
  - **3.5.2 Sets and Dictionaries**
    - Sets
    - Frozensets
    - Dictionaries
  
  - **3.5.3 Maps and Data Structures**
    - Introduction to Mapping Types

# 3.6 Working with Date and Time
- **3.6.1 Introduction to Date and Time in Python**
  - Overview of Date and Time handling in Python.
  
- **3.6.2 Date and Time Now**
  - Using the `datetime` module to get the current date and time.
  - `datetime.now()` and `datetime.today()`.
  - Difference between `datetime.now()` and `datetime.utcnow()`.

- **3.6.3 Combining Date and Time**
  - Using `datetime.combine()` to combine date and time objects.
  - Understanding the `date` and `time` classes in the `datetime` module.

- **3.6.4 Formatting Dates and Times**
  - `strftime()` and `strptime()` methods for formatting dates.
  - Common formatting codes like `%Y`, `%m`, `%d`, `%H`, `%M`, `%S`.

- **3.6.5 Finding Durations**
  - Calculating the difference between two dates/times (`timedelta`).
  - Adding and subtracting time intervals using `timedelta`.

- **3.6.6 Comparing Dates**
  - Comparing dates using comparison operators (`>`, `<`, `==`, etc.).
  - Finding the minimum and maximum dates from a list.

- **3.6.7 Sorting Dates**
  - Sorting lists of dates using Python's `sorted()` function or `sort()`.
  - Sorting a list of `datetime` objects.

- **3.6.8 Pausing Execution Temporarily**
  - Using `time.sleep()` to pause the program for a given number of seconds.
  - Practical use cases for pausing execution (e.g., for delays in network requests).

- **3.6.9 Calculating Duration of Execution**
  - Measuring the time taken for a program or function to execute.
  - Using `time.time()` or `time.perf_counter()` for performance benchmarking.

- **3.6.10 Using the Calendar Module**
  - Overview of the `calendar` module.
  - Displaying calendars for specific months and years.
  - Working with weekdays, month names, and leap years.
  - Using `calendar.month()`, `calendar.calendar()`, and `calendar.isleap()`.


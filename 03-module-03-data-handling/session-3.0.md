
# 3. Introduction to Data Handling

<span style="display: flex; justify-content: space-between; width: 100%; align-items: center;">
    <a href="../02-module-02-python-fundamentals/README.md">
        <img src="https://img.shields.io/badge/Previous-Python_Fundamentals-blue" width="250" height="35">
    </a>
    <a href="../04-module-04-operators/README.md">
        <img src="https://img.shields.io/badge/Next-Operators-brightgreen" width="170" height="35">
    </a>
</span>
<br><br>


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


### Python 2 `long` Data Type

In Python 2, there was a `long` data type for very large integers. However, in Python 3, `long` has been removed, and large integers are represented using the `int` type.


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

### 4. `bool` Data Type

The `bool` data type is used to represent **Boolean values**. The only allowed values for this data type are `True` and `False`.

Internally, Python represents:
- `True` as 1
- `False` as 0

#### Example:
```python
b = True
print(type(b))  # Output: <class 'bool'>
```

#### Using Boolean Expressions:
You can also use Boolean values in expressions to check conditions.

```python
a = 10
b = 20
c = a < b  # This is a comparison, which returns a Boolean value
print(c)  # Output: True
```

#### Arithmetic with Booleans:
Since `True` is 1 and `False` is 0 internally, you can perform arithmetic operations on them.

```python
print(True + True)  # Output: 2
print(True - False)  # Output: 1
```

---

### 5. `str` Data Type

The `str` data type represents **string values** (a sequence of characters). Strings can be enclosed in single quotes (`'`) or double quotes (`"`).

#### Examples:
```python
name = "Sagar"
print(name)  # Output: Sagar

name = 'Sagar'
print(name)  # Output: Sagar
```

#### Multi-line Strings:
To represent multi-line strings, you can use **triple quotes** (`'''` or `"""`).

#### Example:
```python
name = '''Sagar
Chhabriya'''
print(name)
# Output:
# Sagar
# Chhabriya

name = """Sagar
Chhabriya"""
print(name)
# Output:
# Sagar
# Chhabriya
```

You can also use triple quotes to embed quotes within the string.

#### Example:
```python
name = '''This is "a" character'''
print(name)  # Output: This is "a" character

name = 'This is "character"'
print(name)  # Output: This is "character"
```

---

### Python String Slicing

String slicing in Python allows you to extract a part of a string using a **start index** and an **end index**. The general syntax for slicing is:

```python
string[start:end]
```

Where:
- `start`: The index from where the slice starts (inclusive).
- `end`: The index where the slice ends (exclusive).

### Examples:

1. **Basic Slicing**:
   Get characters from position 2 to position 5 (not included):
   ```python
   b = "Hello, World!"
   print(b[2:5])  # Output: "llo"
   ```

2. **Slice From the Start**:
   If the `start` index is omitted, it defaults to the beginning of the string:
   ```python
   b = "Hello, World!"
   print(b[:5])  # Output: "Hello"
   ```

3. **Slice To the End**:
   If the `end` index is omitted, it defaults to the end of the string:
   ```python
   b = "Hello, World!"
   print(b[2:])  # Output: "llo, World!"
   ```

4. **Negative Indexing**:
   You can use negative indices to slice from the end of the string. For example:
   ```python
   b = "Hello, World!"
   print(b[-5:-2])  # Output: "orl"
   ```

   - `-1` refers to the last character, `-2` is the second-last, and so on.

### Exercise: What will the result of the following code be?
```python
x = 'Welcome'
print(x[3:5])
```
Answer: `"co"`

This is because the slice starts at index 3 (which is `'c'`) and ends just before index 5 (which is `'o'`).

In Python, strings are **zero-indexed**, meaning the first character has index 0. You can use slicing (`[]`) to access parts of a string. 

- **Positive Indexing**: Counts from left to right.
- **Negative Indexing**: Counts from right to left.

#### Example:
```python
name = "sagar"
print(name[0])  # Output: s (first character)
print(name[1])  # Output: a (second character)
print(name[-1])  # Output: r (last character)

# Slicing to get a substring
print(name[1:4])  # Output: aga (characters from index 1 to 3)

# Slicing to get from the start to index 4
print(name[:4])  # Output: sag

# Slicing to get from index 1 to the end
print(name[1:])  # Output: agar

# Repeating a string
print(name * 3)  # Output: sagarsagarsagar

# Length of the string
print(len(name))  # Output: 5
```

> **Note**: In Python, the following data types are considered fundamental data types:
- `int`
- `float`
- `complex`
- `bool`
- `str`

---

### Characters as Strings

In Python, there is no separate `char` data type. Characters are simply **strings of length 1**.

#### Example:
```python
text = 'a'
print(type(text))  # Output: <class 'str'>
```

---
### Modify Strings in Python

| Method                        | Description and Example Code                                                                                          | Output                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------|------------------------------|
| **Upper Case (`upper()`)**     | Converts all characters in a string to uppercase. <br>`a = "Hello, World!"`<br>`print(a.upper())`                    | "HELLO, WORLD!"              |
| **Lower Case (`lower()`)**     | Converts all characters in a string to lowercase.<br>`a = "Hello, World!"`<br>`print(a.lower())`                    | "hello, world!"              |
| **Remove Whitespace (`strip()`)** | Removes leading and trailing whitespace (spaces, tabs, etc.).<br>`a = " Hello, World! "`<br>`print(a.strip())`       | "Hello, World!"              |
| **Replace String (`replace()`)** | Replaces a substring in the string with another substring.<br>`a = "Hello, World!"`<br>`print(a.replace("H", "J"))`  | "Jello, World!"              |
| **Split String (`split()`)**   | Splits the string at the specified separator and returns a list of substrings.<br>`a = "Hello, World!"`<br>`print(a.split(","))` | `['Hello', ' World!']`       |
| **String Concatenation (`+`)** | Combines two or more strings into a single string.<br>`a = "Hello"`<br>`b = "World"`<br>`c = a + b`<br>`print(c)`    | "HelloWorld"                 |
|                               | Add a space between the strings.<br>`c = a + " " + b`<br>`print(c)`                                                   | "Hello World"                |

---

In Python, string formatting allows you to insert variables or expressions into a string in a clean and readable way. Python offers multiple ways to format strings, such as using **f-strings** and the **`format()`** method.

### F-Strings (introduced in Python 3.6)
F-strings provide an easy and readable way to embed expressions inside string literals. You simply prepend the string with an `f` and use curly braces `{}` to insert variables or expressions.

#### Example with F-Strings:
```python
age = 36
txt = f"My name is John, I am {age}"
print(txt)  # Output: My name is John, I am 36
```

### Using Modifiers for Formatting
You can also format numbers or expressions inside the f-string using modifiers. For example, to format a number with two decimal places, use `:.2f`.

#### Example with a Modifier:
```python
price = 59
txt = f"The price is {price:.2f} dollars"
print(txt)  # Output: The price is 59.00 dollars
```

You can perform math operations directly inside the placeholders as well.

#### Example with Math Operations:
```python
txt = f"The price is {20 * 59} dollars"
print(txt)  # Output: The price is 1180 dollars
```

In Python, an **escape character** is used to insert special characters into strings that would otherwise be difficult or impossible to include, such as quotes or newline characters.

### Escape Character
An escape character is a backslash `\` followed by the character you want to insert. Here's how you can use escape characters in Python:

### Example of Using Escape Character:
If you want to include double quotes inside a string that is already surrounded by double quotes, you can use the escape character `\"`.

```python
txt = "We are the so-called \"Vikings\" from the north."
print(txt)
# Output: We are the so-called "Vikings" from the north.
```

### Other Escape Characters in Python:
- `\'`: Single Quote
- `\\`: Backslash
- `\n`: New Line
- `\r`: Carriage Return
- `\t`: Tab
- `\b`: Backspace
- `\f`: Form Feed
- `\ooo`: Octal value
- `\xhh`: Hex value

### Example of Using a Newline and Tab:
```python
txt = "Hello\nWorld!\tThis is Python."
print(txt)
# Output:
# Hello
# World!    This is Python.
```

This will print:
- "Hello" on one line,
- "World!" on the next line,
- and "This is Python." with a tab space before it.



# String Methods 

| **No.** | **Method**        | **Description**                                                      | **Example**                                                |
|--------|-------------------|----------------------------------------------------------------------|------------------------------------------------------------|
| 1      | `capitalize()`     | Converts the first character to uppercase.                            | `"hello".capitalize()` -> `"Hello"`                         |
| 2      | `casefold()`       | Converts the entire string to lowercase.                              | `"HELLO".casefold()` -> `"hello"`                           |
| 3      | `center()`         | Centers the string within a specified width, padding with spaces.     | `"hello".center(10, "*")` -> `"**hello***"`                 |
| 4      | `count()`          | Counts the occurrences of a substring.                               | `"hello world".count("o")` -> `2`                           |
| 5      | `encode()`         | Returns an encoded version of the string.                            | `"hello".encode()` -> `b'hello'`                            |
| 6      | `endswith()`       | Returns `True` if the string ends with the specified value.           | `"hello".endswith("lo")` -> `True`                          |
| 7      | `expandtabs()`     | Sets the tab size of the string.                                      | `"hello\tworld".expandtabs(4)` -> `"hello   world"`         |
| 8      | `find()`           | Finds the first occurrence of a substring. Returns `-1` if not found. | `"hello world".find("world")` -> `6`                        |
| 9      | `format()`         | Formats specified values in a string.                                | `"Hello {}".format("world")` -> `"Hello world"`            |
| 10     | `format_map()`     | Similar to `format()`, but uses a mapping (e.g., dictionary).         | `"Hello {name}".format_map({"name": "Alice"})` -> `"Hello Alice"` |
| 11     | `index()`          | Similar to `find()`, but raises an error if the substring is not found. | `"hello world".index("world")` -> `6`                      |
| 12     | `isalnum()`        | Returns `True` if all characters in the string are alphanumeric.     | `"hello123".isalnum()` -> `True`                            |
| 13     | `isalpha()`        | Returns `True` if all characters in the string are alphabetic.       | `"hello".isalpha()` -> `True`                               |
| 14     | `isascii()`        | Returns `True` if all characters in the string are ASCII characters. | `"hello".isascii()` -> `True`                               |
| 15     | `isdecimal()`      | Returns `True` if all characters in the string are decimals.         | `"12345".isdecimal()` -> `True`                             |
| 16     | `isdigit()`        | Returns `True` if all characters in the string are digits.           | `"12345".isdigit()` -> `True`                               |
| 17     | `isidentifier()`   | Returns `True` if the string is a valid identifier.                   | `"myVar".isidentifier()` -> `True`                          |
| 18     | `islower()`        | Returns `True` if all characters in the string are lowercase.        | `"hello".islower()` -> `True`                               |
| 19     | `isnumeric()`      | Returns `True` if all characters in the string are numeric.          | `"12345".isnumeric()` -> `True`                             |
| 20     | `isprintable()`    | Returns `True` if all characters in the string are printable.        | `"hello".isprintable()` -> `True`                           |
| 21     | `isspace()`        | Returns `True` if all characters in the string are whitespaces.      | `"   ".isspace()` -> `True`                                 |
| 22     | `istitle()`        | Returns `True` if the string is in title case.                       | `"Hello World".istitle()` -> `True`                         |
| 23     | `isupper()`        | Returns `True` if all characters in the string are uppercase.        | `"HELLO".isupper()` -> `True`                               |
| 24     | `join()`           | Joins elements of an iterable into a string.                         | `" ".join(['hello', 'world'])` -> `"hello world"`           |
| 25     | `ljust()`          | Returns a left justified version of the string.                      | `"hello".ljust(10, "-")` -> `"hello-----"`                  |
| 26     | `lower()`          | Converts all characters to lowercase.                                | `"HELLO".lower()` -> `"hello"`                              |
| 27     | `lstrip()`         | Returns a left trim version of the string.                           | `"   hello".lstrip()` -> `"hello"`                          |
| 28     | `maketrans()`      | Returns a translation table to be used in translations.              | `str.maketrans("abc", "123")` -> `{97: 49, 98: 50, 99: 51}` |
| 29     | `partition()`      | Returns a tuple where the string is parted into three parts.        | `"hello world".partition(" ")` -> `('hello', ' ', 'world')` |
| 30     | `replace()`        | Replaces a specified substring with another string.                 | `"hello world".replace("world", "Python")` -> `"hello Python"` |
| 31     | `rfind()`          | Finds the last occurrence of a substring. Returns `-1` if not found. | `"hello world".rfind("o")` -> `7`                           |
| 32     | `rindex()`         | Similar to `rfind()`, but raises an error if the substring is not found. | `"hello world".rindex("o")` -> `7`                         |
| 33     | `rjust()`          | Returns a right justified version of the string.                     | `"hello".rjust(10, "-")` -> `"-----hello"`                  |
| 34     | `rpartition()`     | Returns a tuple where the string is parted into three parts from the right. | `"hello world".rpartition(" ")` -> `('hello', ' ', 'world')` |
| 35     | `rsplit()`         | Splits the string at the specified separator from the right.        | `"hello world".rsplit()` -> `['hello', 'world']`           |
| 36     | `rstrip()`         | Returns a right trim version of the string.                         | `"hello   ".rstrip()` -> `"hello"`                          |
| 37     | `split()`          | Splits the string at the specified separator.                       | `"hello world".split()` -> `['hello', 'world']`             |
| 38     | `splitlines()`     | Splits the string at line breaks and returns a list.                | `"hello\nworld".splitlines()` -> `['hello', 'world']`       |
| 39     | `startswith()`     | Returns `True` if the string starts with the specified value.       | `"hello".startswith("he")` -> `True`                        |
| 40     | `strip()`          | Returns a trimmed version of the string.                            | `"   hello   ".strip()` -> `"hello"`                        |
| 41     | `swapcase()`       | Swaps the case of the string (lowercase to uppercase and vice versa). | `"Hello".swapcase()` -> `"hELLO"`                         |
| 42     | `title()`          | Converts the first character of each word to uppercase.             | `"hello world".title()` -> `"Hello World"`                  |
| 43     | `translate()`      | Translates characters using a translation table.                    | `"hello".translate(str.maketrans("aeiou", "12345"))` -> `"h2ll4"` |
| 44     | `upper()`          | Converts all characters to uppercase.                               | `"hello".upper()` -> `"HELLO"`                              |
| 45     | `zfill()`          | Fills the string with a specified number of `0` values at the beginning. | `"42".zfill(5)` -> `"00042"`                              |



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


### Static Typing vs Dynamic Typing in Python:

**1. Dynamic Typing** (Python's default behavior):

In Python, you don't declare the types of variables. The interpreter figures out the type at runtime.

```python
x = 10    # x is an integer
print(type(x))  # <class 'int'>

x = "Hello"  # x is now a string
print(type(x))  # <class 'str'>
```

- Python determines that `x` is an integer first and later a string at runtime.
- **Dynamic Typing**: Types are not explicitly declared, and can change at runtime.

**2. Static Typing (not native to Python but can be enforced with type hints)**:

Python is dynamically typed by default, but you can use **type hints** to suggest the type of a variable. This doesn't enforce the type at runtime, but it can be used by tools like linters or IDEs for better static analysis.

```python
def greet(name: str) -> str:
    return "Hello " + name

int x = 10   # can be written ---> x: int = 10
x = "Hello"  # This will not raise an error at runtime, but linters will warn about it
```

- Python doesn't enforce the type at runtime, but you can specify types with **type hints**.
- **Static Typing**: Type hints in Python can suggest types, but they are not enforced during execution.

- **Dynamic Typing**: Variables can change types at runtime, as Python doesn't enforce strict type rules.
- **Static Typing**: Can be suggested via type hints, but it isn't enforced at runtime.

<!-- Static vs Dynamic Binding -->
   
[Click Here For Exercises on 3.1 Data Types in Python](exercises.md#31-data-types-in-python)


# 3.2 Type Conversion in Python

In Python, we can convert values from one type to another. This process is called **Typecasting** or **Type Coercion**. Python provides several built-in functions to perform type conversion.

## Built-in Type Conversion Functions:

1. `int()`
2. `float()`
3. `complex()`
4. `bool()`
5. `str()`

---

### 1. `int()`
The `int()` function is used to convert a value to an integer.

**Examples:**

```python
int(123.987)      # Converts float to int: 123
int(True)         # Converts boolean True to int: 1
int(False)        # Converts boolean False to int: 0
int("10")         # Converts string "10" to int: 10
```

**Important Notes:**
- You cannot convert a **complex** type to an integer.
- When converting a **string** to an integer, the string must only contain digits (integral values). It should be in base-10.

**Invalid examples:**
```python
int(10+5j)         # TypeError: can't convert complex to int
int("10.3")        # ValueError: invalid literal for int() with base 10: '10.3'
int("ten")         # ValueError
```

---

### 2. `float()`
The `float()` function is used to convert a value to a floating-point number.

**Examples:**

```python
float(10)          # Converts int 10 to float: 10.0
float(True)        # Converts boolean True to float: 1.0
float("10")        # Converts string "10" to float: 10.0
float("10.3")      # Converts string "10.3" to float: 10.3
```

**Important Notes:**
- You cannot convert a **complex** type to a float.
- When converting a **string** to a float, the string must be either an integral or floating-point number in base-10.

**Invalid examples:**
```python
float(10+5j)       # TypeError
float("ten")       # ValueError
float("0B1111")    # ValueError
```

---

### 3. `complex()`
The `complex()` function is used to convert values to a complex number.

#### Form 1: `complex(x)`
Converts `x` to a complex number where `x` is the real part and the imaginary part is `0`.

**Examples:**

```python
complex(10)        # Converts 10 to complex: 10 + 0j
complex(10.5)      # Converts 10.5 to complex: 10.5 + 0j
complex(True)      # Converts True to complex: 1 + 0j
```

#### Form 2: `complex(x, y)`
Converts `x` to the real part and `y` to the imaginary part of the complex number.

**Examples:**

```python
complex(10, -6)    # Converts to complex: 10 - 6j
complex(True, False)  # Converts to complex: 1 + 0j
```

**Invalid example:**
```python
complex("ten")     # ValueError
```

---

### 4. `bool()`
The `bool()` function is used to convert a value to a boolean (`True` or `False`).

**Examples:**

```python
bool(0)            # Converts int 0 to False
bool(1)            # Converts int 1 to True
bool(10)           # Converts int 10 to True
bool(4.4)          # Converts float 4.4 to True
bool(0.0)          # Converts float 0.0 to False
bool(10-3j)        # Converts complex number to True
bool("True")       # Converts non-empty string to True
bool("")           # Converts empty string to False
```

**Important Notes:**
- **For int**: `0` is `False`, any non-zero integer is `True`.
- **For float**: `0.0` is `False`, any non-zero float is `True`.
- **For complex**: `0+0j` is `False`, any non-zero complex number is `True`.
- **For string**: An empty string `""` is `False`, and any non-empty string is `True`.

---

### 5. `str()`
The `str()` function is used to convert a value to a string.

**Examples:**

```python
str(10)            # Converts int 10 to string: "10"
str(10.5)          # Converts float 10.5 to string: "10.5"
str(10+4j)         # Converts complex number to string: "(10+4j)"
str(True)          # Converts boolean True to string: "True"
```

---

- **Typecasting** allows you to convert values from one type to another using functions like `int()`, `float()`, `complex()`, `bool()`, and `str()`.
- Keep in mind the rules for each conversion function, as some conversions may result in errors if the values are incompatible.

---



  - Implicit and Explicit Conversion

[Click Here For Exercises on 3.2 Type Conversion in Python](exercises.md#32-type-conversion-in-python)

# 3.3 Constants in Python


- **Definition**:  
  Constants are variables whose values are not intended to change during the execution of a program. They represent fixed values that remain consistent throughout the code.

- **Naming Convention**:  
  - Use **UPPERCASE** letters for constant names to distinguish them from regular variables.  
  - Separate words with underscores (`_`) for readability.  
  - Example: `MAX_SPEED`, `PI`, `DEFAULT_TIMEOUT`.

- **Best Practices**:
  1. **Immutability**:  
     - Although Python does not enforce immutability for constants, treat them as read-only after definition.  
     - Avoid reassigning values to constants.

  2. **Placement**:  
     - Define constants at the top of a module or script for easy visibility and maintenance.  
     - Group related constants together for better organization.

  3. **Documentation**:  
     - Add comments or docstrings to explain the purpose and usage of constants.  
     - Example:  
       ```python
       # Maximum allowed speed in the application
       MAX_SPEED = 100
       ```

  4. **Avoid Magic Numbers**:  
     - Replace hard-coded values (magic numbers) with named constants to improve code readability and maintainability.  
     - Example:  
       ```python
       # Instead of:
       area = 3.14 * radius ** 2

       # Use:
       PI = 3.14
       area = PI * radius ** 2
       ```

  5. **Module-Level Constants**:  
     - For larger projects, store constants in a separate module (e.g., `constants.py`) and import them as needed.  
     - Example:  
       ```python
       # constants.py
       PI = 3.14159
       GRAVITY = 9.81

       # main.py
       from constants import PI, GRAVITY
       ```

- **Limitations in Python**:  
  - Python does not have built-in support for true constants (unlike some other languages).  
  - Developers must rely on conventions and discipline to enforce constant behavior.

---

[Click Here For Exercises on 3.3 Constants in Python](exercises.md#33-constants-in-python)

# 3.4 Special Data Types

## `None`

In Python, `None` is a special data type that represents the absence of a value or a null value. It is often used to signify that a variable or an object does not hold any meaningful value.

### Key Points:

- **Type**: `None` is a unique object in Python and its own data type. It is the sole instance of the `NoneType` class.
  ```python
  type(None)  # <class 'NoneType'>
  ```

- **Common Uses**:
  1. **Default function return value**: If a function does not explicitly return a value, it returns `None` by default.
     ```python
     def no_return():
         pass
     
     result = no_return()
     print(result)  # Output: None
     ```
  2. **Placeholder**: `None` is often used as a placeholder or a sentinel value, representing "nothing" or "no value."
     ```python
     my_var = None  # Placeholder for a variable that will later be assigned a value
     ```

  3. **Comparison**: `None` is commonly used for comparisons to check whether a variable has been initialized or contains a valid value.
     ```python
     if my_var is None:
         print("my_var has no value assigned")
     ```

  4. **Indicating absence**: `None` can be used to indicate the absence of a return value or when a function parameter has no meaningful default value.
     ```python
     def find_element(lst, value=None):
         if value is None:
             return "Value not provided"
         if value in lst:
             return lst.index(value)
         return -1
     ```

### Characteristics:
- **Singleton**: There is only one instance of `None` in a Python program, making it a singleton object.
- **Identity**: `None` is often checked using the `is` operator, not `==`, because it is a unique singleton object.
  ```python
  a = None
  b = None
  print(a is b)  # Output: True
  ```

- **Falsy Value**: In Python, `None` is considered a "falsy" value, meaning it evaluates to `False` in boolean contexts.
  ```python
  if not None:
      print("None is considered False")  # This will print
  ```

### Example Usage:

```python
# Example 1: Function returning None
def check_number(number):
    if number < 0:
        return None  # Indicating no valid number
    return number * 2

result = check_number(-5)
if result is None:
    print("Invalid number provided.")  # This will print

# Example 2: Using None as a placeholder
default_value = None
if default_value is None:
    print("No default value assigned yet.")  # This will print
```

[Click Here For Exercsies on 3.4 Special Data Types](exercises.md#34-special-data-types)

# 3.5 Introduction to Python Collection/Data Structures

Python provides several built-in collection types to store multiple items in a single variable. These collections are essential for managing large sets of data and provide a variety of operations to manipulate them.

## 3.5.1 Sequences in Python

Sequences are ordered collections of items. Python has two main types of sequences: **Lists** and **Tuples**.

### Lists
- **Definition**: A list is a mutable, ordered collection of items. It allows duplicate values.
- **Syntax**: Lists are defined using square brackets `[]`.
  ```python
  my_list = [1, 2, 3, 4, 5]
  ```
- **Key Operations**:
  - Indexing and slicing: `my_list[0]` (access the first element)
  - Appending: `my_list.append(6)`
  - Insertion: `my_list.insert(2, 'new')`
  - Deletion: `del my_list[1]`
  - List comprehension: `[x*2 for x in my_list]`

  Example:
  ```python
  my_list = [1, 2, 3]
  my_list.append(4)  # [1, 2, 3, 4]
  ```

### Tuples
- **Definition**: A tuple is an immutable, ordered collection of items. Like lists, tuples can contain multiple items, but once created, their elements cannot be modified.
- **Syntax**: Tuples are defined using parentheses `()`.
  ```python
  my_tuple = (1, 2, 3, 4, 5)
  ```
- **Key Operations**:
  - Indexing and slicing: `my_tuple[0]`
  - Concatenation: `tuple1 + tuple2`
  - Tuple unpacking: `a, b, c = my_tuple`

  Example:
  ```python
  my_tuple = (1, 2, 3)
  print(my_tuple[0])  # Output: 1
  ```

---

## 3.5.2 Sets and Dictionaries

### Sets
- **Definition**: A set is an unordered collection of unique items. Sets do not allow duplicate elements and do not guarantee any specific order.
- **Syntax**: Sets are defined using curly braces `{}` or the `set()` constructor.
  ```python
  my_set = {1, 2, 3, 4}
  ```
- **Key Operations**:
  - Adding elements: `my_set.add(5)`
  - Removing elements: `my_set.remove(3)`
  - Set operations: Union (`my_set | another_set`), Intersection (`my_set & another_set`)

  Example:
  ```python
  my_set = {1, 2, 3}
  my_set.add(4)
  print(my_set)  # Output: {1, 2, 3, 4}
  ```

### Frozensets
- **Definition**: A frozenset is an immutable version of a set. Once created, frozensets cannot be modified (no adding or removing elements).
- **Syntax**: Frozensets are created using the `frozenset()` constructor.
  ```python
  my_frozenset = frozenset([1, 2, 3])
  ```

  Example:
  ```python
  my_frozenset = frozenset([1, 2, 3])
  print(my_frozenset)  # Output: frozenset({1, 2, 3})
  ```

### Dictionaries
- **Definition**: A dictionary is an unordered collection of key-value pairs. Each key is unique and maps to a value.
- **Syntax**: Dictionaries are defined using curly braces `{}` with key-value pairs separated by a colon `:`.
  ```python
  my_dict = {"name": "Alice", "age": 25}
  ```
- **Key Operations**:
  - Accessing values: `my_dict["name"]`
  - Adding/updating items: `my_dict["address"] = "New York"`
  - Deleting items: `del my_dict["age"]`
  - Dictionary comprehension: `{key: value for key, value in iterable}`

  Example:
  ```python
  my_dict = {"name": "Alice", "age": 25}
  my_dict["city"] = "London"
  print(my_dict)  # Output: {"name": "Alice", "age": 25, "city": "London"}
  ```

---

## 3.5.3 Maps and Data Structures

### Introduction to Mapping Types
- **Mapping types** in Python are data structures that store key-value pairs, and the most common mapping type is the **dictionary**. However, mapping types can also be extended using classes or specialized types like `defaultdict` from the `collections` module.
  
  - **defaultdict**: A subclass of the dictionary, which provides a default value for nonexistent keys.
    ```python
    from collections import defaultdict
    my_defaultdict = defaultdict(int)
    my_defaultdict["key"] += 1
    print(my_defaultdict)  # Output: defaultdict(<class 'int'>, {'key': 1})
    ```

- **Use cases**:
  - **Dictionaries** are ideal for when you need a flexible mapping of data where you associate unique keys with values.
  - **defaultdict** is useful when you want to avoid key errors and provide default values when a key is accessed that doesn't exist.

### Summary of Collection Types:
- **Lists**: Ordered, mutable collections.
- **Tuples**: Ordered, immutable collections.
- **Sets**: Unordered collections with no duplicate items.
- **Frozensets**: Immutable sets.
- **Dictionaries**: Unordered collections of key-value pairs.
- **Mapping Types**: Specialized data structures like dictionaries or `defaultdict` to map keys to values.

---





# 3.6 Working with Date and Time

Handling date and time in Python is essential for many types of programs, including those that involve scheduling, event logging, or time-based data. Python provides a variety of modules and functions to work with date and time efficiently.

## 3.6.1 Introduction to Date and Time in Python
Python provides several modules for working with dates and times, such as:
- **`datetime` module**: Used for handling both date and time in a more complex and flexible manner.
- **`time` module**: Provides time-related functions like sleeping, measuring execution time, etc.
- **`calendar` module**: Offers functionality for working with calendars.

These modules allow you to manipulate dates and times, format them, calculate durations, and much more.

---

## 3.6.2 Date and Time Now

### Using the `datetime` module to get the current date and time:
The `datetime` module provides multiple ways to get the current date and time.

- **`datetime.now()`**: Returns the current local date and time.
  ```python
  from datetime import datetime
  now = datetime.now()
  print(now)  # Example Output: 2025-01-29 15:45:12.123456
  ```

- **`datetime.today()`**: Returns the current local date and time (same as `datetime.now()`).
  ```python
  today = datetime.today()
  print(today)  # Example Output: 2025-01-29 15:45:12.123456
  ```

- **`datetime.utcnow()`**: Returns the current UTC (Coordinated Universal Time) date and time, useful for time zone differences.
  ```python
  utc_now = datetime.utcnow()
  print(utc_now)  # Example Output: 2025-01-29 20:45:12.123456
  ```

### Difference between `datetime.now()` and `datetime.utcnow()`:
- `datetime.now()` returns the current local time, considering your system's time zone.
- `datetime.utcnow()` returns the current time in UTC, which is independent of local time zones.

[Click Here to Read Detailed Notes on Difference between `datetime.now()` and `datetime.utcnow()](MISC.md#1-datetimenow)

---

## 3.6.3 Combining Date and Time

You can combine separate date and time objects into one `datetime` object using `datetime.combine()`.

### Using `datetime.combine()`:
- Combines a `date` object and a `time` object into a single `datetime` object.
  ```python
  from datetime import date, time, datetime
  d = date(2025, 1, 29)
  t = time(15, 45)
  combined = datetime.combine(d, t)
  print(combined)  # Output: 2025-01-29 15:45:00
  ```

### `date` and `time` classes in the `datetime` module:
- **`date` class**: Represents a date (year, month, day).
  ```python
  d = date(2025, 1, 29)
  print(d)  # Output: 2025-01-29
  ```

- **`time` class**: Represents time (hour, minute, second, microsecond).
  ```python
  t = time(15, 45)
  print(t)  # Output: 15:45:00
  ```

---

## 3.6.4 Formatting Dates and Times

Python provides two key methods for formatting and parsing date/time strings:

- **`strftime()`**: Formats `datetime` objects as strings.
- **`strptime()`**: Parses strings into `datetime` objects.

### Common formatting codes:
- `%Y`: Year with century (e.g., `2025`)
- `%m`: Month as a zero-padded decimal number (e.g., `01` to `12`)
- `%d`: Day of the month as a zero-padded decimal number (e.g., `01` to `31`)
- `%H`: Hour (24-hour clock) as a zero-padded decimal number (e.g., `00` to `23`)
- `%M`: Minute as a zero-padded decimal number (e.g., `00` to `59`)
- `%S`: Second as a zero-padded decimal number (e.g., `00` to `59`)

### Example:
```python
now = datetime.now()
formatted = now.strftime("%Y-%m-%d %H:%M:%S")
print(formatted)  # Output: 2025-01-29 15:45:12
```

### Parsing a date string:
```python
date_string = "2025-01-29 15:45:12"
parsed_date = datetime.strptime(date_string, "%Y-%m-%d %H:%M:%S")
print(parsed_date)  # Output: 2025-01-29 15:45:12
```

---

## 3.6.5 Finding Durations

The `timedelta` class from the `datetime` module allows for calculating the difference between two dates or times and performing arithmetic operations on them.

### Calculating the difference:
```python
from datetime import datetime, timedelta
date1 = datetime(2025, 1, 1)
date2 = datetime.now()
date3 = date2 - date1
print(date3)  # Output: 28 days, 15:45:12.123456

# Tip: print(type(date3))

```

## Difference between two timedelta objects

```python
from datetime import timedelta

t1 = timedelta(weeks = 2, days = 5, hours = 1, seconds = 33)
t2 = timedelta(days = 4, hours = 11, minutes = 4, seconds = 54)

t3 = t1 - t2

print("t3 =", t3)
# Tip: print(type(t3))

```

### Adding and subtracting time intervals:
```python
# Adding 5 days
new_date = date1 + timedelta(days=5)
print(new_date)  # Output: 2025-01-06

# Subtracting 2 hours
new_time = datetime.now() - timedelta(hours=2)
print(new_time)  # Output: 2025-01-29 13:45:12.123456
```

---

## 3.6.6 Comparing Dates

Python allows comparing dates and times directly using comparison operators.

### Example:
```python
date1 = datetime(2025, 1, 1)
date2 = datetime.now()

print(date1 > date2)  # Output: False
print(date1 < date2)  # Output: True
print(date1 == date2)  # Output: False
```

### Finding the minimum and maximum dates:
```python
dates = [datetime(2025, 1, 1), datetime(2024, 12, 31), datetime(2025, 2, 1)]
print(min(dates))  # Output: 2024-12-31 00:00:00
print(max(dates))  # Output: 2025-02-01 00:00:00
```

---

## 3.6.7 Sorting Dates

Python's `sorted()` function can be used to sort lists of `datetime` objects.

### Sorting a list of `datetime` objects:
```python
dates = [datetime(2025, 1, 1), datetime(2024, 12, 31), datetime(2025, 2, 1)]
sorted_dates = sorted(dates)
print(sorted_dates)  # Output: [datetime(2024, 12, 31), datetime(2025, 1, 1), datetime(2025, 2, 1)]
```

---

## 3.6.8 Pausing Execution Temporarily

You can pause the execution of your program for a specific duration using the `time.sleep()` function.

### Example:
```python
import time
print("Start")
time.sleep(3)  # Pauses execution for 3 seconds
print("End")  # This will print after 3 seconds
```

### Practical use cases:
- Introducing delays in network requests.
- Waiting for a specific time interval before repeating a task.

---

## 3.6.9 Calculating Duration of Execution

You can measure the time taken by a program or function using the `time.time()` or `time.perf_counter()` functions.

### Example with `time.time()`:
```python
import time
start_time = time.time()

# Code to measure
time.sleep(2)

end_time = time.time()
print(f"Execution time: {end_time - start_time} seconds")  # Output: Execution time: 2.0xxx seconds
```

---

## 3.6.10 Using the Calendar Module

The `calendar` module allows you to work with calendars, month names, and weekdays.

### Displaying calendars:
- **`calendar.month(year, month)`**: Displays the calendar for a specific month.
- **`calendar.calendar(year)`**: Displays the calendar for a specific year.

### Example:
```python
import calendar
print(calendar.month(2025, 1))  # Displays the calendar for January 2025
```

### Working with weekdays and leap years:
- **`calendar.weekday(year, month, day)`**: Returns the weekday as an integer (0 = Monday, 6 = Sunday).
  ```python
  print(calendar.weekday(2025, 1, 29))  # Output: 2 (Wednesday)
  ```

- **`calendar.isleap(year)`**: Returns `True` if the year is a leap year, otherwise `False`.
  ```python
  print(calendar.isleap(2024))  # Output: True
  ```

[Click Here For Exercises on 3.6 Working with Date and Time](exercises.md#361-introduction-to-date-and-time-in-python)


<span style="display: flex; justify-content: space-between; width: 100%; align-items: center;">
    <a href="../02-module-02-python-fundamentals/README.md">
        <img src="https://img.shields.io/badge/Previous-Python_Fundamentals-blue" width="250" height="35">
    </a>
    <a href="../04-module-04-operators/README.md">
        <img src="https://img.shields.io/badge/Next-Operators-brightgreen" width="170" height="35">
    </a>
</span>
<br><br>

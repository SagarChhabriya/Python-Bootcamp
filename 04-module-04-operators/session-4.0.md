# 4. Operators

<span style="display: flex; justify-content: space-between; width: 100%; align-items: center;">
    <a href="../03-module-03-data-handling/README.md">
        <img src="https://img.shields.io/badge/Previous-Data_Handling-blue" width="250" height="35">
    </a>
    <a href="../05-module-05-debugging/README.md">
        <img src="https://img.shields.io/badge/Next-Debugging-brightgreen" width="200" height="35">
    </a>
</span>
<br><br>
 
## 4.1 Arithmetic Operators

Arithmetic operators are used to perform mathematical operations between numeric values.

| Operator | Description                | Example               | Output  |
|----------|----------------------------|-----------------------|---------|
| `+`      | Addition                   | `5 + 3`               | `8`     |
| `-`      | Subtraction                | `5 - 3`               | `2`     |
| `*`      | Multiplication             | `5 * 3`               | `15`    |
| `/`      | Division (float result)    | `5 / 2`               | `2.5`   |
| `//`     | Floor Division             | `5 // 2`              | `2`     |
| `%`      | Modulo (remainder)         | `5 % 2`               | `1`     |
| `**`     | Exponentiation (power)     | `5 ** 2`              | `25`    |

---



### Examples:

```python
a = 10
b = 2

print("a + b ", a + b)  # Addition: a + b = 12
print("a - b ", a - b)  # Subtraction: a - b = 8
print("a * b ", a * b)  # Multiplication: a * b = 20
print("a / b ", a / b)  # Division (Floating point): a / b = 5.0
print("a // b ", a // b)  # Floor Division: a // b = 5
print("a % b", a % b)  # Modulo (Remainder): a % b = 0
print("a ** b", a ** b)  # Exponentiation: a ** b = 100

print(10/2)   # Floating point division: 10/2 = 5.0
print(10//2)  # Floor division with integers: 10//2 = 5
print(10.0/2)  # Floating point division: 10.0/2 = 5.0
print(10.0//2) # Floor division with float: 10.0//2 = 5.0
```


### Notes on Division Operators:

- The `/` operator **always performs floating-point arithmetic**, and it will always return a float value.
- The `//` operator performs **floor division**. It behaves differently based on the types of arguments:
  - If both arguments are integers, the result will be an **integer**.
  - If at least one of the arguments is a float, the result will be a **float**.

---

### String Operations with `+` and `*`

#### **Using the `+` operator with strings**:

You can concatenate strings using the `+` operator. However, both operands must be of type **string**. If you try to combine a string with a non-string (like an integer), a `TypeError` will be raised.

```python
# Valid example
name = "sagar" + "10"
print(name)  # Output: "sagar10"

# Invalid example: Raises TypeError
name = "sagar" + 10
# TypeError: must be str, not int
```

#### **Using the `*` operator with strings**:

You can use the `*` operator to repeat a string a specified number of times. One operand should be an **integer**, and the other should be a **string**. Using a non-integer (e.g., float) for repetition will raise a `TypeError`.

```python
name = "Sagar"
print(name * 3)  # Output: "SagarSagarSagar"

# Invalid example: Raises TypeError
print(name * 2.5)
# TypeError: can't multiply sequence by non-int of type 'float'
```

---

### Division by Zero

- **`x / 0`** and **`x % 0`** will raise a `ZeroDivisionError`.
  
  ```python
  a = 10
  print(a / 0)  # Raises ZeroDivisionError
  print(a % 0)  # Raises ZeroDivisionError
  ```

---





## 4.2 Relational Operators

Relational operators are used to compare two values and return a Boolean value (`True` or `False`).

| Operator | Description    | Example        | Output |
|----------|----------------|----------------|--------|
| `==`     | Equal to       | `5 == 3`       | `False`|
| `!=`     | Not equal to   | `5 != 3`       | `True` |
| `>`      | Greater than   | `5 > 3`        | `True` |
| `<`      | Less than      | `5 < 3`        | `False`|
| `>=`     | Greater than or equal to | `5 >= 5` | `True` |
| `<=`     | Less than or equal to    | `3 <= 5` | `True` |


### Example 1: Relatoinal operators with int type

```python
a = 10
b = 20
print("a > b ", a > b)      # False
print("a >= b ", a >= b)    # False
print("a < b ", a < b)      # True
print("a <= b ", a <= b)    # True

```

### Example 2: Relational operators with string type

```python
a = "sagar"
b = "sagar"
print("a > b ", a > b)      # False
print("a >= b ", a >= b)    # True
print("a < b ", a < b)      # False 
print("a <= b ", a <= b)    # True
print(7 > "sagar")          # TypeError: '>' not supported between instances of int and str

```

### Example 3: Chaining of relational operators  
In the chaining, if all comparisions returns True then the result will be True. If atleast one comparision returns False then the result is False.

```python

print(5 < 6)            # True
print(5 < 6 < 6)        # True
print(5 < 6 < 7 < 8)    # True
print(5 < 6 < 7 < 8 > 9)# False

```

### Example 4: Equality Operators `==` and `!=`
These operators can be applied on variables of any type even they are not compatible.

```python
print(1 == 2)       # False     
print(1 != 2)       # True
print(4 == True)    # False
print(False == False)       # True
print("Sagar" == "sagar")   # False
print("Sagar" == 5)         # False

```

### Example 5: Chaining of Equality Operators

```python
print( 5 == 6 == 7 == 8)    # False
print( 5 == 5 == 5 == 5)    # True

```


---

## 4.3 Logical Operators

Logical operators are used to combine conditional statements and return a Boolean result.

| Operator | Description          | Example          | Output   |
|----------|----------------------|------------------|----------|
| `and`    | Returns `True` if both conditions are true | `True and False` | `False`  |
| `or`     | Returns `True` if at least one condition is true | `True or False`  | `True`   |
| `not`    | Reverses the result of the condition | `not True`        | `False`  |


Here’s an expanded version with additional examples of how `and`, `or`, and `not` work with various data types (such as lists, dictionaries, etc.) in Python, including the ones you missed:

---


### Example 1: Boolean Type
- **`and`**: If both arguments are `True`, then the result is `True`.
- **`or`**: If at least one argument is `True`, then the result is `True`.
- **`not`**: Complement (i.e., opposite of the value).

```python
print(True and True)    # True
print(True or False)    # True
print(not False)        # True
```

> **Note:** These examples also include the operations on Python collections, such as `list`, `tuple`, etc. You will learn more about these collections in the next modules, so feel free to revisit these examples when you reach that part of your learning journey.

### Example 2: Non-Boolean Type

- **`0`** is treated as `False`.
- **Non-zero values** are treated as `True`.
- **Empty strings** are treated as `False`.
- **Empty lists** `[]`, **empty tuples** `()`, **empty dictionaries** `{}`, and **empty sets** `set()` are treated as `False`.
- **Non-empty containers** (e.g., lists, dictionaries, sets) are treated as `True`.

#### `and` operation:
If `x` evaluates to `False`, the result is `x`; otherwise, the result is `y`.

```python
print(10 and 20)   # 20 (since 10 is non-zero, return 20)
print(0 and 5)     # 0 (since 0 is false, return 0)
print([] and 5)    # [] (empty list is falsy)
print([1, 2] and 5)  # 5 (non-empty list is truthy)
```

#### `or` operation:
If `x` evaluates to `True`, the result is `x`; otherwise, the result is `y`.

```python
print(10 or 15)    # 10 (since 10 is non-zero, return 10)
print(0 or 15)     # 15 (since 0 is false, return 15)
print([] or [5])   # [5] (empty list is falsy, return the second value)
print([1, 2] or [5])  # [1, 2] (non-empty list is truthy, return the first value)
```

#### `not` operation:
If `x` evaluates to `False`, the result is `True`; otherwise, the result is `False`.

```python
print(not 9)       # False (since 9 is non-zero, return False)
print(not 0)       # True (since 0 is false, return True)
print(not [])      # True (empty list is falsy)
print(not [1, 2])  # False (non-empty list is truthy)
```

---

### String Operations with `and`, `or`, `not`

- **`and`**: Returns the first falsy value or the last value.
- **`or`**: Returns the first truthy value or the last value.
- **`not`**: Reverses the truthiness of the value.

```python
print("sagar" and "sagar chhabriya")  # "sagar chhabriya" (both are non-empty strings, returns the last)
print("" and "sagar")                 # "" (empty string, returns the first value)
print("sagar" and "")                 # "" (empty string, returns the last value)

print("sagar" or "sagar chhabriya")   # "sagar" (first string is truthy, returns the first value)
print("" or "sagar")                  # "sagar" (empty string, returns the second value)
print("sagar" or "")                  # "sagar" (first string is truthy, returns the first value)

print(not "")                         # True (empty string is falsy, so `not` returns True)
print(not "sagar")                    # False (non-empty string is truthy, so `not` returns False)
```

---

### Additional Examples with Other Types

#### Lists:
- **Empty list `[]`** is falsy.
- **Non-empty list `[1, 2]`** is truthy.

```python
print([] and [1])         # [] (empty list, returns the first value)
print([1] or [])          # [1] (non-empty list, returns the first value)
print(not [])             # True (empty list is falsy)
print(not [1, 2])         # False (non-empty list is truthy)
```

#### Dictionaries:
- **Empty dictionary `{}`** is falsy.
- **Non-empty dictionary `{"a": 1}`** is truthy.

```python
print({} and {"a": 1})    # {} (empty dictionary, returns the first value)
print({"a": 1} or {})      # {"a": 1} (non-empty dictionary, returns the first value)
print(not {})             # True (empty dictionary is falsy)
print(not {"a": 1})       # False (non-empty dictionary is truthy)
```

#### Tuples:
- **Empty tuple `()`** is falsy.
- **Non-empty tuple `(1, 2)`** is truthy.

```python
print(() and (1, 2))      # () (empty tuple, returns the first value)
print((1, 2) or ())       # (1, 2) (non-empty tuple, returns the first value)
print(not ())             # True (empty tuple is falsy)
print(not (1, 2))         # False (non-empty tuple is truthy)
```

#### Sets:
- **Empty set `set()`** is falsy.
- **Non-empty set `{"a", "b"}`** is truthy.

```python
print(set() and {"a"})   # set() (empty set, returns the first value)
print({"a"} or set())     # {"a"} (non-empty set, returns the first value)
print(not set())          # True (empty set is falsy)
print(not {"a", "b"})     # False (non-empty set is truthy)
```

---

### To Concise:
- **`and`**: Returns the first falsy value or the last value if both are truthy.
- **`or`**: Returns the first truthy value or the last value if both are falsy.
- **`not`**: Reverses the truthiness of the value.
- `0`, `""` (empty string), empty lists `[]`, empty tuples `()`, empty dictionaries `{}`, and empty sets `set()` are treated as **False**.
- Any non-zero number or non-empty container (list, dictionary, string, tuple, set) is treated as **True**.



---


## 4.4 Membership Operators

Membership operators are used to check if a value is found within a sequence (such as a list, tuple, or string).

| Operator    | Description                       | Example         | Output |
|-------------|-----------------------------------|-----------------|--------|
| `in`        | Returns `True` if the value is found in the sequence | `3 in [1, 2, 3]` | `True` |
| `not in`    | Returns `True` if the value is not found in the sequence | `4 not in [1, 2, 3]` | `True` |


### `in` Operator:
The **`in`** operator is used to check if a value is present in a sequence (like a list, tuple, string, or set). It returns `True` if the value is found and `False` otherwise.

#### Example 1: Using `in` with a List

```python
print(3 in [1, 2, 3])   # True (3 is in the list)
```

#### Example 2: Using `in` with a String

```python
print("a" in "apple")   # True ('a' is in the string "apple")
print("z" in "apple")   # False ('z' is not in the string "apple")
```

#### Example 3: Using `in` with a Tuple

```python
print(4 in (1, 2, 3, 4))    # True (4 is in the tuple)
print(5 in (1, 2, 3, 4))    # False (5 is not in the tuple)
```

#### Example 4: Using `in` with a Set

```python
print(1 in {1, 2, 3})   # True (1 is in the set)
print(10 in {1, 2, 3})  # False (10 is not in the set)
```

#### Example 5: Using `in` with a Dictionary (checks keys)

```python
print("name" in {"name": "John", "age": 30})  # True (key 'name' is in the dictionary)
print("address" in {"name": "John", "age": 30})  # False (key 'address' is not in the dictionary)
```

#### Example 6: Using `in` with an Empty Sequence

```python
print(3 in [])      # False (list is empty)
print("a" in "")    # False (empty string)
print(1 in ())      # False (empty tuple)
```

---

### `not in` Operator:
The **`not in`** operator is used to check if a value is **not** present in a sequence. It returns `True` if the value is not found in the sequence, and `False` otherwise.

#### Example 1: Using `not in` with a List

```python
print(4 not in [1, 2, 3])   # True (4 is not in the list)
print(3 not in [1, 2, 3])   # False (3 is in the list)
```

#### Example 2: Using `not in` with a String

```python
print("b" not in "apple")   # True ('b' is not in the string "apple")
print("a" not in "apple")   # False ('a' is in the string "apple")
```

#### Example 3: Using `not in` with a Tuple

```python
print(5 not in (1, 2, 3, 4))    # True (5 is not in the tuple)
print(2 not in (1, 2, 3, 4))    # False (2 is in the tuple)
```

#### Example 4: Using `not in` with a Set

```python
print(10 not in {1, 2, 3})  # True (10 is not in the set)
print(2 not in {1, 2, 3})   # False (2 is in the set)
```

#### Example 5: Using `not in` with a Dictionary (checks keys)

```python
print("address" not in {"name": "John", "age": 30})  # True (key 'address' is not in the dictionary)
print("name" not in {"name": "John", "age": 30})     # False (key 'name' is in the dictionary)
```

#### Example 6: Using `not in` with an Empty Sequence

```python
print(1 not in [])      # True (list is empty, so no 1 is present)
print("z" not in "")    # True (empty string, so no 'z' is present)
print(2 not in ())      # True (empty tuple, so no 2 is present)
```



### To Concise:
- **`in`** is used to check if a value exists **in** a sequence (list, string, tuple, set, etc.).
- **`not in`** is used to check if a value does **not exist** in the sequence.
- These operators are very useful for checking membership and can be used with various types of sequences like lists, tuples, strings, sets, and dictionaries (where they check for keys).





---

## 4.5 Identity Operators

Identity operators are used to compare objects and check if they are the same object in memory.

| Operator    | Description                        | Example            | Output |
|-------------|------------------------------------|--------------------|--------|
| `is`        | Returns `True` if both operands refer to the same object | `x is y` (where `x = 10`, `y = 10`) | `True` |
| `is not`    | Returns `True` if both operands do not refer to the same object | `x is not y` (where `x = 10`, `y = 20`) | `True` |

### `is` Operator:
The **`is`** operator is used to check if two operands refer to the **same object** in memory. It returns `True` if both operands point to the same object (i.e., they have the same memory address), and `False` otherwise.

#### Example 1: Comparing two variables with the same value

```python
x = 10
y = 10
print(x is y)    # True, since small integers are cached in Python
```

#### Example 2: Comparing two variables with different values

```python
x = 10
y = 20
print(x is y)    # False, since they refer to different objects in memory
```

#### Example 3: Comparing two lists with the same values but different memory locations

```python
x = [1, 2, 3]
y = [1, 2, 3]
print(x is y)    # False, lists are mutable and created in different memory locations
```

#### Example 4: Comparing two variables referencing the same list

```python
x = [1, 2, 3]
y = x   # Both variables point to the same list object
print(x is y)    # True, both variables refer to the same list in memory
```

#### Example 5: Comparing `None` with a variable

```python
x = None
y = None
print(x is y)    # True, both variables refer to the same `None` object in memory
```

#### Example 6: Comparing different objects of custom class

```python
class Person:
    def __init__(self, name):
        self.name = name

x = Person("Alice")
y = Person("Alice")

print(x is y)    # False, two different objects with the same data
```

---

### `is not` Operator:
The **`is not`** operator is used to check if two operands **do not refer** to the same object in memory. It returns `True` if the operands refer to different objects, and `False` otherwise.

#### Example 1: Comparing two variables with different values

```python
x = 10
y = 20
print(x is not y)    # True, they refer to different objects in memory
```

#### Example 2: Comparing two variables with the same value but different memory locations

```python
x = [1, 2, 3]
y = [1, 2, 3]
print(x is not y)    # True, even though the lists have the same value, they are stored in different memory locations
```

#### Example 3: Comparing two variables that refer to the same object

```python
x = [1, 2, 3]
y = x   # Both variables refer to the same list object
print(x is not y)    # False, they are the same object in memory
```

#### Example 4: Comparing `None` with a variable

```python
x = None
y = 10
print(x is not y)    # True, they are different objects in memory
```

#### Example 5: Comparing two objects of a custom class

```python
class Person:
    def __init__(self, name):
        self.name = name

x = Person("Alice")
y = Person("Alice")

print(x is not y)    # True, they are two different objects, even though their attributes are the same
```

#### Example 6: Comparing different `None` references

```python
x = None
y = None
print(x is not y)    # False, they refer to the same `None` object in memory
```



### To Concise:
- **`is`**: Checks if two variables point to the **same object** in memory (same memory address).
- **`is not`**: Checks if two variables do **not point** to the same object in memory.
- These identity operators are especially useful when working with immutable types like `None`, `True`, `False`, small integers, and strings that may be cached in Python. For mutable objects (e.g., lists, dictionaries), the `is` and `is not` operators check for **object identity** (memory address), not for equality of their contents.

---

## 4.6 Bitwise Operators

Bitwise operators perform operations on binary numbers (bits).

| Operator | Description            | Example           | Output   |
|----------|------------------------|-------------------|----------|
| `&`      | Bitwise AND            | `5 & 3`           | `1`      |
| `|`      | Bitwise OR             | `5 | 3`           | `7`      |
| `^`      | Bitwise XOR            | `5 ^ 3`           | `6`      |
| `<<`     | Bitwise left shift     | `5 << 1`          | `10`     |
| `>>`     | Bitwise right shift    | `5 >> 1`          | `2`      |
| `~`      | Bitwise NOT            | `~5`              | `-6`     |



### Bitwise AND (`&`):
The **AND** operator (`&`) compares each bit of two numbers and returns `1` if both corresponding bits are `1`, otherwise returns `0`.

#### Example 1: Basic Bitwise AND

```python
print(5 & 3)   # 5 = 0101, 3 = 0011 -> Result: 0001 -> 1
```

#### Example 2: Bitwise AND with 0

```python
print(0 & 3)   # 0 = 0000, 3 = 0011 -> Result: 0000 -> 0
```

#### Example 3: Bitwise AND with same numbers

```python
print(5 & 5)   # 5 = 0101, 5 = 0101 -> Result: 0101 -> 5
```

#### Example 4: Bitwise AND with negative numbers (in two's complement)

```python
print(-5 & 3)  # -5 = ...11111011, 3 = 00000011 -> Result: 00000001 -> 1
```

---

### Bitwise OR (`|`):
The **OR** operator (`|`) compares each bit of two numbers and returns `1` if at least one of the corresponding bits is `1`, otherwise returns `0`.

#### Example 1: Basic Bitwise OR

```python
print(5 | 3)   # 5 = 0101, 3 = 0011 -> Result: 0111 -> 7
```

#### Example 2: Bitwise OR with 0

```python
print(0 | 3)   # 0 = 0000, 3 = 0011 -> Result: 0011 -> 3
```

#### Example 3: Bitwise OR with same numbers

```python
print(5 | 5)   # 5 = 0101, 5 = 0101 -> Result: 0101 -> 5
```

#### Example 4: Bitwise OR with negative numbers

```python
print(-5 | 3)  # -5 = ...11111011, 3 = 00000011 -> Result: 00000011 -> 3
```

---

### Bitwise XOR (`^`):
The **XOR** operator (`^`) compares each bit of two numbers and returns `1` if the bits are different, otherwise returns `0`.

#### Example 1: Basic Bitwise XOR

```python
print(5 ^ 3)   # 5 = 0101, 3 = 0011 -> Result: 0110 -> 6
```

#### Example 2: Bitwise XOR with 0

```python
print(0 ^ 3)   # 0 = 0000, 3 = 0011 -> Result: 0011 -> 3
```

#### Example 3: Bitwise XOR with same numbers (results in 0)

```python
print(5 ^ 5)   # 5 = 0101, 5 = 0101 -> Result: 0000 -> 0
```

#### Example 4: Bitwise XOR with negative numbers

```python
print(-5 ^ 3)  # -5 = ...11111011, 3 = 00000011 -> Result: 00000000 -> 0
```

---

### Bitwise Left Shift (`<<`): Put 0s from trailing bits directions
The **left shift** operator (`<<`) shifts the bits of the number to the left by a specified number of positions. Each left shift is equivalent to multiplying the number by `2` for each position shifted.

#### Example 1: Basic Bitwise Left Shift

```python
print(5 << 1)   # 5 = 0101 -> Shift left by 1 -> 1010 -> 10
```

#### Example 2: Left shift with 0

```python
print(0 << 2)   # 0 = 0000 -> Shift left by 2 -> 0000 -> 0
```

#### Example 3: Left shift by more than one position

```python
print(5 << 2)   # 5 = 0101 -> Shift left by 2 -> 10100 -> 20
```

#### Example 4: Left shift with negative numbers

```python
print(-5 << 1)  # -5 = ...11111011 -> Shift left by 1 -> ...11110110 -> -10
```

---

### Bitwise Right Shift (`>>`): Put 0s from leading bits side
The **right shift** operator (`>>`) shifts the bits of the number to the right by a specified number of positions. Each right shift is equivalent to integer division by `2` for each position shifted.

#### Example 1: Basic Bitwise Right Shift

```python
print(5 >> 1)   # 5 = 0101 -> Shift right by 1 -> 0010 -> 2
```

#### Example 2: Right shift with 0

```python
print(0 >> 2)   # 0 = 0000 -> Shift right by 2 -> 0000 -> 0
```

#### Example 3: Right shift by more than one position

```python
print(5 >> 2)   # 5 = 0101 -> Shift right by 2 -> 0001 -> 1
```

#### Example 4: Right shift with negative numbers

```python
print(-5 >> 1)  # -5 = ...11111011 -> Shift right by 1 -> ...11111101 -> -3
```

---

### Bitwise NOT (`~`):
The **NOT** operator (`~`) inverts all the bits of a number, i.e., it changes all `1`s to `0`s and all `0`s to `1`s. In Python, this is implemented as `-(x+1)` due to two's complement representation of negative integers.

#### Example 1: Basic Bitwise NOT

```python
print(~5)    # 5 = 0101 -> Invert bits -> ...1010 -> -6 (because of two's complement representation)
```

#### Example 2: Bitwise NOT with 0

```python
print(~0)    # 0 = 0000 -> Invert bits -> ...1111 -> -1
```

#### Example 3: Bitwise NOT with negative numbers

```python
print(~-5)   # -5 = ...11111011 -> Invert bits -> ...00000100 -> 4
```

---


### To Concise:
- **Bitwise AND (`&`)**: Only `1` when both bits are `1`.
- **Bitwise OR (`|`)**: `1` when at least one bit is `1`.
- **Bitwise XOR (`^`)**: `1` when bits are different.
- **Bitwise Left Shift (`<<`)**: Shifts bits to the left (multiplies by 2 for each shift).
- **Bitwise Right Shift (`>>`)**: Shifts bits to the right (divides by 2 for each shift).
- **Bitwise NOT (`~`)**: Inverts all bits (works with two's complement).

These operators are commonly used in low-level programming, encryption algorithms, and performance-critical applications where bit manipulation is necessary.


---

## 4.7 Assignment Operators

Assignment operators are used to assign values to variables and can also perform operations on the values.

| Operator | Description                    | Example          | Output |
|----------|--------------------------------|------------------|--------|
| `=`      | Assigns value to variable      | `x = 5`          | `x = 5` |
| `+=`     | Adds value to the variable     | `x += 3`         | `x = 8` |
| `-=`     | Subtracts value from variable  | `x -= 2`         | `x = 3` |
| `*=`     | Multiplies variable by value   | `x *= 2`         | `x = 6` |
| `/=`     | Divides variable by value      | `x /= 2`         | `x = 3.0` |
| `//=`    | Floor divides variable by value| `x //= 2`        | `x = 3` |
| `%=`     | Modulo assigns result to variable | `x %= 2`        | `x = 1` |
| `**=`    | Exponentiation assignment      | `x **= 2`        | `x = 25` |




---

### **1. `=` Assignment Operator (Assigns value to variable)**
This operator simply assigns a value to a variable.

#### **Variables:**
```python
x = 10       # Assigns 10 to x
y = 3.5      # Assigns 3.5 to y
z = "Hello"  # Assigns "Hello" to z
```

#### **Collections:**

- **List**:
```python
lst = [1, 2, 3]  # Assigns a list to lst
```

- **Set**:
```python
my_set = {1, 2, 3}  # Assigns a set to my_set
```

- **Dictionary**:
```python
my_dict = {'a': 1, 'b': 2}  # Assigns a dictionary to my_dict
```

---

### **2. `+=` (Adds to variable or collection)**
This operator adds the value on the right to the variable on the left.
#### **Variables:**

- **Integers**:
```python
x = 5
x += 3   # x = x + 3
print(x) # Output: 8
```

- **Strings (concatenation)**:
```python
text = "Hello"
text += " World"   # text = text + " World"
print(text)         # Output: "Hello World"
```

#### **Collections:**

- **List** (Appends and extends):
```python
lst = [1, 2, 3]
lst += [4]         # Appends 4 to the list
print(lst)         # Output: [1, 2, 3, 4]

lst += [5, 6]      # Extends the list with another list
print(lst)         # Output: [1, 2, 3, 4, 5, 6]
```

- **Set** (Adds an element):
```python
my_set = {1, 2, 3}
my_set += {4}      # Adds 4 to the set (if it's not already present)
print(my_set)      # Output: {1, 2, 3, 4}
```

- **Dictionary** (Merges another dictionary):


```python
# Merging two dictionaries
dict1 = {'a': 1, 'b': 2}
dict2 = {'c': 3, 'd': 4}
dict1 += dict2  # This will throw an error since `+=` is not supported for dictionaries
print(dict1)    # This will raise TypeError: 'dict' object does not support item assignment

# For dictionaries, use the update() method instead:
dict1.update(dict2)  # Merges dict2 into dict1
print(dict1)         # Output: {'a': 1, 'b': 2, 'c': 3, 'd': 4}
```
---

### **3. `-=` (Subtracts from variable or collection)**

This operator subtracts the value on the right from the variable on the left.

#### **Variables:**

- **Integers**:
```python
x = 10
x -= 4   # x = x - 4
print(x) # Output: 6
```

- **Float**
```python
y = 5.5
y -= 2.5  # Equivalent to y = y - 2.5
print(y)  # Output: 3.0
```

- **String**
```python
text = "Hello"
text -= "o"  # This will raise a TypeError
```



#### **Collections:**

- **List** (Removes specific values):
```python
lst = [1, 2, 3, 4]
lst -= [2, 4]    # Removes 2 and 4 from the list
print(lst)       # Output: [1, 3]
```

- **Set** (Removes elements):
```python
my_set = {1, 2, 3, 4}
my_set -= {2, 4}   # Removes 2 and 4
print(my_set)      # Output: {1, 3}
```

- **Dictionary** (Removes key-value pairs using `del`):
```python

# Removing specific key-value pairs from a dictionary
my_dict = {'a': 1, 'b': 2, 'c': 3}
my_dict -= {'a': 1, 'c': 3}  # This will raise an error. Use `del` or `pop()` instead.
print(my_dict)              # Raises a TypeError: 'dict' object is not supported by -=

# Instead, use a loop or pop() to remove key-value pairs:
# Correct way to remove key-value pairs
del my_dict['b']
print(my_dict)  # Output: {'a': 1, 'c': 3}

# or del keyword

my_dict = {'a': 1, 'b': 2, 'c': 3}
del my_dict['b']   # Removes the key 'b' and its value
print(my_dict)     # Output: {'a': 1, 'c': 3}
```

---

### **4. `*=` (Multiplies variable by value)**
This operator multiplies the value of the variable by the value on the right.

#### **Variables:**

- **Integer**
```python
x = 4
x *= 2    # Equivalent to x = x * 2
print(x)  # Output: 8
```

- **Float**
```python
y = 3.5
y *= 2    # Equivalent to y = y * 2
print(y)  # Output: 7.0
```

- **Strings** (Repetition):
```python
text = "abc"
text *= 3  # Repeats the string 3 times
print(text)  # Output: "abcabcabc"
```

#### **Collections:**

- **List** (Repeats the list):
```python
lst = [1, 2, 3]
lst *= 2   # Repeats the list twice
print(lst) # Output: [1, 2, 3, 1, 2, 3]
```

- **Sets** (Cannot use `*=` with sets):
```python
my_set = {1, 2, 3}
# my_set *= 2   # Raises TypeError: 'set' object cannot be multiplied
```

- **Dictionaries** (Cannot use `*=` with dictionaries):
```python
my_dict = {'a': 1, 'b': 2}
# my_dict *= 2   # Raises TypeError: 'dict' object cannot be multiplied
```

---

### **5. `/=` (Divides elements in variable or collection)**
This operator divides the value of the variable by the value on the right.

#### **Variables:**

- **Integers**:
```python
x = 10
x /= 2    # x = x / 2
print(x)  # Output: 5.0 (Result is a float)
```

- **Float**
```python
y = 6.0
y /= 2.0  # Equivalent to y = y / 2.0
print(y)  # Output: 3.0
```

- **Dividing by zero (raises error)**

```python
x = 10
x /= 0    # This will raise a ZeroDivisionError
```



#### **Collections:**
The `/=` operator is not commonly used with collections like lists, sets, or dictionaries in Python. It is meant for scalar types like numbers. Using it with collections will raise errors.
<br>
However, you can use the division operator to perform operations on the elements of the collection, but you need to do this manually in a loop or list comprehension.



- **List** (Dividing each element by 2):
```python
lst = [10, 20, 30]
lst = [x / 2 for x in lst]   # Divide each element by 2
print(lst)  # Output: [5.0, 10.0, 15.0]
```

- **Dictionaries** (Dividing each dictionary value by 2):
```python
my_dict = {'a': 10, 'b': 20}
my_dict = {k: v / 2 for k, v in my_dict.items()}
print(my_dict)  # Output: {'a': 5.0, 'b': 10.0}
```

---

### **6. `//=` (Floor divides elements in variable or collection)**

This operator performs floor division (division that rounds down the result). Similar to division, floor division will also need to be applied element-wise in collections.

#### **Variables:**

- **Integers**:
```python
x = 10
x //= 3   # x = x // 3 (floor division)
print(x)  # Output: 3
```

- **Floor dividing with a negative number**
```python
y = -7
y //= 3   # Equivalent to y = y // 3
print(y)  # Output: -3 (-7 // 3 = -3)

# -7 / 3  ---> -2.3333333333333335
# -7 // 3 ---> -3
```


- **Floor dividing with a positive number**
```python
y = 7
y //= 3   # Equivalent to y = y // 3
print(y)  # Output: 3 (7 // 3 = 2)

#  7 / 3  --->  2.3333333333333335
#  7 // 3 --->  2
```




#### **Collections:**

- **List** (Floor dividing each element by 2):
```python
lst = [10, 20, 30]
lst = [x // 2 for x in lst]   # Floor divide each element by 2
print(lst)  # Output: [5, 10, 15]
```

- **Dictionaries** (Floor dividing each dictionary value by 2):
```python
my_dict = {'a': 10, 'b': 25}
my_dict = {k: v // 2 for k, v in my_dict.items()}
print(my_dict)  # Output: {'a': 5, 'b': 12}
```

---

### **7. `%=` (Modulo operation on variable or collection)**

This operator computes the remainder of the division of the variable by the value on the right.
#### **Variables:**

- **Integers**:
```python
x = 10
x %= 3   # x = x % 3
print(x)  # Output: 1
```

- **Float**
```python
y = 10.5
y %= 3    # Equivalent to y = y % 3
print(y)  # Output: 1.5 (10.5 % 3 = 1.5)
```


#### **Collections:**
Modulo operation can be applied element-wise in a similar way as division or floor division.

- **List** (Modulo each element by 3):
```python
lst = [10, 20, 30]
lst = [x % 3 for x in lst]   # Apply modulo 3 to each element
print(lst)  # Output: [1, 2, 0]
```

- **Dictionaries** (Modulo each value by 3):
```python
my_dict = {'a': 10, 'b': 25}
my_dict = {k: v % 3 for k, v in my_dict.items()}
print(my_dict)  # Output: {'a': 1, 'b': 1}
```

---

### **8. `**=` (Exponentiation operation on variable or collection)**

This operator raises the variable to the power of the value on the right.
#### **Variables:**

- **Integers**:
```python
x = 2
x **= 3  # x = x ** 3
print(x)  # Output: 8
```

- **Float**
```python
y = 3.0
y **= 2   # Equivalent to y = y ** 2
print(y)  # Output: 9.0 (3.0 ** 2 = 9.0)
```

- **Negative Exponents**
```python
z = 4
z **= -2  # Equivalent to z = z ** -2
print(z)  # Output: 0.0625 (4 ** -2 = 1/16 = 0.0625)
```



#### **Collections:**
Exponentiation, like other operations, needs to be performed element-wise in collections.


- **List** (Exponentiating each element):
```python
lst = [2, 3, 4]
lst = [x ** 2 for x in lst]   # Raise each element to the power of 2
print(lst)  # Output: [4, 9, 16]
```

- **Dictionaries** (Exponentiating each value):
```python
my_dict = {'a': 2, 'b': 3}
my_dict = {k: v ** 2 for k, v in my_dict.items()}
print(my_dict)  # Output: {'a': 4, 'b': 9}
```

---

### To Concise:

- **`=`**: Assigns values to variables or collections.
- **`+=`**: Adds (or appends) to variables or collections (lists, sets, dictionaries).
- **`-=`**: Subtracts from variables or removes elements from collections (lists, sets).
- **`*=`**: Repeats elements in collections (lists, strings); not supported for sets or dictionaries.
- **`/=`**: Divides variables

 or elements in collections.
- **`//=`**: Floor divides variables or elements in collections.
- **`%=`**: Applies modulo operation on variables or elements in collections.
- **`**=`**: Exponentiates variables or elements in collections.


---

## 4.8 Operators Precedence

Operator precedence determines the order in which operations are performed in an expression.


| Precedence | Operator(s)                     | Description                 |
|------------|---------------------------------|-----------------------------|
| 1          | `()`                            | Parentheses                 |
| 2          | `**`                            | Exponentiation              |
| 3          | `~`, `+`, `-`                   | Bitwise NOT, Unary Plus/Minus |
| 4          | `*`, `/`, `//`, `%`             | Multiplication, Division, Modulus |
| 5          | `+`, `-`                        | Addition, Subtraction       |
| 6          | `<<`, `>>`                      | Bitwise Shifts              |
| 7          | `&`                             | Bitwise AND                 |
| 8          | `^`                             | Bitwise XOR                 |
| 9          | `|`                             | Bitwise OR                  |
| 10         | `==`, `!=`, `>`, `<`, `>=`, `<=`| Comparison Operators        |
| 11         | `is`, `is not`                  | Identity Operators          |
| 12         | `in`, `not in`                  | Membership Operators        |
| 13         | `not`                           | Logical NOT                 |
| 14         | `and`                           | Logical AND                 |
| 15         | `or`                            | Logical OR                  |

---

## 4.9 Evaluating Expressions

Python evaluates expressions based on operator precedence and associativity.

### Example:
```python
result = 5 + 3 * 2  # Multiplies first due to precedence
print(result)  # Output: 11
```

### Associativity:
- Left to right for most operators (e.g., `+`, `-`, `*`).
- Right to left for exponentiation (`**`).

---

## 4.10 Type Casting

Type casting is the process of converting one data type to another.

### Implicit Type Conversion (Automatic Conversion):
Python automatically converts smaller data types to larger data types during operations.

```python
x = 5  # int
y = 2.5  # float
result = x + y  # Implicit conversion of int to float
print(result)  # Output: 7.5
```

### Explicit Type Conversion (Manual Conversion):
You can manually convert data types using `int()`, `float()`, `str()`, etc.

```python
x = "5"
y = int(x)  # Explicit conversion from string to int
print(y)  # Output: 5
```

---

## 4.11 Miscellaneous Operators

### Division Operator (`/` vs `//`):
- `/` performs float division.
- `//` performs floor division (returns an integer).

```python
result1 = 5 / 2  # Output: 2.5
result2 = 5 // 2  # Output: 2
```

### Operator Overloading:
Python allows operators to be overloaded so that they behave differently based on the operands. This means you can define custom behavior for operators like `+`, `-`, etc., when they are used with user-defined classes.

#### Example 1: Using `+` for string concatenation:

The `+` operator can be used to concatenate strings, as shown below:

```python
str1 = "Hello, "
str2 = "World!"
result = str1 + str2  # Concatenates the two strings
print(result)  # Output: Hello, World!
```

In this case, the `+` operator is used to concatenate two strings. This demonstrates how the same operator behaves differently based on the data types it is used with.

#### Example 2: Overloading `+` for numeric addition:

In Python, you can overload operators to define custom behavior for specific classes. Here's how the `+` operator can be overloaded for a custom class to add numerical values:

```python
class MyClass:
    def __init__(self, value):
        self.value = value
        
    def __add__(self, other):
        return self.value + other.value

obj1 = MyClass(5)
obj2 = MyClass(3)
result = obj1 + obj2  # Calls __add__ method
print(result)  # Output: 8
```

In this example, we overloaded the `+` operator to add the `value` attribute of two `MyClass` objects.

### Explanation:
- In **Example 1**, the `+` operator is used to concatenate two string objects, resulting in the combined string `"Hello, World!"`.
- In **Example 2**, the `+` operator is overloaded to perform numerical addition between objects of a custom class `MyClass`, adding their `value` attributes.

This illustrates how the same operator (`+`) can be used with different types (strings vs. custom objects) to perform different operations.

## 4.12 Inplace vs Standard Operators

In-place operators modify the value of a variable directly, while standard operators create a new value.

| Operator    | In-place | Standard |
|-------------|----------|----------|
| `+=`        | Yes      | No       |
| `-=`        | Yes      | No       |
| `*=`        | Yes      | No       |
| `/=`        | Yes      | No       |
| `+`         | No       | Yes      |
| `-`         | No       | Yes      |

### Example:
```python
x = 5
x += 3  # In-place addition (x = x + 3)
print(x)  # Output: 8
```

---

## 4.13 Comparing `==` vs `is`

### `==` vs `is`:
- `==` checks for value equality.
- `is` checks for identity (whether two objects are the same in memory).

### Example:
```python
x = [1, 2, 3]
y = [1, 2, 3]
z = x

print(x == y)  # True (values are equal)
print(x is y)  # False (different objects)
print(x is z)  # True (same object)
```

---

## 4.14 Membership and Identity Operators

### Differences between `in`, `not in`, `is`, `is not`:
- **`in` / `not in`**: Used to check if a value is in a sequence.
- **`is` / `is not`**: Used to check if two objects refer to the same memory location.

### Example:
```python
x = [1, 2, 3]
y = [1, 2, 3]
z = x

print(3 in x)  # True
print(x is y)  # False
print(x is z)  # True
```

| Operator   | Description           | Example                               | Result |
|------------|-----------------------|---------------------------------------|--------|
| `in`       | Checks membership     | `"a" in ["a", "b", "c"]`              | `True` |
| `not in`   | Checks non-membership | `"d" not in ["a", "b", "c"]`          | `True` |
| `is`       | Checks object identity| `x = 5; y = 5; x is y`                | `True` |
| `is not`   | Checks non-identity   | `x = 5; y = 6; x is not y`            | `True` |


# 4.15 Ternary Operator

A **ternary operator** allows you to write a simple `if-else` condition in a single line, making the code more concise.

## Syntax:
```python
<expression1> if <condition> else <expression2>
```
- If `<condition>` evaluates to `True`, then `<expression1>` is executed.
- If `<condition>` evaluates to `False`, then `<expression2>` is executed.

---

## Example 1: Basic Ternary Operator

```python
a, b = 10, 20
x = 30 if a < b else 40
print(x)
```

**Explanation**:  
Here, the condition `a < b` is checked. Since `a` is less than `b`, the value of `x` will be `30`.

**Output**:
```
30
```

---

## Example 2: Read Two Numbers from the Keyboard and Print the Minimum Value

```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
min_value = a if a < b else b
print("Minimum value:", min_value)
```

**Explanation**:  
This example reads two numbers from the user and then uses the ternary operator to find and print the smaller of the two.

**Output Example**:
```
Enter first number: 12
Enter second number: 8
Minimum value: 8
```

---

## Nesting of Ternary Operators

You can nest multiple ternary operators to handle more complex conditions. The general syntax would look like this:

```python
<expression1> if <condition1> else <expression2> if <condition2> else <expression3>
```

### Example:

```python
a, b, c = 10, 20, 30
x = a if a > b and a > c else b if b > c else c
print(x)
```

**Explanation**:  
Here, the nested ternary operator checks which of the three values `a`, `b`, or `c` is the largest and assigns it to `x`.

**Output**:
```
30
```

---

### Note on Readability:

While ternary operators can help write concise code, overusing them or nesting too many levels can reduce code readability. It’s often best to use ternary operators for simple conditions, and use regular `if-else` statements for more complex logic.


<span style="display: flex; justify-content: space-between; width: 100%; align-items: center;">
    <a href="../03-module-03-data-handling/README.md">
        <img src="https://img.shields.io/badge/Previous-Data_Handling-blue" width="250" height="35">
    </a>
    <a href="../05-module-05-debugging/README.md">
        <img src="https://img.shields.io/badge/Next-Debugging-brightgreen" width="200" height="35">
    </a>
</span>
<br><br>
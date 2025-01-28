# 4. Operators

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

---

## 4.3 Logical Operators

Logical operators are used to combine conditional statements and return a Boolean result.

| Operator | Description          | Example          | Output   |
|----------|----------------------|------------------|----------|
| `and`    | Returns `True` if both conditions are true | `True and False` | `False`  |
| `or`     | Returns `True` if at least one condition is true | `True or False`  | `True`   |
| `not`    | Reverses the result of the condition | `not True`        | `False`  |

---

## 4.4 Membership Operators

Membership operators are used to check if a value is found within a sequence (such as a list, tuple, or string).

| Operator    | Description                       | Example         | Output |
|-------------|-----------------------------------|-----------------|--------|
| `in`        | Returns `True` if the value is found in the sequence | `3 in [1, 2, 3]` | `True` |
| `not in`    | Returns `True` if the value is not found in the sequence | `4 not in [1, 2, 3]` | `True` |

---

## 4.5 Identity Operators

Identity operators are used to compare objects and check if they are the same object in memory.

| Operator    | Description                        | Example            | Output |
|-------------|------------------------------------|--------------------|--------|
| `is`        | Returns `True` if both operands refer to the same object | `x is y` (where `x = 10`, `y = 10`) | `True` |
| `is not`    | Returns `True` if both operands do not refer to the same object | `x is not y` (where `x = 10`, `y = 20`) | `True` |

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
z =

 x

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

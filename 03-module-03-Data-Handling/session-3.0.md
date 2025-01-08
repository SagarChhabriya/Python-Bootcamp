
## Literals



## Operators


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
```

This markdown content explains the different types of literals in Python and provides examples to clarify their usage.
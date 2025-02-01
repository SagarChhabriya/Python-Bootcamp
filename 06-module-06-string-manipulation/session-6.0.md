# String Manipulation
<span style="display: flex; justify-content: space-between; width: 100%; align-items: center;">
    <a href="../05-module-05-debugging/README.md">
        <img src="https://img.shields.io/badge/Previous-Debugging-blue" width="200" height="35">
    </a>
    <a href="../07-module-07-lists/README.md">
        <img src="https://img.shields.io/badge/Next-Python_Lists-brightgreen" width="170" height="35">
    </a>
</span>
<br><br>


### **6.1 Introduction to Python Strings**
- **Immutable Nature of Strings**: In Python, strings are immutable, which means once a string is created, it cannot be modified directly.
  ```python
  s = "hello"
  s[0] = "H"  # This will raise an error because strings are immutable.
  ```

### **6.2 Accessing String Elements**
- **Accessing Individual Characters**: You can access characters in a string using indexing.
  ```python
  s = "hello"
  print(s[0])  # Output: 'h'
  ```
  
- **Using Positive and Negative Indexing**:
  - Positive indices start from `0` at the beginning of the string.
  - Negative indices count from the end, starting with `-1`.
  ```python
  print(s[1])    # Output: 'e'
  print(s[-1])   # Output: 'o'
  ```

### **6.3 String Operators**
- **Concatenation (`+`)**: Combines two or more strings.
  ```python
  s1 = "Hello"
  s2 = "World"
  print(s1 + " " + s2)  # Output: 'Hello World'
  ```
  
- **Repetition (`*`)**: Repeats a string a specified number of times.
  ```python
  print("Hello " * 3)  # Output: 'Hello Hello Hello '
  ```

### **6.4 String Slicing**
- **How to slice strings**: Extract a portion of a string using the syntax `string[start:end:step]`.
  ```python
  s = "hello"
  print(s[1:4])  # Output: 'ell'
  print(s[:3])   # Output: 'hel'
  print(s[::2])  # Output: 'hlo'
  ```

- **Detailed Examples**

```python
# Replace the string with a new one
s = "Python programming is super fun and easy!"

# 1. Slice from index 1 to 7 with step 1
# This slice starts at index 1, ends just before index 7, and takes every character between them with a step of 1.
# So it picks characters at positions 1, 2, 3, 4, 5, and 6.
print(s[1:7:1])  # Output: 'ython '

# 2. Slice from index 1 to 7 without specifying step
# This slice is similar to the previous one, but here we didn't specify a step.
# So Python defaults to a step of 1, meaning it picks characters from index 1 to 6.
print(s[1:7])  # Output: 'ython '

# 3. Slice from index 1 to 7 with step 2
# This slice starts at index 1, ends just before index 7, and takes every second character between the indices.
# So it picks characters at positions 1, 3, 5 (skipping the even-indexed ones).
print(s[1:7:2])  # Output: 'yhn'

# 4. Slice up to index 7 (excluding 7)
# This slice includes all characters from the start of the string up to index 7 (but not including it).
# So it picks characters at positions 0, 1, 2, 3, 4, 5, and 6.
print(s[:7])  # Output: 'Python '

# 5. Slice the entire string
# This slice takes the entire string since we didn't specify any start or end index.
# It essentially includes everything from the beginning to the end of the string.
print(s[:])  # Output: 'Python programming is super fun and easy!'

# 6. Reverse the string
# This slice uses a negative step of -1, which means Python starts from the end of the string and goes backwards.
# It reverses the entire string, so it picks characters in reverse order from the last one to the first.
print(s[::-1])  # Output: '!ysae dna nuf repus si gnimmargorp nohtyP'

```  

[Click here to read more on String Slicing](MISC.md#string-slicing)

### **6.5 Common String Functions and Methods**
- **`upper()` and `lower()`**: Converts all characters to uppercase or lowercase.
  ```python
  s = "Hello"
  print(s.upper())  # Output: 'HELLO'
  print(s.lower())  # Output: 'hello'
  ```

- **`isupper()` and `islower()`**: Checks if all characters are uppercase or lowercase.
  ```python
  print(s.isupper())  # Output: False
  print(s.islower())  # Output: False
  ```

- **`count()`**: Counts occurrences of a substring in the string.
  ```python
  print(s.count('l'))  # Output: 2
  ```

- **`strip()`**: Removes leading and trailing whitespace.
  ```python
  s = "  hello  "
  print(s.strip())  # Output: 'hello'
  ```

- **`replace()`**: Replaces a substring with another substring.
  ```python
  print(s.replace("hello", "world"))  # Output: 'world'
  ```

- **`join()`**: Joins elements of an iterable (e.g., a list) into a string.
  ```python
  words = ["Hello", "World"]
  print(" ".join(words))  # Output: 'Hello World'
  ```

- **`split()`**: Splits a string into a list based on a delimiter (default is whitespace).
  ```python
  s = "Hello World"
  print(s.split())  # Output: ['Hello', 'World']
  ```

- **`index()`**: Returns the index of the first occurrence of a substring.
  ```python
  print(s.index('e'))  # Output: 1
  ```

### **6.6 Working with String Formatting**
- **Using f-strings**: (Python 3.6+)
  ```python
  name = "John"
  age = 30
  print(f"My name is {name} and I am {age} years old.")  
  # Output: 'My name is John and I am 30 years old.'
  ```

- **Using `format()`**:
  ```python
  print("My name is {} and I am {} years old.".format(name, age))
  # Output: 'My name is John and I am 30 years old.'
  ```

- **Using `%` formatting**:
  ```python
  print("My name is %s and I am %d years old." % (name, age))
  # Output: 'My name is John and I am 30 years old.'
  ```

[Clich here to read more on string formatting](MISC.md#string-templating)

## **6.7 Advanced String Methods**

### **`capitalize()`**
- Converts the first character of the string to uppercase and the rest to lowercase.
  ```python
  s = "hello world"
  print(s.capitalize())  # Output: 'Hello world'
  ```

---

### **`casefold()`**
- Converts the string to lowercase, but more aggressively than `lower()` (useful for case-insensitive comparisons).
  ```python
  s = "HELLO"
  print(s.casefold())  # Output: 'hello'
  ```

---

### **`center(width, fillchar)`**
- Centers the string in a specified width, padding with a specified character (default is space).
  ```python
  s = "hello"
  print(s.center(10, '-'))  # Output: '--hello---'
  print(s.center(10))       # Output: '  hello   '
  ```

---

### **`encode(encoding, errors)`**
- Encodes the string into bytes using the specified encoding (e.g., `utf-8`).
  ```python
  s = "hello"
  print(s.encode('utf-8'))  # Output: b'hello'
  ```

---

### **`endswith(suffix)`**
- Checks if the string ends with the specified suffix.
  ```python
  s = "hello"
  print(s.endswith('o'))  # Output: True
  print(s.endswith('x'))  # Output: False
  ```

---

### **`expandtabs(tabsize)`**
- Replaces tab characters (`\t`) with spaces (default tab size is 8).
  ```python
  s = "hello\tworld"
  print(s.expandtabs(4))  # Output: 'hello   world'
  ```

---

### **`find(substring)`**
- Returns the index of the first occurrence of the substring (returns `-1` if not found).
  ```python
  s = "hello"
  print(s.find('e'))  # Output: 1
  print(s.find('x'))  # Output: -1
  ```

---

### **`format_map(mapping)`**
- Similar to `format()`, but uses a dictionary for substitutions.
  ```python
  data = {'name': 'John', 'age': 30}
  print("My name is {name} and I am {age} years old.".format_map(data))
  # Output: 'My name is John and I am 30 years old.'
  ```

---

### **`isalnum()`**
- Checks if all characters in the string are alphanumeric (letters or numbers).
  ```python
  s = "hello123"
  print(s.isalnum())  # Output: True
  s = "hello 123"
  print(s.isalnum())  # Output: False
  ```

---

### **`isalpha()`**
- Checks if all characters in the string are alphabetic (letters only).
  ```python
  s = "hello"
  print(s.isalpha())  # Output: True
  s = "hello123"
  print(s.isalpha())  # Output: False
  ```

---

### **`isascii()`**
- Checks if all characters in the string are ASCII characters.
  ```python
  s = "hello"
  print(s.isascii())  # Output: True
  s = "héllo"
  print(s.isascii())  # Output: False
  ```

---

### **`isdecimal()`**
- Checks if all characters in the string are decimal digits.
  ```python
  s = "123"
  print(s.isdecimal())  # Output: True
  s = "½"
  print(s.isdecimal())  # Output: False
  ```

---

### **`isdigit()`**
- Checks if all characters in the string are digits.
  ```python
  s = "123"
  print(s.isdigit())  # Output: True
  s = "½"
  print(s.isdigit())  # Output: False
  ```

---

### **`isidentifier()`**
- Checks if the string is a valid Python identifier (e.g., variable name).
  ```python
  s = "hello_world"
  print(s.isidentifier())  # Output: True
  s = "123hello"
  print(s.isidentifier())  # Output: False
  ```

---

### **`isnumeric()`**
- Checks if all characters in the string are numeric (includes Unicode numbers).
  ```python
  s = "½"
  print(s.isnumeric())  # Output: True
  s = "123"
  print(s.isnumeric())  # Output: True
  s = "hello"
  print(s.isnumeric())  # Output: False
  ```

---

### **`isprintable()`**
- Checks if all characters in the string are printable (e.g., no escape characters).
  ```python
  s = "hello\n"
  print(s.isprintable())  # Output: False
  s = "hello"
  print(s.isprintable())  # Output: True
  ```

---

### **`isspace()`**
- Checks if all characters in the string are whitespace.
  ```python
  s = "   "
  print(s.isspace())  # Output: True
  s = "hello"
  print(s.isspace())  # Output: False
  ```

---

### **`istitle()`**
- Checks if the string follows title case (first letter of each word capitalized).
  ```python
  s = "Hello World"
  print(s.istitle())  # Output: True
  s = "hello world"
  print(s.istitle())  # Output: False
  ```

---

### **`ljust(width, fillchar)`**
- Left-justifies the string in a specified width, padding with a specified character.
  ```python
  s = "hello"
  print(s.ljust(10, '-'))  # Output: 'hello-----'
  print(s.ljust(10))       # Output: 'hello     '
  ```

---

### **`lstrip(chars)`**
- Removes leading whitespace or specified characters.
  ```python
  s = "  hello  "
  print(s.lstrip())  # Output: 'hello  '
  s = "xxhelloxx"
  print(s.lstrip('x'))  # Output: 'helloxx'
  ```

---

### **`maketrans(x, y, z)`**
- Creates a translation table for `translate()`.
  ```python
  trans = str.maketrans('aeiou', '12345')
  s = "hello"
  print(s.translate(trans))  # Output: 'h2ll4'
  ```

---

### **`partition(separator)`**
- Splits the string into three parts: before the separator, the separator, and after the separator.
  ```python
  s = "hello world"
  print(s.partition(' '))  # Output: ('hello', ' ', 'world')
  ```

---

### **`removeprefix(prefix)`**
- Removes the specified prefix from the string (Python 3.9+).
  ```python
  s = "hello world"
  print(s.removeprefix('hello '))  # Output: 'world'
  ```

---

### **`removesuffix(suffix)`**
- Removes the specified suffix from the string (Python 3.9+).
  ```python
  s = "hello world"
  print(s.removesuffix(' world'))  # Output: 'hello'
  ```

---

### **`rfind(substring)`**
- Returns the highest index of the substring (returns `-1` if not found).
  ```python
  s = "hello"
  print(s.rfind('l'))  # Output: 3
  print(s.rfind('x'))  # Output: -1
  ```

---

### **`rindex(substring)`**
- Similar to `rfind()`, but raises an error if the substring is not found.
  ```python
  s = "hello"
  print(s.rindex('l'))  # Output: 3
  # print(s.rindex('x'))  # Raises ValueError
  ```

---

### **`rjust(width, fillchar)`**
- Right-justifies the string in a specified width, padding with a specified character.
  ```python
  s = "hello"
  print(s.rjust(10, '-'))  # Output: '-----hello'
  print(s.rjust(10))       # Output: '     hello'
  ```

---

### **`rpartition(separator)`**
- Splits the string into three parts, starting from the right.
  ```python
  s = "hello world"
  print(s.rpartition(' '))  # Output: ('hello', ' ', 'world')
  ```

---

### **`rsplit(separator)`**
- Splits the string into a list, starting from the right.
  ```python
  s = "hello world"
  print(s.rsplit(' '))  # Output: ['hello', 'world']
  ```

---

### **`splitlines(keepends)`**
- Splits the string at line breaks and returns a list of lines.
  ```python
  s = "hello\nworld"
  print(s.splitlines())  # Output: ['hello', 'world']
  ```

---

### **`startswith(prefix)`**
- Checks if the string starts with the specified prefix.
  ```python
  s = "hello"
  print(s.startswith('h'))  # Output: True
  print(s.startswith('x'))  # Output: False
  ```

---

### **`swapcase()`**
- Swaps the case of all characters in the string.
  ```python
  s = "Hello World"
  print(s.swapcase())  # Output: 'hELLO wORLD'
  ```

---

### **`translate(table)`**
- Translates the string using a translation table (created with `maketrans()`).
  ```python
  trans = str.maketrans('aeiou', '12345')
  s = "hello"
  print(s.translate(trans))  # Output: 'h2ll4'
  ```

---

### **`zfill(width)`**
- Pads the string with zeros on the left until it reaches the specified width.
  ```python
  s = "42"
  print(s.zfill(5))  # Output: '00042'
  ```

---


## **6.8 The `string` Module**

The `string` module in Python provides a collection of useful constants and functions for working with strings. Below is a breakdown of the most commonly used components.

---

### **6.8.1 Constants in the `string` Module**

| Constant            | Description                                                                 | Example                     |
|---------------------|-----------------------------------------------------------------------------|-----------------------------|
| **`ascii_letters`** | A string containing all ASCII letters (both lowercase and uppercase).       | `'abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ'` |
| **`ascii_lowercase`** | A string containing all lowercase ASCII letters.                           | `'abcdefghijklmnopqrstuvwxyz'` |
| **`ascii_uppercase`** | A string containing all uppercase ASCII letters.                           | `'ABCDEFGHIJKLMNOPQRSTUVWXYZ'` |
| **`digits`**        | A string containing all decimal digits.                                     | `'0123456789'`              |
| **`hexdigits`**     | A string containing all hexadecimal digits.                                 | `'0123456789abcdefABCDEF'`  |
| **`octdigits`**     | A string containing all octal digits.                                       | `'01234567'`                |
| **`printable`**     | A string containing all printable ASCII characters.                         | `'0123456789abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ!"#$%&\'()*+,-./:;<=>?@[\\]^_`{|}~ \t\n\r\x0b\x0c'` |
| **`punctuation`**   | A string containing all ASCII punctuation characters.                       | `'!"#$%&\'()*+,-./:;<=>?@[\\]^_`{|}~'` |
| **`whitespace`**    | A string containing all ASCII whitespace characters.                        | `' \t\n\r\x0b\x0c'`         |

---

### **6.8.2 Functions in the `string` Module**

#### **`capwords(s, sep=None)`**
- Capitalizes each word in a string, optionally using a specified separator.
  ```python
  import string
  s = "hello world"
  print(string.capwords(s))  # Output: 'Hello World'
  ```

---

### **6.8.3 Classes in the `string` Module**

#### **`string.Formatter`**
- A class for creating and customizing string formatting.
  ```python
  from string import Formatter
  formatter = Formatter()
  print(formatter.format("Hello, {name}!", name="Alice"))  # Output: 'Hello, Alice!'
  ```

#### **`string.Template`**
- A class for simple string substitution using `$`-based placeholders.
  ```python
  from string import Template
  t = Template("Hello, $name!")
  print(t.substitute(name="Alice"))  # Output: 'Hello, Alice!'
  ```

---

### **6.8.4 Examples of Using `string` Module Constants**

#### **Check if a String Contains Only Letters**
```python
import string

s = "HelloWorld"
print(all(c in string.ascii_letters for c in s))  # Output: True
```

#### **Check if a String Contains Only Digits**
```python
s = "12345"
print(all(c in string.digits for c in s))  # Output: True
```

#### **Check if a String Contains Only Punctuation**
```python
s = "!@#$"
print(all(c in string.punctuation for c in s))  # Output: True
```

#### **Remove All Whitespace from a String**
```python
s = "  Hello  World  "
print("".join(c for c in s if c not in string.whitespace))  # Output: 'HelloWorld'
```

---

### **6.8.5 Practical Use Cases**

#### **Generate a Random Password**
```python
import string
import random

def generate_password(length=8):
    chars = string.ascii_letters + string.digits + string.punctuation
    return ''.join(random.choice(chars) for _ in range(length))

print(generate_password(12))  # Output: Random password like 'aB3$fG7@kL9!'
```

#### **Validate a Hexadecimal String**
```python
def is_hex(s):
    return all(c in string.hexdigits for c in s)

print(is_hex("1a2f"))  # Output: True
print(is_hex("1g2f"))  # Output: False
```

---


<span style="display: flex; justify-content: space-between; width: 100%; align-items: center;">
    <a href="../05-module-05-debugging/README.md">
        <img src="https://img.shields.io/badge/Previous-Debugging-blue" width="200" height="35">
    </a>
    <a href="../07-module-07-lists/README.md">
        <img src="https://img.shields.io/badge/Next-Python_Lists-brightgreen" width="170" height="35">
    </a>
</span>
<br><br>
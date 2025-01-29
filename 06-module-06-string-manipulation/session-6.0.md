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


# String Slicing


|  s  |  t  |  r  |  i  |  n  |  g  |     |  s  |  l  |  i  |  c  |  i  |  n  |  g  |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
|  0  |  1  |  2  |  3  |  4  |  5  |  6  |  7  |  8  |  9  |  10 |  11 |  12 |  13 |
| -14 | -13 | -12 | -11 | -10 |  -9 | -8  | -7  | -6  | -5  | -4  | -3  | -2  | -1  |


### Basic String Slicing:
1. **Extract the substring from index 2 to index 5**:
   ```python
   s = "string slicing"
   s[2:6]  # "rin"
   ```

2. **Extract the first 3 characters**:
   ```python
   s = "string slicing"
   s[:3]  # "str"
   ```

3. **Extract the substring from the 3rd to the last character**:
   ```python
   s = "string slicing"
   s[2:]  # "ring slicing"
   ```

4. **Extract the last 4 characters**:
   ```python
   s = "string slicing"
   s[-4:]  # "cing"
   ```

5. **Extract from index 3 to index 8 with step 2**:
   ```python
   s = "string slicing"
   s[3:9:2]  # "rn"
   ```

### Slicing with Step Values:
6. **Slice the entire string with step 2 (every second character)**:
   ```python
   s = "string slicing"
   s[::2]  # "srg icn"
   ```

7. **Slice the string in reverse with step -1**:
   ```python
   s = "string slicing"
   s[::-1]  # "gnicils gnirts"
   ```

8. **Slice the string from the 2nd to the 6th character with step 2**:
   ```python
   s = "string slicing"
   s[1:6:2]  # "tr"
   ```

9. **Slice the string from the 4th character backwards with step -2**:
   ```python
   s = "string slicing"
   s[3::-2]  # "tns"
   ```

10. **Slice the string from index 5 to index 0 with step -1**:
    ```python
    s = "string slicing"
    s[5:0:-1]  # "gnirts"
    ```

### Negative Indexing:
11. **Slice the string from the 2nd last character to the end**:
    ```python
    s = "string slicing"
    s[-2:]  # "ng"
    ```

12. **Extract the substring from the 3rd character from the end to the 2nd character from the end**:
    ```python
    s = "string slicing"
    s[-3:-1]  # "in"
    ```

13. **Extract the last 3 characters**:
    ```python
    s = "string slicing"
    s[-3:]  # "ing"
    ```

14. **Slice the string with negative step, reverse it, and get every third character**:
    ```python
    s = "string slicing"
    s[::-3]  # "gcn"
    ```

### Working with Larger Strings:
15. **Extract every 3rd character from index 5 to index 15**:
    ```python
    s = "string slicing"
    s[5:15:3]  # "sni"
    ```

16. **Extract characters from index 7 to the second last character in reverse**:
    ```python
    s = "string slicing"
    s[7:-1:-1]  # "n"
    ```

17. **Extract the last 3 characters with negative step**:
    ```python
    s = "string slicing"
    s[-1:-4:-1]  # "gn"
    ```

### Combining Forward and Backward Slicing:
18. **Slice the first half and reverse it**:
    ```python
    s = "string slicing"
    s[:len(s)//2][::-1]  # "gnirts"
    ```

19. **Slice the second half and reverse it**:
    ```python
    s = "string slicing"
    s[len(s)//2:][::-1]  # "gnicils"
    ```

20. **Combine forward and reverse slices to get a specific pattern**:
    ```python
    s = "string slicing"
    s[::2] + s[::-3]  # "srg icn"
    ```

21. **Reverse the string and then slice it in steps of 2**:
    ```python
    s = "string slicing"
    s[::-1][::2]  # "gcnr"
    ```

### Practical Exercises:
22. **Extract the first word from the string**:
    ```python
    s = "string slicing"
    s.split()[0]  # "string"
    ```

23. **Extract the last word from the string**:
    ```python
    s = "string slicing"
    s.split()[-1]  # "slicing"
    ```

24. **Extract every third letter of the string**:
    ```python
    s = "string slicing"
    s[::3]  # "stsc"
    ```

25. **Reverse and extract every second character**:
    ```python
    s = "string slicing"
    s[::-1][::2]  # "gnns"
    ```

26. **Extract characters from the middle of the string**:
    ```python
    s = "string slicing"
    mid = len(s) // 2
    s[mid-2:mid+3]  # "li "
    ```

27. **Get the substring without the first and last characters**:
    ```python
    s = "string slicing"
    s[1:-1]  # "tring slicin"
    ```


# String Templating

```python
from string import Template
```

Then you create a `Template` object and use `substitute()` (or `safe_substitute()`) to replace placeholders in the string with values.

Example:

```python
from string import Template

# Create a template with placeholders
template = Template("Hello, my name is $name and I am $age years old.")

# Use substitute to fill in the values
greeting = template.substitute(name="Alice", age=30)
print(greeting)
```

### Difference Between `substitute()` and `safe_substitute()`:
- `substitute()`: If a placeholder is missing or undefined, it raises a `KeyError`.
- `safe_substitute()`: If a placeholder is missing, it leaves the placeholder unchanged instead of raising an error.

Example with `safe_substitute()`:

```python
greeting = template.safe_substitute(name="Alice")
print(greeting)  # Output: Hello, my name is Alice and I am $age years old.
```


# Maketrans 

The `maketrans()` method in Python is used to create a translation table that can be used with the `translate()` method to replace characters in a string.

### Syntax:
```python
str.maketrans(x, y)
```
- `x`: A string or a dictionary. If it’s a string, it’s a set of characters to be replaced.
- `y`: A string with the same length as `x`. Each character in `x` is replaced by the character in the same position in `y`.

### Example 1: Basic Character Replacement
```python
# Create a translation table
trans_table = str.maketrans("abc", "123")

# Use the translate method to replace characters
original = "abcdef"
result = original.translate(trans_table)

print(result)  # Output: "123def"
```
In this example, the characters `'a'`, `'b'`, and `'c'` are replaced by `'1'`, `'2'`, and `'3'` respectively.

### Example 2: Using `maketrans()` with a Dictionary
```python
# Create a translation table using a dictionary
trans_table = str.maketrans({"a": "1", "b": "2", "c": "3"})

# Use the translate method to replace characters
original = "abcxyz"
result = original.translate(trans_table)

print(result)  # Output: "123xyz"
```
Here, the dictionary specifies which characters should be replaced with what.

### Example 3: Replacing Multiple Characters
```python
# Replace vowels with other characters
trans_table = str.maketrans("aeiou", "12345")

# Apply the translation
text = "hello world"
translated_text = text.translate(trans_table)

print(translated_text)  # Output: "h2ll4 w4rld"
```
This example replaces the vowels 'a', 'e', 'i', 'o', 'u' with the digits '1', '2', '3', '4', '5'.

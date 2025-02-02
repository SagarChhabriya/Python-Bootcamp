# String Slicing

|  s  |  t  |  r  |  i  |  n  |  g  |     |  s  |  l  |  i  |  c  |  i  |  n  |  g  |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
|  0  |  1  |  2  |  3  |  4  |  5  |  6  |  7  |  8  |  9  |  10 |  11 |  12 |  13 |
| -14 | -13 | -12 | -11 | -10 |  -9 | -8  | -7  | -6  | -5  | -4  | -3  | -2  | -1  |



### Example 1: `s[start:end]` with +ve indexing

```python
s = "string slicing"

# Four possible combinations
s[ : ]      # "string slicing"
s[1: ]      # "tring slicing"
s[ :4]      # "stri"
s[1:4]      # "tri"
```
**Explanation of Outputs:**
- `s[:]`: The entire string is returned.
- `s[1:]`: The substring from index 1 to the end is returned, which is `"tring slicing"`.
- `s[:4]`: The substring from the start to index 3 is returned, which is `"stri"`.
- `s[1:4]`: The substring from index 1 to index 3 (excluding index 4) is returned, which is `"tri"`.

---

### Example 2: `s[start:end]` with -ve indexing

```python
s = "string slicing"

# Four possible combinations
s[  :  ]    # "string slicing"
s[-4:  ]    # "cing"
s[  :-1]    # "string slicin"
s[-4:-1]    # "cin"
```
**Explanation of Outputs:**
- `s[:]`: The entire string is returned.
- `s[-4:]`: The last 4 characters, `"cing"`, are returned.
- `s[:-1]`: The string excluding the last character is returned, which is `"string slicin"`.
- `s[-4:-1]`: The substring from the 4th last character to the second last character is returned, which is `"cin"`.

---

### Example 3: `s[start:end:step]` with +ve start, end, and +ve step

```python
s = "string slicing"

# Eight possible combinations
s[  :  :  ]     # "string slicing"
s[  :  : 2]     # "srn lcn"
s[  : 8:  ]     # "string s"
s[  : 8: 2]     # "srn "
s[1 :  :  ]     # "tring slicing"
s[1 :  : 2]     # "tigsiig"
s[1 :10:  ]     # "tring sli"
s[1 :12: 2]     # "tigsii"
```
**Explanation of Outputs:**
- `s[::]`: The entire string is returned.
- `s[::2]`: Every second character from the string is returned, which is `"srn lcn"`.
- `s[:8:]`: The first 8 characters of the string are returned, which is `"string s"`.
- `s[:8:2]`: Every second character from the first 8 characters is returned, which is `"srn "`.
- `s[1::]`: The string from index 1 to the end is returned, which is `"tring slicing"`.
- `s[1::2]`: Every second character from index 1 to the end is returned, which is `"tigsiig"`.
- `s[1:10:]`: The string from index 1 to index 9 is returned, which is `"tring sli"`.
- `s[1:12:2]`: Every second character from index 1 to index 11 is returned, which is `"tigsii"`.

---

### Example 4: `s[start:end:step]` with +ve start, end, and -ve step

```python
s = "string slicing"

# Eight possible combinations
s[ : :-1]     # 'gnicils gnirts'  # Reverse of string
s[ : :-2]     # 'giisgit'         # Every second character from the reversed string
s[8:0:-1]     # 'ls gnirt'        # Slices from index 8 to index 1 (excluding index 0) backwards
s[8: :-1]     # 'ls gnirts'       # Slices from index 8 to the start backwards
s[8: :-2]     # 'l nrs'           # Every second character from index 8 to the start backwards
s[8: :-3]     # 'lgr'             # Every third character from index 8 to the start backwards
```
**Explanation of Outputs:**
- `s[::-1]`: The entire string is reversed, yielding `"gnicils gnirts"`.
- `s[::-2]`: Every second character from the reversed string is returned, yielding `"giisgit"`.
- `s[8:0:-1]`: The slice starts from index 8 and moves backwards, excluding index 0, yielding `"ls gnirt"`.
- `s[8::-1]`: Similar to the previous, but includes index 0, yielding `"ls gnirts"`.
- `s[8::-2]`: Every second character from index 8 moving backwards, yielding `"l nrs"`.
- `s[8::-3]`: Every third character from index 8 moving backwards, yielding `"lgr"`.

---


### Combining Forward and Backward Slicing:

#### **Slice the first half and reverse it**:

```python
s = "string slicing"
s[:len(s)//2][::-1]  # "gnirts"
```

**Step-by-Step Explanation:**

1. **First part: `s[:len(s)//2]`**
   - `len(s)` gives the length of the string `"string slicing"`, which is 14.
   - `len(s)//2` calculates the integer division of 14 by 2, which gives `7`. 
   - So `s[:7]` returns the first 7 characters of the string, which is `"string "`.

2. **Second part: `[::1]` on `s[:7]` (i.e., `'string '`):**
   - After slicing out `"string "`, we apply the reverse slicing `[::-1]`.
   - `[::-1]` reverses the string `"string "`, resulting in `"gnirts"`.

So the output is `"gnirts"`.

**Note:**
- `s[:len(s)//2]`: This slices the first half of the string.
- `[::1]` reverses the string `"string "`.
- By combining these two steps, we first slice a portion of the string and then reverse that portion.




### ** Slice the second half and reverse it:

```python
s = "string slicing"
s[len(s)//2:][::-1]  # "gnicils"
```

**Step-by-Step Explanation:**

1. **First part: `s[len(s)//2:]`**
   - `len(s)` gives the length of the string `"string slicing"`, which is 15.
   - `len(s)//2` calculates the integer division of 15 by 2, which gives `7`.
   - So, `s[7:]` slices from index 7 to the end, which gives `"slicing"`.

2. **Second part: `[::1]` on `s[7:]` (i.e., `'slicing'`)**
   - We reverse the string `"slicing"` using `[::-1]`.
   - Reversing `"slicing"` results in `"gnicils"`.

**Output:**
- The final result is `"gnicils"`.

**Note:**
- The first slice `s[len(s)//2:]` gets the second half of the string (`"slicing"`).
- The `[::-1]` reverses that second half, resulting in `"gnicils"`.
- This technique can be useful when you want to work with a specific portion of the string (e.g., the second half) and then reverse it.


### Combine forward and reverse slices to get a specific pattern:

```python
s = "string slicing"
s[::2] + s[::-3]  # 'srn lcngcsnt'
```

**Step-by-Step Explanation:**

1. **First part: `s[::2]`**
   - `s[::2]` takes every second character from the string, starting from the first character.
   - From `"string slicing"`, we get `'srn lcn'` (characters at positions 0, 2, 4, 6, 8, 10, 12).

2. **Second part: `s[::-3]`**
   - `s[::-3]` takes every third character from the string but in reverse order.
   - Reversing `"string slicing"` gives `"gnicils gnirts"`, and taking every third character results in `'gcsnt'` (characters at positions -1, -4, -7, -10, -13).

3. **Combining the two parts:**
   - The two slices are concatenated: `'srn lcn' + 'gcsnt'` gives `'srn lcngcsnt'`.

**Output:**
- The final result is `'srn lcngcsnt'`.


### Reverse the string and then slice it in steps of 2:

```python
s = "string slicing"
s[::-1][::2]  # 'giisgit'
```

**Step-by-Step Explanation:**

1. **First part: `s[::-1]`**
   - `s[::-1]` reverses the string `"string slicing"`, giving `"gnicils gnirts"`.

2. **Second part: `[::2]` on `s[::-1]` (i.e., `"gnicils gnirts"`)**
   - `s[::-1][::2]` takes every second character of the reversed string.
   - From `"gnicils gnirts"`, we get `'giisgit'` (characters at positions 0, 2, 4, 6, 8, 10, 12).

**Output:**
- The final result is `'giisgit'`.

**Note:**
- By reversing the string first and then slicing with a step of 2 (`[::2]`), you can extract characters in a specific pattern.
- This method can be useful when you want to manipulate a string both by reversing it and applying a specific step size to the result.

---



### Practical Exercises:
1. **Extract the first word from the string**:
    ```python
    s = "string slicing"

    s.split() # ['string', 'slicing']

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
    s[::3]  # 'si in'
    ```

25. **Reverse and extract every second character**:
    ```python
    s = "string slicing"
    s[::-1][::2]  # 'giisgit'
    ```

26. **Extract characters from the middle of the string**:
    ```python
    s = "string slicing"
    mid = len(s) // 2
    s[mid-2:mid+3]  # 'g sli'
    ```

27. **Get the substring without the first and last characters**:
    ```python
    s = "string slicing"
    s[1:-1]  # "tring slicin"
    ```


---


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

---

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



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



# 8. Tuples


<span style="display: flex; justify-content: space-between; width: 100%; align-items: center;">
    <a href="../07-module-07-lists/README.md">
        <img src="https://img.shields.io/badge/Previous-Python_Lists-blue" width="200" height="35">
    </a>
    <a href="../09-module-09-dictionaries/README.md">
        <img src="https://img.shields.io/badge/Next-Python_Dictionaries-brightgreen" width="200" height="35">
    </a>
</span>
<br><br>


## 8.1 Introduction to Tuples
Tuples are immutable sequences in Python. They are used to store a collection of items that should not be changed after creation. Since tuples are immutable, they offer benefits like performance optimization and protection from accidental modification. Tuples also allow duplicates.

- **Characteristics of Tuples**:
  - Immutable: Once created, the elements of a tuple cannot be modified, added, or removed.
  - Ordered: Tuples maintain the order of elements.
  - Can contain mixed data types: Tuples can hold different data types (e.g., integers, strings, lists).
  - Hashable: Because they are immutable, tuples can be used as keys in dictionaries.

- **Comparison with Lists**:
  - Lists are mutable (you can change, add, or remove elements).
  - Tuples are faster and use less memory than lists because of their immutability.

- **Why Use Tuples?**:
  - **Performance**: Tuples are faster than lists for iteration and memory consumption.
  - **Immutability**: Their immutability ensures data integrity, making them safer to use in certain situations.

---

## 8.2 Creating Tuples
You can create tuples in multiple ways in Python.

- **Using literals**:
  A tuple is created by placing a sequence of elements within parentheses.

  ```python
  # Example
  my_tuple = (1, 2, 3, 4)
  print(my_tuple)
  ```

- **Using the `tuple()` constructor**:
  You can also create a tuple by passing an iterable (like a list or string) to the `tuple()` function.

  ```python
  my_list = [1, 2, 3, 4]
  my_tuple = tuple(my_list)
  print(my_tuple)
  ```

---

## 8.3 Single-item and Multiple-item Tuples

### Single-item Tuples
To create a tuple with a single element, you must add a comma after the element. Without the comma, Python treats the parentheses as a grouping operator.

```python
# Single-item tuple
single_item_tuple = (5,)
print(type(single_item_tuple))  # <class 'tuple'>
```

Without the comma, Python would treat it as a regular integer:

```python
# Not a tuple
not_a_tuple = (5)
print(type(not_a_tuple))  # <class 'int'>
```

### Multiple-item Tuples
Multiple items are separated by commas within parentheses:

```python
# Multiple-item tuple
multi_item_tuple = (1, 'apple', 3.14, True)
print(multi_item_tuple)
```

---

## 8.4 Packing and Unpacking Tuples

### Packing Multiple Values into a Tuple
Packing refers to the process of placing multiple values inside a tuple. Python automatically packs the values when you use parentheses.

```python
# Packing
packed_tuple = 1, 2, 3
print(packed_tuple)
```

### Unpacking Tuple Elements into Variables
Unpacking is the process of extracting elements from a tuple and assigning them to individual variables.

```python
# Unpacking
a, b, c = (1, 2, 3)
print(a, b, c)  # Output: 1 2 3
```

### Extended Unpacking
With extended unpacking, you can capture any remaining elements in a list while unpacking a tuple.

```python
# Extended Unpacking
a, *rest = (1, 2, 3, 4, 5)
print(a)       # Output: 1
print(rest)    # Output: [2, 3, 4, 5]
```

---

## 8.5 Accessing Tuple Elements
You can access tuple elements using indexing and slicing.

### Indexing (Positive and Negative Indexing)
- **Positive indexing** starts at 0 for the first element.
- **Negative indexing** starts from -1 for the last element.

```python
# Positive indexing
my_tuple = (10, 20, 30, 40)
print(my_tuple[0])  # Output: 10

# Negative indexing
print(my_tuple[-1])  # Output: 40
```

### Accessing Individual Elements
You can access individual elements with their respective index:

```python
print(my_tuple[1])  # Output: 20
```

### Using Slicing to Access Multiple Elements
Slicing allows you to extract a part of the tuple.

```python
# Slicing
print(my_tuple[1:3])  # Output: (20, 30)
print(my_tuple[:2])   # Output: (10, 20)
```

---

## 8.6 Modifying Tuples
Although tuples themselves are immutable, you can still perform certain operations like concatenation and replication.

### Why Tuples are Immutable
Tuples are immutable because they provide data integrity. Once created, the elements cannot be changed, added, or deleted.

### Tuple Operations: Concatenation, Replication
You can concatenate and replicate tuples to form new tuples.

```python
# Concatenation
tuple1 = (1, 2)
tuple2 = (3, 4)
result = tuple1 + tuple2
print(result)  # Output: (1, 2, 3, 4)

# Replication
replicated = (1, 2) * 3
print(replicated)  # Output: (1, 2, 1, 2, 1, 2)
```

### Tuple Slicing and Changing References
While you can't modify a tuple directly, you can create a new tuple with modified contents via slicing.

```python
original_tuple = (1, 2, 3)
modified_tuple = original_tuple[:2] + (4,)
print(modified_tuple)  # Output: (1, 2, 4)
```

---

## 8.7 Limitations of Tuples
- **Immutable Nature**: Once a tuple is created, you cannot change its contents. 
  - You can create a new tuple to replace the original one, but you cannot modify the elements within an existing tuple.

- **Why Immutability Can Be Useful**:
  - Immutability makes tuples safer for concurrent programming because the data is not subject to change.
  - They can be used as dictionary keys, unlike lists.

---

## 8.8 Tuple Functions and Methods

- **`count()`**: Returns the number of occurrences of a specified value in the tuple.
  
  ```python
  my_tuple = (1, 2, 3, 2, 2)
  print(my_tuple.count(2))  # Output: 3
  ```

- **`index()`**: Returns the index of the first occurrence of a specified value.

  ```python
  print(my_tuple.index(2))  # Output: 1
  ```

---

## 8.9 Deleting Elements

- **Deleting Tuples with `del`**:
  You can delete the entire tuple with the `del` statement. However, you cannot delete individual elements from a tuple.

  ```python
  my_tuple = (1, 2, 3)
  del my_tuple
  # print(my_tuple)  # This will raise an error: NameError: name 'my_tuple' is not defined
  ```

- **Deleting Specific Elements**: Since tuples are immutable, you cannot delete individual elements from them directly. You can, however, recreate a new tuple without the unwanted elements.

---

## 8.10 Reassigning Tuples
Tuples are immutable, so you can't change their values directly. However, you can create a new tuple and assign it to the same variable or a new variable.

```python
# Reassigning a tuple
my_tuple = (1, 2, 3)
my_tuple = (4, 5, 6)  # Reassigning with a new tuple
print(my_tuple)  # Output: (4, 5, 6)
```

---

## 8.11 Tuples and Performance
Tuples have a lower memory overhead and are faster than lists because they are immutable. This makes them particularly useful for situations where you need to iterate over data frequently or store fixed data.

- **Memory Efficiency**:
  Tuples use less memory than lists because they are static in size, meaning the Python interpreter doesn't need to allocate additional memory to manage dynamic resizing as it does with lists.

- **Speed**:
  Since tuples are immutable, they can be optimized by the Python runtime for faster access and iteration.

---

## 8.12 Tuple as Keys in Dictionaries
Since tuples are immutable, they can be used as keys in dictionaries. Lists, however, cannot be used as dictionary keys because they are mutable.

```python
# Tuple as a key in a dictionary
my_dict = { (1, 2): "value1", (3, 4): "value2" }
print(my_dict[(1, 2)])  # Output: value1
```

In contrast, using a list as a key would raise a `TypeError`:

```python
# List as a key (will raise an error)
my_dict = { [1, 2]: "value1" }  # TypeError: unhashable type: 'list'
```



<br><br>

<span style="display: flex; justify-content: space-between; width: 100%; align-items: center;">
    <a href="../07-module-07-lists/README.md">
        <img src="https://img.shields.io/badge/Previous-Python_Lists-blue" width="200" height="35">
    </a>
    <a href="../09-module-09-dictionaries/README.md">
        <img src="https://img.shields.io/badge/Next-Python_Dictionaries-brightgreen" width="200" height="35">
    </a>
</span>
<br><br>
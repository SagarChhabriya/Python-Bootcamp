# Python Lists: Basic Concepts and Operations


<span style="display: flex; justify-content: space-between; width: 100%; align-items: center;">
    <a href="../06-module-06-string-manipulation/README.md">
        <img src="https://img.shields.io/badge/Previous-Debugging-blue" width="200" height="35">
    </a>
    <a href="../08-module-08-tuples/README.md">
        <img src="https://img.shields.io/badge/Next-Python_Lists-brightgreen" width="170" height="35">
    </a>
</span>
<br><br>


## 7.1 Introduction to Python Lists
A list in Python is a collection of ordered, mutable (changeable) items. Lists can store elements of different data types, including numbers, strings, and other objects.

### Characteristics of Lists:
- **Ordered**: Items have a specific order and can be accessed by their position.
- **Mutable**: Elements of a list can be modified after the list is created.
- **Indexed**: Items in a list are indexed, starting from 0.
- **Heterogeneous**: Lists can hold items of different data types.

## 7.2 Creating and Accessing Lists

### Creating Lists
You can create lists using different methods:

1. **Using List Literals**:
   ```python
   my_list = [1, 2, 3, "apple", 4.5]
   ```
   
2. **Using the `list()` Constructor**:
   ```python
   my_list = list([1, 2, 3, "apple", 4.5])
   ```

3. **Empty List**:
   ```python
   empty_list = []
   ```

### Accessing List Elements
You can access elements in a list using **indexing**.

### Indexing:
- **Positive Indexing**: Starts from 0 for the first element.
  ```python
  my_list = [10, 20, 30, 40]
  print(my_list[0])  # Output: 10
  ```

- **Negative Indexing**: Starts from -1 for the last element.
  ```python
  print(my_list[-1])  # Output: 40
  ```

### Accessing Individual Elements:
To access an element:
```python
print(my_list[1])  # Output: 20
```

## 7.3 Modifying Lists
You can modify lists in several ways:

1. **Joining Lists**:
   ```python
   list1 = [1, 2, 3]
   list2 = [4, 5, 6]
   combined = list1 + list2
   print(combined)  # Output: [1, 2, 3, 4, 5, 6]
   ```

2. **Replicating Lists**:
   ```python
   repeated = [1, 2] * 3
   print(repeated)  # Output: [1, 2, 1, 2, 1, 2]
   ```

3. **List Slicing**:
   ```python
   my_list = [10, 20, 30, 40, 50]
   print(my_list[1:4])  # Output: [20, 30, 40]
   ```

## 7.4 Common List Methods

1. **`append()`**: Adds an element at the end of the list.
   ```python
   my_list.append(60)
   ```

2. **`pop()`**: Removes and returns the last element.
   ```python
   last_item = my_list.pop()
   ```

3. **`sort()`**: Sorts the list in ascending order.
   ```python
   my_list.sort()
   ```

4. **`count()`**: Counts how many times an element appears in the list.
   ```python
   count = my_list.count(10)
   ```

5. **`index()`**: Returns the index of the first occurrence of an element.
   ```python
   index = my_list.index(20)
   ```

6. **`insert()`**: Inserts an element at a specified index.
   ```python
   my_list.insert(2, 15)  # Insert 15 at index 2
   ```

7. **`remove()`**: Removes the first occurrence of an element.
   ```python
   my_list.remove(20)
   ```

### Prepending Elements:
Use `insert()` or list concatenation to prepend items:
```python
my_list.insert(0, "new_first_element")
```

## 7.5 List Comprehension
List comprehension provides a concise way to create lists.

### Syntax:
```python
new_list = [expression for item in iterable if condition]
```

### Example:
```python
squares = [x ** 2 for x in range(5)]  # Output: [0, 1, 4, 9, 16]
```

## 7.6 List Mutation and Packing/Unpacking
Lists are **mutable**, meaning you can change their elements in place.

Example:
```python
my_list[0] = 100  # Modifying the first element
print(my_list)  # Output: [100, 20, 30, 40, 50]
```

### Packing and Unpacking Lists
- **Packing**: Multiple elements packed into a list.
  ```python
  packed = [1, 2, 3]
  ```

- **Unpacking**: Assigning list elements to variables.
  ```python
  a, b, c = packed
  print(a, b, c)  # Output: 1 2 3
  ```

## 7.9 Limitations and Iteration 

### Limitations of Lists
- Lists **cannot** hold immutable elements (e.g., tuples, sets).
- Lists have a **fixed size** when created but can grow or shrink dynamically.
- Lists are not the most efficient for large-scale data due to their performance considerations.

### Iteration over Lists
You can iterate over a list using a `for` loop or list comprehension.

### Example with `for` Loop:
```python
for item in my_list:
    print(item)
```

### Example with List Comprehension:
```python
squared = [x**2 for x in my_list if isinstance(x, int)]
```

## 7.8 Membership and Concatenation

### Membership Operators
Check if an element is present in a list using the `in` and `not in` operators.

### Example:
```python
print(10 in my_list)  # Output: True or False
print(100 not in my_list)  # Output: True
```

### List Concatenation
You can combine multiple lists using `+` or `extend()`.

#### Using `+`:
```python
list1 = [1, 2]
list2 = [3, 4]
combined = list1 + list2  # Output: [1, 2, 3, 4]
```

#### Using `extend()`:
```python
list1.extend(list2)  # List1 is now [1, 2, 3, 4]
```

## 7.9 Multi-dimensional Lists
A multi-dimensional list (nested list) is a list containing other lists as elements.

### Example:
```python
matrix = [[1, 2], [3, 4], [5, 6]]
print(matrix[1])  # Output: [3, 4]
print(matrix[1][0])  # Output: 3
```

## 7.10 Deleting and Reassigning Elements

### Deleting Elements
You can delete elements from a list using `del`, `pop()`, or `remove()`.

1. **`del`**:
   ```python
   del my_list[2]  # Deletes the element at index 2
   ```

2. **`pop()`**: Removes and returns an element from the list.
   ```python
   item = my_list.pop(2)  # Removes element at index 2
   ```

3. **`remove()`**: Removes the first occurrence of a value.
   ```python
   my_list.remove(20)
   ```

### Reassigning List Elements
You can reassign values to specific indexes.

### Example:
```python
my_list[2] = 99  # Change the element at index 2
```

## 7.11 Advanced List Operations

### Copying Lists

- **Shallow Copy**:
  - Creates a new list but references the same objects.
  ```python
  original = [1, 2, 3]
  copy = original.copy()  # or copy = original[:]
  print(copy)  # Output: [1, 2, 3]
  ```

- **Deep Copy**:
  - Creates a new list and recursively copies all objects within it.
  ```python
  import copy
  original = [[1, 2], [3, 4]]
  deep_copy = copy.deepcopy(original)
  print(deep_copy)  # Output: [[1, 2], [3, 4]]
  ```

---

### List Equality and Identity

- **Equality (`==`)**:
  - Checks if two lists have the same elements in the same order.
  ```python
  list1 = [1, 2, 3]
  list2 = [1, 2, 3]
  print(list1 == list2)  # Output: True
  ```

- **Identity (`is`)**:
  - Checks if two lists refer to the same object in memory.
  ```python
  print(list1 is list2)  # Output: False
  ```

---

## List as Stack or Queue

- **Stack (LIFO)**:
  - Use `append()` to push and `pop()` to pop.
  ```python
  stack = []
  stack.append(1)  # Push
  stack.append(2)
  print(stack.pop())  # Pop: Output: 2
  ```

- **Queue (FIFO)**:
  - Use `append()` to enqueue and `pop(0)` to dequeue.
  ```python
  queue = []
  queue.append(1)  # Enqueue
  queue.append(2)
  print(queue.pop(0))  # Dequeue: Output: 1
  ```

---

## List Filtering

- **Using `filter()`**:
  - Filters elements based on a condition.
  ```python
  numbers = [1, 2, 3, 4, 5]
  even_numbers = list(filter(lambda x: x % 2 == 0, numbers))
  print(even_numbers)  # Output: [2, 4]
  ```

- **Using List Comprehension**:
  ```python
  even_numbers = [x for x in numbers if x % 2 == 0]
  print(even_numbers)  # Output: [2, 4]
  ```

---

## List Sorting

- **Sorting in Place**:
  ```python
  numbers = [3, 1, 4, 2]
  numbers.sort()  # Output: [1, 2, 3, 4]
  ```

- **Sorting with a Key**:
  ```python
  words = ["apple", "banana", "cherry"]
  words.sort(key=len)  # Sort by length: Output: ['apple', 'cherry', 'banana']
  ```

- **Returning a Sorted List**:
  ```python
  sorted_numbers = sorted(numbers)  # Output: [1, 2, 3, 4]
  ```

---

## List Reversal

- **Reversing in Place**:
  ```python
  numbers = [1, 2, 3]
  numbers.reverse()  # Output: [3, 2, 1]
  ```

- **Returning a Reversed List**:
  ```python
  reversed_numbers = numbers[::-1]  # Output: [3, 2, 1]
  ```

---

## List to String Conversion

- **Using `join()`**:
  ```python
  words = ["Hello", "World"]
  sentence = " ".join(words)  # Output: 'Hello World'
  ```

---

## List to Other Data Structures

- **List to Tuple**:
  ```python
  my_list = [1, 2, 3]
  my_tuple = tuple(my_list)  # Output: (1, 2, 3)
  ```

- **List to Set**:
  ```python
  my_set = set(my_list)  # Output: {1, 2, 3}
  ```

- **List to Dictionary**:
  ```python
  my_dict = dict(zip(["a", "b", "c"], my_list))  # Output: {'a': 1, 'b': 2, 'c': 3}
  ```

---

## 7.12 Performance and Best Practices

### List Performance Considerations

- **Time Complexity**:
  - **Access**: O(1) (constant time for indexing).
  - **Append**: O(1) (amortized constant time).
  - **Insert/Delete**: O(n) (linear time for middle elements).
  - **Search**: O(n) (linear time for unsorted lists).

- **Space Complexity**:
  - Lists use contiguous memory, which can lead to inefficiencies for large datasets.

---

### List vs Other Data Structures

- **Lists vs Tuples**:
  - Lists are mutable; tuples are immutable.
  - Lists are better for dynamic data; tuples are better for fixed data.
  

- **Lists vs Sets**:
  - Lists allow duplicates and maintain order; sets do not.
  - Sets are faster for membership tests (`in` operator).

- **Lists vs Dictionaries**:
  - Lists are indexed by integers; dictionaries are indexed by keys.
  - Dictionaries are faster for lookups by key.

---

### List Aliasing

- **Aliasing**:
  - When two variables reference the same list object.
  ```python
  list1 = [1, 2, 3]
  list2 = list1
  list2[0] = 99
  print(list1)  # Output: [99, 2, 3] (list1 is also modified)
  ```

---



### List as Function Arguments

- **Mutable Default Arguments**:
  - Avoid using mutable default arguments (e.g., lists) in functions.
  ```python
  def add_item(item, my_list=[]):
      my_list.append(item)
      return my_list

  print(add_item(1))  # Output: [1]
  print(add_item(2))  # Output: [1, 2] (unexpected behavior)
  ```

---


### Indexing Errors
Trying to access an index that doesn't exist will raise an `IndexError`.

### Example:
```python
my_list = [10, 20, 30]
print(my_list[5])  # Raises IndexError: list index out of range
```

### Nested List Comprehension
You can use list comprehensions inside other list comprehensions for multi-dimensional lists.

### Example:
```python
matrix = [[1, 2], [3, 4], [5, 6]]
flat = [item for sublist in matrix for item in sublist]
# Output: [1, 2, 3, 4, 5, 6]
```

###  `clear()` Method
Removes all elements from the list.

### Example:
```python
my_list.clear()  # Removes all elements from the list
```


### Using `*args` to Accept List-like Arguments
In function definitions, you can use `*args` to accept a variable number of arguments as a list.

### Example:
```python
def print_elements(*args):
    for arg in args:
        print(arg)

print_elements(1, 2, 3)  # Output: 1 2 3
```


### `max()` and `min()` Functions
You can use `max()` and `min()` to find the largest and smallest elements in a list.

### Example:
```python
max_value = max(my_list)
min_value = min(my_list)
```


### List Memory Management
- **Garbage Collection**: Python automatically frees memory for unused lists.
- **Explicit Deletion**: Use `del` to delete a list explicitly.
  ```python
  del list1
  ```
<br><br>
<br><br>

<span style="display: flex; justify-content: space-between; width: 100%; align-items: center;">
    <a href="../06-module-06-string-manipulation/README.md">
        <img src="https://img.shields.io/badge/Previous-Debugging-blue" width="200" height="35">
    </a>
    <a href="../08-module-08-tuples/README.md">
        <img src="https://img.shields.io/badge/Next-Python_Lists-brightgreen" width="170" height="35">
    </a>
</span>
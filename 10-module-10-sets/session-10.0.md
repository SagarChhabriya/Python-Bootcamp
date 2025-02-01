# 10. Set and Frozenset

<span style="display: flex; justify-content: space-between; width: 100%; align-items: center;">
    <a href="../09-module-09-dictionaries/README.md">
        <img src="https://img.shields.io/badge/Previous-Python_Dictionaries-blue" width="250" height="35">
    </a>
    <!-- <a href="../11-module-11-nested-data-structures/README.md">
        <img src="https://img.shields.io/badge/Next-Nested_Data_Structures-brightgreen" width="270" height="35">
    </a> -->
</span>
<br><br>

## 10.1 Introduction to Set and Frozenset

### **Characteristics and Differences Between Set and Frozenset**
- **Set**:
  - **Unordered**: Elements have no specific order and are not indexed.
  - **Mutable**: Can add, remove, or update elements.
  - **Unique elements**: Duplicate elements are not allowed in a set.
  - **Not hashable**: Since sets are mutable, they cannot be used as keys in dictionaries or added to other sets.
  - **Use cases**: Remove duplicates from a collection, test for membership, perform set operations like union, intersection, and difference.
  
  Example:
  ```python
  my_set = {1, 2, 3, 3}  # {1, 2, 3} (duplicate '3' is removed)
  ```
  
- **Frozenset**:
  - **Unordered**: Like sets, frozensets do not maintain any order.
  - **Immutable**: Once created, elements cannot be added or removed.
  - **Hashable**: Since frozensets are immutable, they are hashable and can be used as keys in dictionaries or elements in other sets.
  - **Use cases**: Used in situations that require an immutable collection (e.g., as dictionary keys, or in sets of sets).

  Example:
  ```python
  frozen_set = frozenset([1, 2, 3])  # frozenset({1, 2, 3})
  ```

---

## 10.2 Creating Sets and Frozensets

### **Creating Sets**
- **Set Literals**: You can define a set directly using curly braces `{}`.
  ```python
  my_set = {1, 2, 3}
  ```

- **Using `set()` Constructor**: You can create a set from any iterable (list, tuple, string, etc.).
  ```python
  list_example = [1, 2, 3]
  set_from_list = set(list_example)  # {1, 2, 3}
  
  string_example = "hello"
  set_from_string = set(string_example)  # {'h', 'e', 'l', 'o'}
  ```

- **From Dictionaries**: When passing a dictionary to `set()`, it creates a set of the dictionary's keys.
  ```python
  dict_example = {"a": 1, "b": 2}
  set_from_dict = set(dict_example)  # {'a', 'b'}
  ```

### **Creating Frozensets**
- **Using `frozenset()` Constructor**: Frozensets are created using the `frozenset()` constructor, and like sets, they can be made from iterables.
  ```python
  frozen_set_example = frozenset([1, 2, 3])  # frozenset({1, 2, 3})
  ```

- **Creating from a Tuple**:
  ```python
  tuple_example = (1, 2, 3)
  frozen_set_from_tuple = frozenset(tuple_example)  # frozenset({1, 2, 3})
  ```

---

## 10.3 Accessing Elements in Sets

- **Unordered Nature of Sets**: 
  - Since sets are unordered collections, they do not support indexing, slicing, or accessing elements by position like lists or tuples.

- **Iteration over Sets**:
  - To access all elements, you must iterate through the set using a `for` loop.
  ```python
  my_set = {1, 2, 3}
  for element in my_set:
      print(element)
  ```

- **Checking Membership**:
  - You can check if an element exists in a set using the `in` keyword.
  ```python
  2 in my_set  # Returns True
  4 in my_set  # Returns False
  ```

---

## 10.4 Joining Sets

### **Set Operations**:
Sets in Python support several operations, such as union, intersection, difference, and symmetric difference.

- **Union (`|`)**: Combines elements from two or more sets, removing duplicates.
  ```python
  set1 = {1, 2, 3}
  set2 = {3, 4, 5}
  union_set = set1 | set2  # {1, 2, 3, 4, 5}
  ```

- **Intersection (`&`)**: Returns elements that are present in both sets.
  ```python
  intersection_set = set1 & set2  # {3}
  ```

- **Difference (`-`)**: Returns elements that are in the first set but not in the second.
  ```python
  difference_set = set1 - set2  # {1, 2}
  ```

- **Symmetric Difference (`^`)**: Returns elements that are in either of the sets, but not in both.
  ```python
  symmetric_diff_set = set1 ^ set2  # {1, 2, 4, 5}
  ```

- **Method Equivalents**:
  - `.union()`, `.intersection()`, `.difference()`, `.symmetric_difference()`
  ```python
  union_set = set1.union(set2)  # {1, 2, 3, 4, 5}
  ```

---

## 10.5 Replicating and Slicing Sets

- **Slicing**: 
  - Sets do not support slicing as they are unordered. You cannot slice a set like a list or tuple.
  
- **Replicating Sets**:
  - While sets cannot be "replicated" in the same way lists can (because they do not allow duplicates), you can use the `copy()` method to create a duplicate set.
  ```python
  original_set = {1, 2, 3}
  copied_set = original_set.copy()  # {1, 2, 3}
  ```

- **Replicating by Multiplying**:
  - Multiplying a set does not duplicate elements. It only replicates the set itself (which still maintains unique elements).
  ```python
  replicated_set = original_set * 2  # {1, 2, 3}
  ```

---

## 10.6 Mutation in Sets

- **Modifying Sets**:
  - **Adding Elements**:
    - `add()` adds a single element to a set.
    ```python
    my_set = {1, 2}
    my_set.add(3)  # {1, 2, 3}
    ```
  
  - **Adding Multiple Elements**:
    - `update()` adds multiple elements to a set from an iterable.
    ```python
    my_set.update([4, 5])  # {1, 2, 3, 4, 5}
    ```

  - **Removing Elements**:
    - `remove()` removes an element. If the element is not found, it raises a `KeyError`.
    ```python
    my_set.remove(3)  # {1, 2, 4, 5}
    ```

    - `discard()` removes an element but does not raise an error if the element is not found.
    ```python
    my_set.discard(6)  # No error, set remains the same
    ```

    - `pop()` removes and returns an arbitrary element from the set.
    ```python
    popped_item = my_set.pop()  # Removes and returns an arbitrary element
    ```

  - **Clearing the Set**:
    - `clear()` removes all elements from a set.
    ```python
    my_set.clear()  # {}
    ```

---

## 10.7 Packing and Unpacking Sets

- **Packing Sets**:
  - **Adding Multiple Items**: You can "pack" items into a set by adding them using the `update()` method.
  ```python
  packed_set = set()
  packed_set.update([1, 2, 3, 4])  # {1, 2, 3, 4}
  ```

- **Unpacking Sets**:
  - The `*` operator can be used to unpack the elements of a set into a function or another iterable.
  ```python
  def print_elements(*args):
      for item in args:
          print(item)
  
  print_elements(*packed_set)  # 1 2 3 4 (in arbitrary order)
  ```

---

## 10.8 Limitations of Sets and Frozensets

- **Sets**:
  - **Unordered**: Sets do not maintain any order of their elements.
  - **Mutable**: You can add, remove, and update elements of a set.
  - **Not hashable**: Since sets are mutable, they cannot be used as dictionary keys or added to other sets.
  
- **Frozensets**:
  - **Immutable**: Once created, frozensets cannot be changed.
  - **Hashable**: Frozensets are hashable, so they can be used as dictionary keys or elements in other sets.
  - **Performance Considerations**: Creating frozensets can be slightly slower than creating sets due to their immutability, but they are necessary when you need an immutable set.
  
  Example of frozenset in a set:

  ```python
  fs = frozenset([1,2])
  s = {fs}  # Frozenset can be added to a set
  ```

---

<span style="display: flex; justify-content: space-between; width: 100%; align-items: center;">
    <a href="../09-module-09-dictionaries/README.md">
        <img src="https://img.shields.io/badge/Previous-Python_Dictionaries-blue" width="250" height="35">
    </a>
    <!-- <a href="../11-module-11-nested-data-structures/README.md">
        <img src="https://img.shields.io/badge/Next-Nested_Data_Structures-brightgreen" width="270" height="35">
    </a> -->
</span>
<br><br>
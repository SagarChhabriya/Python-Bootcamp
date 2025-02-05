# 11. Nested Data Structures 

Nested data structures are collections (like lists, dictionaries, or tuples) that contain other collections as elements. They are useful for representing complex, hierarchical data.

---

## **11.1 Introduction to Nested Data Structures**
- **Definition**: A nested data structure is a collection (e.g., list, dictionary, tuple) that contains other collections as its elements.
- **Use Cases**:
  - Representing hierarchical data (e.g., organizational charts, file systems).
  - Storing multi-dimensional data (e.g., matrices, tables).
  - Modeling real-world relationships (e.g., user profiles with nested attributes).

---

## **11.2 Arrays**
- **Definition**: In Python, arrays are represented using lists.
- **Characteristics**:
  - Ordered, mutable, and can hold heterogeneous data types.
- **Example**:
  ```python
  my_array = [1, 2, 3, "apple", 4.5]
  ```

### **Operations on Arrays**:
- **Accessing Elements**:
  ```python
  print(my_array[0])  # Output: 1
  ```
- **Slicing**:
  ```python
  print(my_array[1:3])  # Output: [2, 3]
  ```
- **Concatenation**:
  ```python
  new_array = my_array + [5, 6]
  print(new_array)  # Output: [1, 2, 3, 'apple', 4.5, 5, 6]
  ```
- **Repetition**:
  ```python
  repeated_array = my_array * 2
  print(repeated_array)  # Output: [1, 2, 3, 'apple', 4.5, 1, 2, 3, 'apple', 4.5]
  ```

---

## **11.3 Array of Arrays (Lists of Lists)**
- **Definition**: A list where each element is itself a list.
- **Use Case**: Representing matrices or grids.
- **Example**:
  ```python
  matrix = [
      [1, 2, 3],
      [4, 5, 6],
      [7, 8, 9]
  ]
  ```

### **Operations on Arrays of Arrays**:
- **Accessing Elements**:
  ```python
  print(matrix[1][2])  # Output: 6 (Accessing the element in the 2nd row, 3rd column)
  ```
- **Modifying Elements**:
  ```python
  matrix[0][1] = 99
  print(matrix)  # Output: [[1, 99, 3], [4, 5, 6], [7, 8, 9]]
  ```
- **Iterating Through Rows and Columns**:
  ```python
  for row in matrix:
      for element in row:
          print(element, end=" ")
      print()
  ```

---

## **11.4 Arrays of Dictionaries**
- **Definition**: A list where each element is a dictionary.
- **Use Case**: Storing multiple records with key-value pairs.
- **Example**:
  ```python
  users = [
      {"name": "John", "age": 25},
      {"name": "Alice", "age": 30}
  ]
  ```

### **Operations on Arrays of Dictionaries**:
- **Accessing Elements**:
  ```python
  print(users[0]["name"])  # Output: John (Accessing the name of the first user)
  ```
- **Modifying Elements**:
  ```python
  users[1]["age"] = 31
  print(users)  # Output: [{'name': 'John', 'age': 25}, {'name': 'Alice', 'age': 31}]
  ```
- **Iterating Through Elements**:
  ```python
  for user in users:
      print(f"Name: {user['name']}, Age: {user['age']}")
  ```

---

## **11.5 Arrays of Tuples**
- **Definition**: A list where each element is a tuple.
- **Use Case**: Storing immutable sequences of data.
- **Example**:
  ```python
  coordinates = [
      (1, 2),
      (3, 4),
      (5, 6)
  ]
  ```

### **Operations on Arrays of Tuples**:
- **Accessing Elements**:
  ```python
  print(coordinates[1][0])  # Output: 3 (Accessing the first element of the second tuple)
  ```
- **Iterating Through Elements**:
  ```python
  for x, y in coordinates:
      print(f"X: {x}, Y: {y}")
  ```

---

## **11.6 Arrays as Values in Dictionaries**
- **Definition**: A dictionary where the values are lists.
- **Use Case**: Storing multiple values for a single key.
- **Example**:
  ```python
  student_grades = {
      "John": [85, 90, 78],
      "Alice": [92, 88, 95]
  }
  ```

### **Operations on Arrays as Values in Dictionaries**:
- **Accessing Elements**:
  ```python
  print(student_grades["John"][1])  # Output: 90 (Accessing John's second grade)
  ```
- **Modifying Elements**:
  ```python
  student_grades["Alice"][0] = 95
  print(student_grades)  # Output: {'John': [85, 90, 78], 'Alice': [95, 88, 95]}
  ```

---

## **11.8 Tuples as Values in Dictionaries**
- **Definition**: A dictionary where the values are tuples.
- **Use Case**: Storing immutable sequences of data as values.
- **Example**:
  ```python
  employee_details = {
      "John": ("Manager", 50000),
      "Alice": ("Developer", 45000)
  }
  ```

### **Operations on Tuples as Values in Dictionaries**:
- **Accessing Elements**:
  ```python
  print(employee_details["Alice"][0])  # Output: Developer (Accessing Alice's role)
  ```

---

## **11.9 Nested Dictionaries**
- **Definition**: A dictionary where the values are themselves dictionaries.
- **Use Case**: Representing hierarchical or tree-like data.
- **Example**:
  ```python
  company = {
      "CEO": {
          "name": "John",
          "age": 45,
          "team": {
              "Manager": "Alice",
              "Developer": "Bob"
          }
      }
  }
  ```

### **Operations on Nested Dictionaries**:
- **Accessing Elements**:
  ```python
  print(company["CEO"]["team"]["Developer"])  # Output: Bob
  ```
- **Modifying Elements**:
  ```python
  company["CEO"]["team"]["Developer"] = "Charlie"
  print(company)  # Output: {'CEO': {'name': 'John', 'age': 45, 'team': {'Manager': 'Alice', 'Developer': 'Charlie'}}}
  ```

---

## **11.10 Mixed Nested Structures**
- **Definition**: Combining lists, dictionaries, and tuples in a single structure.
- **Use Case**: Representing complex, real-world data.
- **Example**:
  ```python
  data = {
      "students": [
          {"name": "John", "grades": (85, 90, 78)},
          {"name": "Alice", "grades": (92, 88, 95)}
      ],
      "teachers": [
          {"name": "Mr. Smith", "subjects": ["Math", "Science"]},
          {"name": "Ms. Brown", "subjects": ["History", "English"]}
      ]
  }
  ```
 
### **Operations on Mixed Nested Structures**:
- **Accessing Elements**:
  ```python
  print(data["students"][0]["grades"][1])  # Output: 90 (Accessing John's second grade)
  ```
- **Modifying Elements**:
  ```python
  data["teachers"][1]["subjects"].append("Geography")
  print(data)  
  # Output: 
  #{ 
  #  'students': [
  #      {'name': 'John', 'grades': (85, 90, 78)}, 
  #      {'name': 'Alice', 'grades': (92, 88, 95)}
  #  ], 
  #  'teachers':[
  #      {'name': 'Mr. Smith', 'subjects': ['Math', 'Science']}, 
  #      {'name': 'Ms. Brown', 'subjects': ['History', 'English', 'Geography']}
  #  ]
  #}
  
  ```

---


## **11.11 Advanced Operations on Nested Data Structures**

### **1. Flattening Nested Lists**
- **Use Case**: Convert a nested list into a flat list.
- **Example**:
  ```python
  nested_list = [[1, 2], [3, 4], [5, 6]]
  flat_list = [item for sublist in nested_list for item in sublist]
  print(flat_list)  # Output: [1, 2, 3, 4, 5, 6]
  ```

---

### **2. Merging Nested Dictionaries**
- **Use Case**: Combine multiple dictionaries into one.
- **Example**:
  ```python
  dict1 = {"a": 1, "b": 2}
  dict2 = {"c": 3, "d": 4}
  merged_dict = {**dict1, **dict2}
  print(merged_dict)  # Output: {'a': 1, 'b': 2, 'c': 3, 'd': 4}
  ```

---

### **3. Sorting Nested Data**
- **Use Case**: Sort a list of dictionaries by a specific key.
- **Example**:
  ```python
  users = [
      {"name": "John", "age": 25},
      {"name": "Alice", "age": 30},
      {"name": "Bob", "age": 20}
  ]
  sorted_users = sorted(users, key=lambda x: x["age"])
  print(sorted_users)
  # Output: [{'name': 'Bob', 'age': 20}, {'name': 'John', 'age': 25}, {'name': 'Alice', 'age': 30}]
  ```
  > Read more on `lambda` function in functions module.


---

### **4. Filtering Nested Data**
- **Use Case**: Filter elements in a nested structure based on a condition.
- **Example**:
  ```python
  users = [
      {"name": "John", "age": 25},
      {"name": "Alice", "age": 30},
      {"name": "Bob", "age": 20}
  ]
  filtered_users = [user for user in users if user["age"] > 22]
  print(filtered_users)
  # Output: [{'name': 'John', 'age': 25}, {'name': 'Alice', 'age': 30}]
  ```

---

### **5. Deep Copying Nested Structures**
- **Use Case**: Create a completely independent copy of a nested structure.
- **Example**:
  ```python
  import copy
  original = [[1, 2], [3, 4]]
  deep_copy = copy.deepcopy(original)
  deep_copy[0][0] = 99
  print(original)  # Output: [[1, 2], [3, 4]]
  print(deep_copy)  # Output: [[99, 2], [3, 4]]
  ```

---

### **6. Checking for Existence in Nested Structures**
- **Use Case**: Check if a key or value exists in a nested dictionary or list.
- **Example**:
  ```python
  data = {
      "users": [
          {"name": "John", "age": 25},
          {"name": "Alice", "age": 30}
      ]
  }
  # Check if "Alice" exists in the nested structure
  exists = any(user["name"] == "Alice" for user in data["users"])
  print(exists)  # Output: True
  ```

  > Read more on `any` function in functions module.

---

### **7. Updating Nested Dictionaries**
- **Use Case**: Update a nested dictionary with another dictionary.
- **Example**:
  ```python
  original = {"a": 1, "b": {"c": 2, "d": 3}}
  update = {"b": {"c": 99, "e": 4}}
  original.update(update)
  print(original)  # Output: {'a': 1, 'b': {'c': 99, 'd': 3, 'e': 4}}
  ```

---

### **8. Recursive Operations on Nested Structures**
- **Use Case**: Perform operations recursively on deeply nested structures.
- **Example**:
  ```python
  def recursive_sum(nested_list):
      total = 0
      for element in nested_list:
          if isinstance(element, list):
              total += recursive_sum(element)
          else:
              total += element
      return total

  nested_list = [1, [2, [3, 4], 5], 6]
  print(recursive_sum(nested_list))  # Output: 21
  ```

  > Read more on `isinstance` function in functions module.

---

### **9. Converting Nested Structures to JSON**
- **Use Case**: Convert nested structures to JSON for serialization.
- **Example**:
  ```python
  import json
  data = {
      "users": [
          {"name": "John", "age": 25},
          {"name": "Alice", "age": 30}
      ]
  }
  json_data = json.dumps(data, indent=4)
  print(json_data)
  ```

---

### **10. Handling Missing Keys in Nested Dictionaries**
> Notes will be added soon.
<!-- - **Use Case**: Safely access nested keys without raising errors.
- **Example**:
  ```python
  from collections import defaultdict

  nested_dict = defaultdict(dict)
  nested_dict["a"]["b"] = 1
  print(nested_dict["a"]["b"])  # Output: 1
  print(nested_dict["x"]["y"])  # Output: {} (No KeyError)
  ``` -->

---

### **11. Using `zip()` with Nested Structures**
- **Use Case**: Combine multiple lists or dictionaries.
- **Example**:
  ```python
  keys = ["a", "b", "c"]
  values = [1, 2, 3]
  combined = dict(zip(keys, values))
  print(combined)  # Output: {'a': 1, 'b': 2, 'c': 3}
  ```

---

### **12. Using `map()` and `filter()` on Nested Structures**
- **Use Case**: Apply functions to nested structures.
- **Example**:
  ```python
  nested_list = [[1, 2], [3, 4], [5, 6]]
  flattened = list(map(lambda x: x[0], nested_list))
  print(flattened)  # Output: [1, 3, 5]
  ```

---

### **13. Using `reduce()` on Nested Structures**
- **Use Case**: Reduce nested structures to a single value.
- **Example**:
  ```python
  from functools import reduce
  nested_list = [[1, 2], [3, 4], [5, 6]]
  total = reduce(lambda acc, x: acc + sum(x), nested_list, 0)
  print(total)  # Output: 21
  ```

---

### **14. Using `itertools` for Nested Structures**
- **Use Case**: Perform advanced iterations on nested structures.
- **Example**:
  ```python
  import itertools
  nested_list = [[1, 2], [3, 4], [5, 6]]
  flattened = list(itertools.chain.from_iterable(nested_list))
  print(flattened)  # Output: [1, 2, 3, 4, 5, 6]
  ```

---




# 9. Dictionaries

<span style="display: flex; justify-content: space-between; width: 100%; align-items: center;">
    <a href="../08-module-08-tuples/README.md">
        <img src="https://img.shields.io/badge/Previous-Python_Tuples-blue" width="200" height="35">
    </a>
    <a href="../10-module-10-sets/README.md">
        <img src="https://img.shields.io/badge/Next-Python_Sets-brightgreen" width="170" height="35">
    </a>
</span>
<br><br>

## 9.1 Introduction to Dictionaries
Dictionaries are mutable, ordered collections of key-value pairs. They are commonly used for mapping values to unique keys, where the keys are hashable.

- **Characteristics and Use of Dictionaries in Python**:
  - Ordered collection of key-value pairs.
  - Keys must be unique, but values can be duplicated.
  - Commonly used for looking up data via keys, like a phone book or database index.

- **Comparison with Other Data Structures**:
  - Lists and Tuples store ordered data, but dictionaries store key-value pairs.
  - Unlike sets, dictionaries store a mapping of unique keys to values.

## 9.2 Properties of Dictionaries
Dictionaries have unique properties that make them different from other data structures.

- **Uniqueness of Keys**:
  - Dictionary keys must be unique. If you try to insert a duplicate key, the old value gets overwritten.

  ```python
  my_dict = {'a': 1, 'b': 2}
  my_dict['a'] = 3  # Overwrites the previous value for key 'a'
  print(my_dict)  # Output: {'a': 3, 'b': 2}
  ```

- **Values Can Be of Any Data Type**:
  - Values in dictionaries can be any data type, including lists, tuples, or even other dictionaries.

- **Order of Elements**:
  - As of Python 3.7+, dictionaries are ordered collections (the order of insertion is preserved). Prior to Python 3.7, dictionaries were unordered.

- **Key-Value Structure**:
  - The structure is a key-value pair, where the key is unique, and each key is associated with a value.

## 9.3 Accessing Values in Dictionaries
You can access values in dictionaries using keys.

- **Accessing Elements using Keys**:
  - You can directly access a value using its corresponding key.

  ```python
  my_dict = {'a': 1, 'b': 2, 'c': 3}
  print(my_dict['a'])  # Output: 1
  ```

- **Using `get()` for Safe Access**:
  - The `get()` method is useful when you want to access a key but avoid a `KeyError` if the key doesn't exist.

  ```python
  print(my_dict.get('a'))  # Output: 1
  print(my_dict.get('d'))  # Output: None (returns None if key does not exist)
  ```

- **Default Values with `get()`**:
  - You can also provide a default value to return if the key doesn’t exist.

  ```python
  print(my_dict.get('d', 0))  # Output: 0 (returns 0 if key 'd' is not found)
  ```

## 9.4 Methods in Dictionaries
Dictionaries come with several built-in methods that allow for easy manipulation of data.

- **Common Methods**:
  - `keys()`: Returns a view object that displays all keys in the dictionary.
  - `values()`: Returns a view object that displays all values in the dictionary.
  - `items()`: Returns a view object that displays all key-value pairs.
  - `get()`: Retrieves the value for the specified key (with an optional default value).
  - `pop()`: Removes and returns a value for the specified key.
  - `clear()`: Removes all items from the dictionary.
  - `copy()`: Returns a shallow copy of the dictionary.

  ```python
  my_dict = {'a': 1, 'b': 2}
  print(my_dict.keys())   # Output: dict_keys(['a', 'b'])
  print(my_dict.values()) # Output: dict_values([1, 2])
  print(my_dict.items())  # Output: dict_items([('a', 1), ('b', 2)])
  ```

- **Additional Methods**:
  - `setdefault()`: Returns the value if the key exists, or sets it with a default value if it doesn't.
  - `update()`: Updates the dictionary with elements from another dictionary or an iterable of key-value pairs.
  - `fromkeys()`: Creates a new dictionary with keys from an iterable and values set to a specified value.

  ```python
  # Using `setdefault()`
  my_dict.setdefault('a', 100)  # Will not change 'a', as it already exists
  my_dict.setdefault('d', 4)    # Adds key 'd' with value 4
  ```

- **Merging Dictionaries**:
  - You can merge two dictionaries using the `update()` method or the `**` unpacking operator.

  ```python
  dict1 = {'a': 1, 'b': 2}
  dict2 = {'c': 3, 'd': 4}
  dict1.update(dict2)  # Merges dict2 into dict1
  print(dict1)  # Output: {'a': 1, 'b': 2, 'c': 3, 'd': 4}

  dict3 = {**dict1, **dict2}  # Merging using `**` operator
  print(dict3)  # Output: {'a': 1, 'b': 2, 'c': 3, 'd': 4}
  ```

- **fromkeys()**
  ```python
  keys = ['a', 'b', 'c']
  value = 0
  new_dict = dict.fromkeys(keys, value)
  print(new_dict)
  ```


## 9.5 Dictionary Comprehension
Dictionary comprehension allows you to create dictionaries from iterable data in a concise and readable way.

- **Syntax**:
  ```python
  new_dict = {key: value for key, value in iterable}
  ```

- **Examples**:
  - Creating a dictionary from a list:

  ```python
  my_list = [(1, 'a'), (2, 'b'), (3, 'c')]
  my_dict = {k: v for k, v in my_list}
  print(my_dict)  # Output: {1: 'a', 2: 'b', 3: 'c'}
  ```

  - Filtering key-value pairs based on conditions:

  ```python
  my_dict = {x: x**2 for x in range(5)}
  print(my_dict)  # Output: {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}
  ```

## 9.6 Mutation in Dictionaries
Dictionaries are mutable, which means you can modify their contents.

- **How Dictionaries are Mutable**:
  - You can change, add, or remove key-value pairs after creation.

  ```python
  my_dict = {'a': 1, 'b': 2}
  my_dict['a'] = 10  # Modifies the value of 'a'
  my_dict['c'] = 3   # Adds a new key-value pair ('c': 3)
  print(my_dict)  # Output: {'a': 10, 'b': 2, 'c': 3}
  ```

- **Adding and Updating Key-Value Pairs**:
  - Add a new pair or update an existing key using assignment.

- **Nested Dictionaries**:
  - You can have dictionaries inside dictionaries, and you can mutate the inner dictionaries as well.

  ```python
  nested_dict = {'a': {'x': 1, 'y': 2}}
  nested_dict['a']['z'] = 3  # Adds key 'z' to the nested dictionary
  print(nested_dict)  # Output: {'a': {'x': 1, 'y': 2, 'z': 3}}
  ```

## 9.7 Packing and Unpacking Dictionaries

- **Packing Key-Value Pairs into a Dictionary**:
  - You can create dictionaries directly by specifying key-value pairs.

  ```python
  packed_dict = {'name': 'John', 'age': 25}
  ```

- **Unpacking with `**` Operator**:
  - The `**` operator can be used to unpack dictionaries when passing them as arguments to functions or merging them.

  ```python
  def print_info(**kwargs):
      print(kwargs)

  print_info(name="Alice", age=30)
  ```

- **Unpacking into variables**
  ```python

  # Unpacking into variables
  name, age = packed_dict.values()
  print(name, age)  # Output: John 25

  # Unpacking keys and values separately
  keys = {*packed_dict}
  values = {**packed_dict}
  print(keys)    # Output: {'name', 'age'}
  print(values)  # Output: {'name': 'John', 'age': 25}
  ```




## 9.8 Limitations of Dictionaries

- **Dictionaries are Unordered** (in versions prior to Python 3.7):
  - In Python versions earlier than 3.7, dictionaries were unordered. In Python 3.7+, dictionaries maintain insertion order.

- **Restrictions on Key Types**:
  - Keys must be hashable (immutable). For example, lists cannot be used as dictionary keys, but tuples can.

  ```python
  # This will raise a TypeError
  my_dict = {[1, 2]: 'value'}
  ```

- **Not Suitable for Storing Multiple Identical Keys**:
  - Since dictionary keys are unique, you cannot have multiple identical keys. The last value for a given key will overwrite previous ones.

## 9.9 Deleting Elements in Dictionaries

- **Using `del`, `pop()`, and `clear()` for Deletion**:
  - **`del`**: Deletes a specific key-value pair.

  ```python


  del my_dict['a']  # Deletes the key 'a'
  ```

  - **`pop()`**: Removes and returns the value for a specified key.

  ```python
  value = my_dict.pop('b')  # Removes key 'b' and returns its value
  ```

  - **`clear()`**: Removes all elements from the dictionary.

  ```python
  my_dict.clear()  # Clears the entire dictionary
  ```

## 9.10 Membership in Dictionaries

- **Checking Membership with `in` and `not in` Operators**:
  - You can check if a key exists in a dictionary.

  ```python
  my_dict = {'a': 1, 'b': 2}
  print('a' in my_dict)  # Output: True
  print('c' not in my_dict)  # Output: True
  ```

- **Checking Membership of Keys vs Values**:
  - You can use `in` to check for the presence of keys, but for values, you'll need to use the `values()` method.

  ```python
  print(1 in my_dict.values())  # Output: True
  ```


---

# 9.11 Use Cases and Real-World Applications

## **Storing Configurations, Caching, and Representing Data**

Dictionaries are commonly used in many real-world applications due to their efficiency and flexibility. Here are a few notable use cases:

### **1. Storing Configuration Settings**
   - **Scenario**: Many programs require the use of configuration settings, such as database credentials, feature flags, or user preferences.
   - **Why Dictionaries**: The key-value pair structure of dictionaries is a natural fit for configuration settings, as it allows quick retrieval of values based on known keys.
   
   **Example**:
   ```python
   config = {
       'host': 'localhost',
       'port': 8080,
       'use_ssl': True,
       'timeout': 30
   }

   print(config['host'])  # Output: 'localhost'
   print(config.get('timeout'))  # Output: 30
   ```
   In this example, the dictionary `config` is used to store various configuration parameters. The keys represent the configuration options, and the values represent their settings.

### **2. Caching Data**
   - **Scenario**: Caching is a technique used to store temporary data to improve the performance of an application. In scenarios like web scraping, API calls, or expensive computations, the result of an operation is cached so that it doesn't need to be recalculated.
   - **Why Dictionaries**: Since dictionary lookups have an average time complexity of O(1), they are ideal for caching data where speed is essential.
   
   **Example** (Memoization Pattern):
   ```python
   cache = {}

   def expensive_computation(n):
       if n in cache:
           return cache[n]
       # Simulate expensive computation
       result = n * 2  # Just an example computation
       cache[n] = result
       return result

   print(expensive_computation(10))  # Computation happens
   print(expensive_computation(10))  # Retrieved from cache
   ```

### **3. Representing Data**
   - **Scenario**: Dictionaries are often used to represent structured data, such as user profiles, product catalogs, or inventory.
   - **Why Dictionaries**: They provide a natural way to store and retrieve attributes, with the flexibility to handle varying data structures.

   **Example**:
   ```python
   user_profile = {
       'username': 'john_doe',
       'email': 'john@example.com',
       'age': 28,
       'active': True
   }

   print(user_profile['username'])  # Output: 'john_doe'
   ```

### **4. JSON-Like Data and API Responses**
   - **Scenario**: Many modern APIs return data in JSON format, which is essentially a collection of key-value pairs. This data is directly compatible with Python dictionaries.
   - **Why Dictionaries**: JSON objects are parsed into dictionaries, making it easy to work with API responses. You can easily access values using keys and even modify or update the data.

   **Example**:
   ```python
   api_response = {
       'status': 'ok',
       'data': {
           'user': 'john_doe',
           'followers': 150,
           'posts': 10
       }
   }

   # Accessing nested data
   print(api_response['data']['followers'])  # Output: 150
   ```

---

# 9.12 Dictionary Performance

Dictionaries in Python are highly efficient data structures, thanks to their use of hash tables. The underlying mechanism allows for fast lookups, insertions, and deletions. Below, we'll look at the time complexities of various dictionary operations and when dictionaries should be used for optimal performance.

## **Time Complexity of Dictionary Operations**

Python dictionaries are implemented as hash tables, meaning that for most operations, the time complexity is O(1), i.e., constant time. However, there are some important nuances to keep in mind.

### **1. Lookups (`dict[key]`)**
   - **Time Complexity**: O(1) on average.
   - **Explanation**: When you query a dictionary using a key, Python calculates the hash value of the key and retrieves the associated value directly from the underlying data structure in constant time.

   **Example**:
   ```python
   user_info = {'name': 'Alice', 'age': 30}
   print(user_info['name'])  # O(1) lookup, Output: 'Alice'
   ```

### **2. Insertions (`dict[key] = value`)**
   - **Time Complexity**: O(1) on average.
   - **Explanation**: Inserting a new key-value pair into a dictionary is a fast operation because Python can directly place the value at the location corresponding to the hash of the key.

   **Example**:
   ```python
   user_info = {'name': 'Alice', 'age': 30}
   user_info['city'] = 'New York'  # O(1) insertion
   ```

### **3. Deletions (`del dict[key]`)**
   - **Time Complexity**: O(1) on average.
   - **Explanation**: Deleting an item from a dictionary is a fast operation since it is essentially finding the key’s hash and removing the associated entry.

   **Example**:
   ```python
   user_info = {'name': 'Alice', 'age': 30, 'city': 'New York'}
   del user_info['city']  # O(1) deletion
   ```

### **4. Checking Membership (`key in dict`)**
   - **Time Complexity**: O(1) on average.
   - **Explanation**: Checking if a key exists in a dictionary is a constant-time operation, thanks to the hash table structure.

   **Example**:
   ```python
   user_info = {'name': 'Alice', 'age': 30}
   print('name' in user_info)  # Output: True
   print('city' in user_info)  # Output: False
   ```

### **5. Iterating Over Keys, Values, or Items**
   - **Time Complexity**: O(n) where n is the number of items in the dictionary.
   - **Explanation**: Iterating over the dictionary requires visiting each key-value pair, so the time complexity is linear in terms of the number of elements.

   **Example**:
   ```python
   user_info = {'name': 'Alice', 'age': 30}
   for key, value in user_info.items():
       print(f"{key}: {value}")  # O(n) iteration over dictionary
   ```

## **When to Use Dictionaries for Efficiency**

Dictionaries are especially useful when you need to:

1. **Store Key-Value Pairs**: Whenever you need to associate one item (key) with another (value) and require fast access to those pairs.
   
2. **Perform Fast Lookups**: If your application requires frequent access to data based on some unique key (e.g., user profiles, product catalogs, etc.), dictionaries are optimal because of their O(1) average lookup time.

3. **Avoid Duplicate Keys**: If you need to store unique keys and avoid duplication, dictionaries handle this for you. However, unlike lists or sets, you can store different values for the same key, which makes them flexible for a wide range of applications.

4. **Handling JSON-like Data**: In applications dealing with APIs or working with data in JSON format, dictionaries are ideal for parsing and accessing nested data structures.

5. **Efficient Memory Usage**: Python dictionaries are generally space-efficient for storing key-value pairs compared to alternatives like lists of tuples. They only store the keys and values you use, and hash-based indexing minimizes memory overhead.

### **When Not to Use Dictionaries**
While dictionaries are extremely efficient in many cases, they might not be the best choice when:

- **Order is Critical** (Before Python 3.7): If you need to guarantee insertion order (before Python 3.7), dictionaries would not be suitable. However, from Python 3.7 onwards, dictionaries maintain insertion order.
- **Memory Concerns**: If you are dealing with extremely large datasets and memory usage is critical, other data structures like `collections.defaultdict` or custom data structures might be more efficient.
- **Multiple Identical Keys**: If your application requires multiple values for the same key (duplicates), a dictionary is not ideal. In such cases, a `list` of tuples or a `defaultdict` from the `collections` module may be better suited.

---

<br><br>
<span style="display: flex; justify-content: space-between; width: 100%; align-items: center;">
    <a href="../08-module-08-tuples/README.md">
        <img src="https://img.shields.io/badge/Previous-Python_Tuples-blue" width="200" height="35">
    </a>
    <a href="../10-module-10-sets/README.md">
        <img src="https://img.shields.io/badge/Next-Python_Sets-brightgreen" width="170" height="35">
    </a>
</span>
<br><br>
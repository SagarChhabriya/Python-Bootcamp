# [9. Dictionaries](session-9.0.md#9-dictionaries)

<span style="display: flex; justify-content: space-between; width: 100%; align-items: center;">
    <a href="../08-module-08-tuples/README.md">
        <img src="https://img.shields.io/badge/Previous-Python_Tuples-blue" width="200" height="35">
    </a>
    <a href="../10-module-10-sets/README.md">
        <img src="https://img.shields.io/badge/Next-Python_Sets-brightgreen" width="170" height="35">
    </a>
</span>
<br><br>

# [9.1 Introduction to Dictionaries](session-9.0.md#91-introduction-to-dictionaries)
- **Characteristics and Use of Dictionaries in Python**
- **Comparison with Other Data Structures**: Lists, Tuples, and Sets (highlight when to choose dictionaries over these).

# [9.2 Properties of Dictionaries](session-9.0.md#92-properties-of-dictionaries)
- **Uniqueness of Keys**: Keys must be unique, but values can be duplicated.
- **Values Can Be of Any Data Type**
- **Order of Elements**: Dictionaries are ordered as of Python 3.7+, but this wasn’t always the case.
- **Key-Value Structure**: The basic structure of a dictionary and why it is useful for mapping and storing data.

# [9.3 Accessing Values in Dictionaries](session-9.0.md#93-accessing-values-in-dictionaries)
- **Accessing Elements using Keys**: Standard and Nested Dictionaries
- **Using `get()` for Safe Access** (vs direct indexing)
- **Default Values with `get()`**: Explain how the `get()` method can return a default value if a key doesn’t exist.
   
# [9.4 Methods in Dictionaries](session-9.0.md#94-methods-in-dictionaries)
- **Common Methods**: `keys()`, `values()`, `items()`, `get()`, `pop()`, `clear()`, `copy()`
- **Additional Methods**: `setdefault()`, `update()`, and `fromkeys()`
- **Merging Dictionaries**: Using `update()` and the `**` unpacking operator to merge dictionaries.

# [9.5 Dictionary Comprehension](session-9.0.md#95-dictionary-comprehension)
- **Syntax and Examples of Dictionary Comprehension**
- **Filtering Items**: Show how to use dictionary comprehension to filter key-value pairs.
- **Example with conditional logic**.

# [9.6 Mutation in Dictionaries](session-9.0.md#96-mutation-in-dictionaries)
- **How Dictionaries are Mutable**: Modifying Values in Place
- **Adding and Updating Key-Value Pairs**: Updating a value using the key and adding a new pair.
- **Nested Dictionaries**: Modifying values in nested dictionaries.

# [9.7 Packing and Unpacking Dictionaries](session-9.0.md#97-packing-and-unpacking-dictionaries)
- **Packing Key-Value Pairs into a Dictionary**
- **Unpacking with `**` Operator**: Using `**` for function arguments and merging dictionaries.

# [9.8 Limitations of Dictionaries](session-9.0.md#98-limitations-of-dictionaries)
- **Dictionaries are unordered** (in versions prior to Python 3.7)
- **Restrictions on Key Types**: Only Hashable Types Allowed
- **Not Suitable for Storing Multiple Identical Keys**: As keys must be unique, and duplicates are not allowed.

# [9.9 Deleting Elements in Dictionaries](session-9.0.md#99-deleting-elements-in-dictionaries)
- **Using `del`, `pop()`, and `clear()` for Deletion**
- **Deleting Specific Key-Value Pair**: How `pop()` works when you want to both retrieve and delete a key.
- **Deleting All Items**: Using `clear()` vs just `del`.

# [9.10 Membership in Dictionaries](session-9.0.md#910-membership-in-dictionaries)
- **Checking Membership with `in` and `not in` Operators**
- **Checking Membership of Keys vs Values**: Clarify the difference between checking for key existence and value existence.

# [9.11 Use Cases and Real-World Applications](session-9.0.md#911-use-cases-and-real-world-applications)
- **Storing Configurations, Caching, and Representing Data**
- **Using Dictionaries with APIs and Data Structures**: Examples of API responses or JSON-like structures.

# [9.12 Dictionary Performance](session-9.0.md#912-dictionary-performance)
- **Time Complexity of Dictionary Operations**: O(1) for lookups, insertions, and deletions.
- **When to Use Dictionaries for Efficiency**

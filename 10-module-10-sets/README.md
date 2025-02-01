# [10. Set and Frozenset](session-10.0.md#10-set-and-frozenset)

<span style="display: flex; justify-content: space-between; width: 100%; align-items: center;">
    <a href="../09-module-09-dictionaries/README.md">
        <img src="https://img.shields.io/badge/Previous-Python_Dictionaries-blue" width="250" height="35">
    </a>
    <!-- <a href="../11-module-11-nested-data-structures/README.md">
        <img src="https://img.shields.io/badge/Next-Nested_Data_Structures-brightgreen" width="270" height="35">
    </a> -->
</span>
<br><br>

## [10.1 Introduction to Set and Frozenset](session-10.0.md#101-introduction-to-set-and-frozenset)
- **Characteristics and Differences Between Set and Frozenset**
- **Use Cases and Applications**: Where to use sets and frozensets (e.g., for removing duplicates, as dictionary keys, etc.)

## [10.2 Creating Sets and Frozensets](session-10.0.md#102-creating-sets-and-frozensets)
- **Creating Sets**: Using set literals, `set()` constructor, from other iterables (list, tuple, string, etc.)
- **Creating Frozensets**: Using `frozenset()` constructor, from other iterables

## [10.3 Accessing Elements in Sets](session-10.0.md#103-accessing-elements-in-sets)
- **Unordered Nature of Sets**: No direct indexing or slicing
- **Iteration over Sets**: Using `for` loop to access elements

## [10.4 Joining Sets](session-10.0.md#104-joining-sets)
- **Union** (`|`) and `.union()`
- **Intersection** (`&`) and `.intersection()`
- **Difference** (`-`) and `.difference()`
- **Symmetric Difference** (`^`) and `.symmetric_difference()`

## [10.5 Replicating and Slicing Sets](session-10.0.md#105-replicating-and-slicing-sets)
- **Slicing**: Not supported due to unordered nature
- **Replicating Sets**: Using `copy()` method to duplicate sets

## [10.6 Mutation in Sets](session-10.0.md#106-mutation-in-sets)
- **Modifying Sets**: Adding and removing elements
  - `add()`, `update()`
  - `remove()`, `discard()`, `pop()`, `clear()`
- **Difference between `remove()` and `discard()`**

## [10.7 Packing and Unpacking Sets](session-10.0.md#107-packing-and-unpacking-sets)
- **Packing Sets**: Using `add()` and `update()`
- **Unpacking Sets**: Using `*` operator for function arguments and merging sets

## [10.8 Limitations of Sets and Frozensets](session-10.0.md#108-limitations-of-sets-and-frozensets)
- **Sets**: Unordered and mutable
- **Frozensets**: Immutable and hashable
- **Performance Considerations**: When to use frozensets vs sets, and how immutability affects performance

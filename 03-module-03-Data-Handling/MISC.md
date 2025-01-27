![](/Python-Bootcamp/03-module-03-Data-Handling/assets/01-variable-reference.png)
  

In Python, variables don't directly store data. Instead, they store **references** to data in memory. Here’s a simplified explanation with examples, along with how you can check memory locations using the `id()` function.

### 1. **Reassigning a Variable (First Example)**

When you assign a new value to a variable, it points to a new memory location, leaving the old value behind.

```python
a = 10   # a points to the value 10
print(id(a))  # Prints the memory location of 10
a = 20   # a now points to the value 20
print(id(a))  # Prints the memory location of 20
```

**Memory:**
```
a --> 10   (initially)
a --> 20   (after reassignment)
```

- `a` originally points to `10`, but after reassignment (`a = 20`), it now points to `20`, and the reference to `10` is lost.
- The `id()` function shows the memory address of the variable's value.

---

### 2. **Multiple Variables Pointing to the Same Value (Second Example)**

When two variables are assigned the same value, they both point to the same memory location.

```python
a = 10   # a points to the value 10
b = 10   # b also points to the value 10
print(id(a))  # Prints the memory location of 10
print(id(b))  # Prints the memory location of 10
```

**Memory:**
```
a --> 10
b --> 10
```

- Both `a` and `b` point to the same value `10` in memory. Instead of creating two separate copies of `10`, both variables reference the same memory location.
- The `id()` function shows that `a` and `b` have the same memory address because they point to the same value.

---

### Key Points:
- In Python, variables hold **references** to data, not the data itself.
- When you reassign a variable, it points to a new value, and the old value is discarded (unless other references still exist).
- If two variables share the same value, they may point to the same memory location to save space (for immutable data types like integers).
- The `id()` function can be used to confirm whether two variables point to the same memory location. If `id(a) == id(b)`, both variables are referencing the same memory.
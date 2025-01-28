### Static Binding vs Dynamic Binding in Python:

**1. Static Binding (Early Binding)**:

Static binding is not commonly used in Python, as Python is inherently dynamic. However, Python can exhibit behavior akin to static binding in certain situations, like method calls on objects that don't involve polymorphism.

Example of **Static Binding** (in Python):

```python
class Animal:
    def speak(self):
        print("Animal speaks")

a = Animal()
a.speak()  # Static binding: The method is resolved at compile time (Python still uses dynamic lookup, but no polymorphism involved).
```

- In this case, the method `speak()` is directly linked to the `Animal` class. There is no polymorphism or dynamic dispatch.

**2. Dynamic Binding (Late Binding)**:

Dynamic binding is typical in Python, especially with polymorphism (method overriding). The method that gets called is determined at runtime based on the actual object type.

Example of **Dynamic Binding**:

```python
class Animal:
    def speak(self):
        print("Animal speaks")

class Dog(Animal):
    def speak(self):
        print("Dog barks")

# Dynamic Binding happens here
a = Animal()
d = Dog()

a.speak()  # Output: Animal speaks
d.speak()  # Output: Dog barks
```

- Even though both `a` and `d` are assigned to variables of type `Animal`, Python uses dynamic binding to call the correct `speak()` method based on the actual object type (`Dog` or `Animal`).
- This is **Dynamic Binding**, as the method resolution happens at runtime.

---

### Summary of Python's behavior:


- **Static Binding**: Rare in Python, and typically happens in cases without polymorphism or method overriding.
- **Dynamic Binding**: Common in Python, especially when using inheritance and polymorphism.

Let me know if you want more clarification!
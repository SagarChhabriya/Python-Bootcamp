
# Variables and Assignments in Python 

In programming, **variables** are used to store data values. The way variables are declared and assigned values can vary between programming languages. Let's compare **Python** with other languages such as **C**, **Java**, and **JavaScript**.

## 1. **Variable Declaration and Assignment in Python**
In Python, you don’t need to explicitly declare the type of a variable before assigning a value to it. The type is automatically inferred from the value assigned. This is due to Python being a **dynamically typed** language.

### Example:
```python
x = 10            # x is an integer
y = "Hello"       # y is a string
z = 3.14          # z is a float
```

- Python uses a simple assignment operator `=`.
- **No need for explicit type declaration.**
- Variables are created when they are assigned a value.

### Variable Types in Python:
- Integers (`int`), Floating-point numbers (`float`), Strings (`str`), Booleans (`bool`), Lists (`list`), Dictionaries (`dict`), etc.
  
## 2. **Variable Declaration and Assignment in C**
In C, variables must be **explicitly declared** with a specific type before they can be assigned a value. C is a **statically typed** language, meaning the type of the variable is determined at compile-time and cannot change during runtime.

### Example:
```c
int x = 10;       // x is an integer
char y[] = "Hello";  // y is a string (character array)
float z = 3.14;   // z is a float
```

- In C, you must specify the type of variable (e.g., `int`, `char`, `float`).
- Variables must be declared **before** they are used.

## 3. **Variable Declaration and Assignment in Java**
Java, like C, is also a **statically typed** language. Variables in Java must be explicitly declared with a type, and the type cannot change once declared.

### Example:
```java
int x = 10;       // x is an integer
String y = "Hello";  // y is a string
double z = 3.14;  // z is a double
```

- Java requires explicit type declaration (`int`, `String`, `double`).
- **Variables cannot change types** after they are declared.

## 4. **Variable Declaration and Assignment in JavaScript**
JavaScript is more similar to Python in that it is a **dynamically typed** language. You don’t need to specify the type of a variable when declaring it, and the type can change during runtime.

### Example:
```javascript
let x = 10;       // x is a number
let y = "Hello";  // y is a string
let z = 3.14;     // z is a float
```

- JavaScript uses `let`, `const`, or `var` for declaring variables.
  - `let` is used to declare a variable with block scope.
  - `const` is used to declare a variable that cannot be reassigned.
  - `var` is used to declare variables with function scope, but is now largely outdated.

### Differences Between Python and Other Languages:

| Feature                          | **Python**                    | **C**                            | **Java**                        | **JavaScript**                  |
|-----------------------------------|-------------------------------|----------------------------------|---------------------------------|---------------------------------|
| **Variable Declaration**          | Implicit (no type required)   | Explicit (type required)         | Explicit (type required)        | Implicit (no type required)     |
| **Type of Language**              | Dynamically typed             | Statically typed                | Statically typed                | Dynamically typed               |
| **Variable Type Change**          | Allowed                       | Not allowed                     | Not allowed                     | Allowed                         |
| **Variable Scope**                | Global/Local                   | Local (in functions)            | Local (in methods)              | Local (block-scoped with `let`) |
| **Memory Management**             | Automatic (Garbage Collection) | Manual (developer-controlled)   | Automatic (Garbage Collection)  | Automatic (Garbage Collection)  |

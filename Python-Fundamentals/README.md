

# Table of Contents

1. [Language Fundamentals](#language-fundamentals)
   - [Introduction](#introduction)
   - [Example 1: To print "Hello World"](##example-1-to-print-hello-world)
   - [Example 2: To print the sum of 2 numbers](##example-2-to-print-the-sum-of-2-numbers)
   - [Functional Programming Features from C](##functional-programming-features-from-c)
   - [Object-Oriented Programming Features from C++](##object-oriented-programming-features-from-c++)
   - [Scripting Language Features from Perl and Shell Script](##scripting-language-features-from-perl-and-shell-script)
   - [Modular Programming Features from Modula-3](##modular-programming-features-from-modula-3)
   - [Syntax Origins](##syntax-origins)
   - [Where Can We Use Python?](##where-can-we-use-python)
   - [Note](##note)
   
2. [Features of Python](#features-of-python)

3. [Limitations of Python](#limitations-of-python)

4. [Flavors of Python](#flavors-of-python)

5. [Python Versions](#python-versions)

6. [Identifiers](#identifiers)
   - [Rules to Define Identifiers in Python](##rules-to-define-identifiers-in-python)
   - [Additional Identifier Rules](##additional-identifier-rules)
   - [Validity Check for Python Identifiers](##validity-check-for-python-identifiers)
   - [Notes](##notes)




# Language Fundamentals


## Introduction
- Python is a general-purpose high-level programming language.
- Python was developed by Guido van Rossum in 1989 while working at the National Research Institute in the Netherlands.
- Officially, Python was made available to the public in 1991. The official Date of Birth for Python is February 20, 1991.
- Python is recommended as the first programming language for beginners.

---

### Example 1: To print "Hello World"

**Java:**
```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```


**C:**
```C
#include <stdio.h>
void main() {
    printf("Hello World");
}

```

**python:**

```python
print("Hello World")
```

## Example 2: To print the sum of 2 numbers
**Java:**
```java
public class Add {
    public static void main(String[] args) {
        int a, b;
        a = 10;
        b = 20;
        System.out.println("The Sum: " + (a + b));
    }
}

```

**C:**
```C
#include <stdio.h>
void main() {
    int a, b;
    a = 10;
    b = 20;
    printf("The Sum: %d", (a + b));
}
```


**python:**
```python
a = 10
b = 20
print("The Sum:", (a + b))
```

The name "Python" was selected from the TV show *Monty Python's Flying Circus*, which was broadcast on the BBC from 1969 to 1974.

Guido developed the Python language by taking programming features from different languages:

- **Functional Programming Features** from C
- **Object-Oriented Programming Features** from C++
- **Scripting Language Features** from Perl and Shell Script


## Functional Programming Features from C

In C, while functional programming is not the primary paradigm, it allows functions to be used as first-class citizens. Python embraces this concept more naturally. Below is an example of a higher-order function in Python:

```python
# Using higher-order functions (like function pointers in C)

def square(x):
    return x * x

def apply_function(func, value):
    return func(value)

result = apply_function(square, 5)
print(result)  # Output: 25
```

## Object-Oriented Programming Features from C++
Python supports object-oriented programming similar to C++. It allows for class definitions, encapsulation, and inheritance. Here’s a basic example:

```python
# Class definition and inheritance

class Animal:
    def speak(self):
        return "I am an animal"

class Dog(Animal):
    def speak(self):
        return "Woof!"

dog = Dog()
print(dog.speak())  # Output: Woof!
```

## Scripting Language Features from Perl and Shell Script
Python is widely used as a scripting language, comparable to Perl and shell scripts. Below is an example demonstrating file handling and string manipulation:

```python
# Reading a file and processing its content

with open('example.txt', 'r') as file:
    lines = file.readlines()

for line in lines:
    print(line.strip())  # Remove whitespace and print each line
```

## Modular Programming Features from Modula-3
Python also supports modular programming, which allows for organizing code into reusable modules. This promotes better code organization and maintainability. Below is a simple example:

```python
# Example of a module

# mymodule.py
def greet(name):
    return f"Hello, {name}!"

# main.py
import mymodule

print(mymodule.greet("World"))  # Output: Hello, World!
```

## Syntax Origins

Most of the syntax in Python is derived from C and ABC languages.

## Where Can We Use Python?

Python can be used in a variety of application areas. Some of the most common and important applications include:

- Developing Desktop Applications
- Developing Web Applications
- Developing Database Applications
- Network Programming
- Developing Games
- Data Analysis Applications
- Machine Learning
- Developing Artificial Intelligence Applications
- Internet of Things (IoT)

## Note

- Internally, Google and YouTube use Python for various coding tasks.
- NASA and the New York Stock Exchange have developed applications using Python.
- Top software companies like Google, Microsoft, IBM, and Yahoo use Python extensively.

# Features of Python

1. **Simple and Easy to Learn:** Python has a simple syntax that resembles English, making it easy to read and write.
2. **Freeware and Open Source:** Python is free to use, and its source code can be customized.
3. **High Level Programming Language:** Python abstracts low-level details, making it programmer-friendly.
4. **Platform Independent:** Python programs can run on any platform without modification.
5. **Portability:** Python programs can easily migrate between platforms while providing consistent results.
6. **Dynamically Typed:** Variable types are assigned automatically, offering flexibility to programmers.
7. **Both Procedure-Oriented and Object-Oriented:** Supports both programming paradigms, allowing for security and reusability.
8. **Interpreted:** Python programs are compiled and executed by the interpreter without explicit compilation.
9. **Extensible:** Other language programs can be integrated into Python, enhancing performance and reusability.
10. **Embedded:** Python can be embedded within other language programs.
11. **Extensive Library:** Python comes with a rich set of inbuilt libraries for immediate use.

# Limitations of Python

1. **Performance:** Python's interpreted nature can lead to slower performance compared to compiled languages.
2. **Mobile Applications:** Python is not commonly used for mobile application development.




# Flavors of Python

1. **CPython:** The standard flavor of Python; compatible with C language applications.
2. **Jython (JPython):** Designed for Java applications; runs on the Java Virtual Machine (JVM).
3. **IronPython:** Tailored for the C#.NET platform.
4. **PyPy:** Enhances performance with a Just-In-Time (JIT) compiler included in the Python Virtual Machine (PVM).
5. **RubyPython:** Designed for integration with Ruby platforms.
6. **AnacondaPython:** Specifically built for handling large volumes of data processing.

# Python Versions

- **Python 1.0:** Introduced in January 1994.
- **Python 2.0:** Introduced in October 2000.
- **Python 3.0:** Introduced in December 2008.

> **Note:** Python 3 does not provide backward compatibility with Python 2, meaning there is no guarantee that Python 2 programs will run in Python 3.

## Current Versions

- Python  3.12.7
- Python 2.7.13



# Identifiers

An identifier is a name in a Python program.

It can be a class name, function name, module name, or variable name.

For example:
```python
a = 10
```

# Rules to Define Identifiers in Python

The only allowed characters in Python are:

- Alphabet symbols (either lowercase or uppercase)
- Digits (0 to 9)
- Underscore symbol (_)

By mistake, if we use any other symbol like `$`, we will get a syntax error.

- **Valid:** `cash = 10` ✅
- **Invalid:** `ca$h = 20` ❌

Identifiers should not start with a digit.

- **Invalid:** `123total` ❌
- **Valid:** `total123` ✅

Identifiers are case sensitive. Python language is case sensitive.

## Example:

```python
total = 10
TOTAL = 999
print(total)  # Output: 10
print(TOTAL)  # Output: 999
```

## Additional Identifier Rules

- Identifiers can contain alphabet symbols (either uppercase or lowercase).
- If an identifier starts with an underscore (_), then it indicates that it is private.
- Identifiers should not start with digits.
- Identifiers are case sensitive.
- We cannot use reserved words as identifiers.
  - **Example:** `def = 10` ❌
- There is no length limit for Python identifiers, but it is not recommended to use overly lengthy identifiers.
- The dollar symbol ($) is not allowed in Python.

## Validity Check for Python Identifiers

Which of the following are valid Python identifiers?

- `123total` ❌
- `total123` ✅
- `java2share` ✅
- `ca$h` ❌
- `_abc_abc_` ✅
- `def` ❌
- `if` ❌

## Notes

1. If an identifier starts with an underscore (_), it indicates that it is private.
2. If an identifier starts with two underscore symbols (__), it indicates that it is a strongly private identifier.
3. If the identifier starts and ends with two underscore symbols, then the identifier is a language-defined special name, which is also known as magic methods.
   - **Example:** `__add__`



# Reserved Words in Python

In Python, certain words are reserved to represent specific meanings or functionalities. These words are known as **reserved words**. 

## List of Reserved Words
There are 33 reserved words available in Python:

- `True`, `False`, `None`
- `and`, `or`, `not`, `is`
- `if`, `elif`, `else`
- `while`, `for`, `break`, `continue`, `return`, `in`, `yield`
- `try`, `except`, `finally`, `raise`, `assert`
- `import`, `from`, `as`, `class`, `def`, `pass`, `global`, `nonlocal`, `lambda`, `del`, `with`

## Notes:
1. All reserved words in Python contain only alphabet symbols.
2. Except for the following three reserved words, all others contain only lowercase alphabet symbols:
   - `True`
   - `False`
   - `None`

## Examples
- Invalid: `a = true` ❌
- Valid: `a = True` ✅

You can view the list of reserved words in Python using the following code:

```python
import keyword
print(keyword.kwlist)
```

```css
['False', 'None', 'True', 'and', 'as', 'assert', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
```



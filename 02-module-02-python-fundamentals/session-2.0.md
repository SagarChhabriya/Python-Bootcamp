# 2. Python Fundamentals

# 2.1 Basic Syntax


## Indentation

- **Python**: 
  - Python uses indentation to indicate code blocks instead of curly braces.
  - **Scenario**: You have a block of code inside an `if` condition.
    ```python
    if x > 10:
        print("x is greater than 10")
    ```
  - **Python is strict about indentation**; inconsistent indentation will cause a `IndentationError`.

- **Other Languages (Java, C, JavaScript)**:
  - Java, C, and JavaScript use curly braces `{}` to denote code blocks. Indentation is still a convention, but not strictly enforced.
    ```java
    if (x > 10) {
        System.out.println("x is greater than 10");
    }
    ```
  - Missing braces or improper formatting doesn’t cause an error (just less readable code).

## No Semicolon, No Parentheses (for control statements)

- **Python**:
  - Python does not require semicolons at the end of statements.
  - **Scenario**: Writing a simple print statement.
    ```python
    print("Hello, world!")
    ```

- **Other Languages**:
  - **Java/C/JavaScript**: Require semicolons after each statement.
    ```java
    System.out.println("Hello, world!");  // Semicolon is required
    ```
  - **Control structures** (like `if`, `for`, etc.) in Python do not require parentheses.
    ```python
    if x > 10:
        print("x is greater than 10")
    ```

  - In **Java/C/JavaScript**, parentheses are required:
    ```java
    if (x > 10) {
        System.out.println("x is greater than 10");
    }
    ```


## Python Character Set


## Python Tokens, Keywords, PEP8

---

# 2.2 Flow of the Python Program

- Depends on python flavor


- **Python**:
  - **Sequential Execution**: Statements are executed in the order they appear.
    ```python
    x = 5
    y = x + 3
    print(y)
    ```

  - **Control Flow**: Use of conditional statements, loops, functions, and exceptions to change execution.
    ```python
    if x > 10:
        print("x is greater than 10")
    else:
        print("x is 10 or less")
    ```

- **Other Languages**:
  - **Java/C/JavaScript**: Similar flow with the use of control flow statements (`if`, `while`, `for`), but often with a more verbose syntax for defining structures.
    ```java
    if (x > 10) {
        System.out.println("x is greater than 10");
    } else {
        System.out.println("x is 10 or less");
    }
    ```
  - **Java/C**: More explicit type declarations before using variables.

---

# 2.3 Working with Interactive Mode

## Evaluating expressions

- **Python**:
  - Python's interactive mode (REPL) evaluates expressions immediately and prints results.
    ```python
    >>> 5 + 3
    8
    >>> "Hello" + " World"
    'Hello World'
    ```

- **Optional in Python**:
  - You can use interactive mode for quick testing or debugging.
  - You can also assign variables and use expressions in the REPL.
    ```python
    >>> x = 5
    >>> y = x * 2
    >>> y
    10
    ```

- **Other Languages**:
  - **Java, C, JavaScript**: Do not have a native interactive mode like Python. You would need to write and compile the entire program.
    - **Java**: You need to write the whole class structure to execute the code.
    ```java
    public class Main {
        public static void main(String[] args) {
            System.out.println(5 + 3);  // Output 8
        }
    }
    ```
    - **C**: Similarly, you need to write a full program to test a simple expression.
    ```c
    #include <stdio.h>
    int main() {
        printf("%d", 5 + 3);  // Output 8
        return 0;
    }
    ```
    - **JavaScript**: You can use the browser’s console for quick evaluation.
    ```javascript
    console.log(5 + 3);  // Output 8
    ```

---


# 2.4 Working with Script Mode

## What is a Script?

- **Python**:
  - A script is a Python file containing statements that can be executed. Typically ends with `.py`.
    - **Scenario**: Writing a function in a script.
      ```python
      def greet(name):
          print(f"Hello, {name}!")
      greet("Alice")
      ```

- **Other Languages**:
  - **JavaScript**: A JavaScript script is often a `.js` file that can be executed in the browser or using Node.js.
    ```javascript
    function greet(name) {
        console.log(`Hello, ${name}!`);
    }
    greet("Alice");
    ```

  - **C/Java**: Requires an entry point like `main()` and generally needs to be compiled before execution.
    - **C**:
    ```c
    #include <stdio.h>
    int main() {
        printf("Hello, Alice!\n");
        return 0;
    }
    ```
    - **Java**:
    ```java
    public class Main {
        public static void main(String[] args) {
            System.out.println("Hello, Alice!");
        }
    }
    ```


## What is a Program?

- A program is a set of instructions for a computer, written in a programming language such as Python, Java, or C++. It tells the computer how to perform specific tasks and is composed of source code written by a programmer. 

- A program can be compiled, converting the code to machine code, or interpreted, where it is executed line-by-line. When executed, the computer follows these instructions to produce the desired output.


## Types of Script

Scripting languages are used to create scripts that automate tasks without requiring human interpretation. They are typically run through an interpreter rather than being compiled. Scripting languages can be divided into client-side (affecting what the user interacts with) and server-side (operating behind the scenes on the server).

**14 Top Scripting Languages**:
1. **JavaScript** - For interactive websites.
2. **PHP** - A general-purpose scripting language, mainly used in web development.
3. **Python** - Known for its simplicity, used in web development, AI, and more.
4. **Perl** - Used for text processing and web development.
5. **Ruby** - Ideal for web applications and data analysis.
6. **Bash** - A command-line scripting language for Unix systems.
7. **R** - Popular for statistics and data analysis.
8. **Lua** - Used in game development.
9. **Emacs Lisp** - For Unix systems and command line tasks.
10. **Groovy** - Similar to Java, used in web development.
11. **PowerShell** - Primarily for automating computer tasks.
12. **VBA** - Used to automate Microsoft applications like Excel.
13. **GML** - Scripting language for Game Maker Studio.
14. **VBScript** - A client-side and server-side language based on Visual Basic.

**Tips for Learning Scripting**:
- Align language learning with career goals.
- Use online courses and resources.
- Consider formal education in computer science.
- Practice coding regularly to improve skills.
- Search for solutions in online communities when stuck.



## Types of Programming Languages

1. **Procedural Languages**  
   - **Ada**, **C/C++**, **JavaScript**.

2. **Functional Languages**  
   - **Agda**, **PureScript**, **APL**.

3. **Object-oriented Languages**  
   - **Java**, **Python**, **Ruby**.

4. **Scripting Languages**  
   - **Perl**, **PHP**, **JavaScript**.

5. **Declarative Languages**  
    - **Prolog**, **Lisp**, **Haskell**.


---



# 2.5 Variables

## Identifiers

In Python, an **identifier** is a name given to various program elements such as classes, functions, modules, or variables.

### Rules for Defining Identifiers in Python:

1. **Allowed Characters**:
   - Identifiers can consist of alphabetic characters (both uppercase and lowercase).
   - Identifiers can include digits (0-9), but they cannot start with a digit.
   - The underscore symbol (`_`) is allowed.
   - Using other special characters like `$` will result in a syntax error.
     - **Valid**: `cash = 10`
     - **Invalid**: `ca$h = 10`

2. **Start of Identifier**:
   - An identifier cannot begin with a digit.
     - **Invalid**: `123total`
     - **Valid**: `total123`

3. **Case Sensitivity**:
   - Python is case-sensitive. This means `total`, `TOTAL`, and `Total` are considered distinct identifiers.
   
   ```python
   total = 10
   TOTAL = 999
   print(total)  # Output: 10
   print(TOTAL)  # Output: 999
   ```

4. **Reserved Words**:
   - Python has a set of reserved keywords that cannot be used as identifiers (e.g., `if`, `def`, `class`, etc.).
     - **Invalid**: `def = 10`
     - **Valid**: `my_def = 10`

5. **Length**:
   - There is no length limit for identifiers, but it is recommended not to use overly long names for clarity.

6. **Special Symbols**:
   - The dollar symbol (`$`) is not allowed in identifiers.

### Additional Notes on Identifiers:
- If an identifier starts with an underscore (`_`), it is often used to indicate that the identifier is intended to be "private."
- If an identifier starts with two underscores (`__`), it indicates a **strongly private** identifier.
- If an identifier begins and ends with two underscores (`__`), it is a **special** name or "magic method" defined by Python (e.g., `__add__`).

### Examples of Identifiers:
- **Valid Identifiers**:
  - `total123`
  - `java2python`
  - `_abc_abc`
  - `__init__`

- **Invalid Identifiers**:
  - `123total` (cannot start with a digit)
  - `ca$h` (invalid character `$`)
  - `def` (reserved keyword)
  - `if` (reserved keyword)

---

### Exercise:
Evaluate whether the following names are valid Python identifiers:
- `123total` 
- `total123` 
- `java2python` 
- `ca$h` 
- `_abc_abc` 
- `def` 
- `if` 

---

**Note**:
- An identifier starting with a single underscore (`_`) typically signals that it is private (although not strictly enforced in Python).
- Identifiers that start and end with two underscores (`__`) are **magic methods** (e.g., `__add__`).






# Variables and Assignments in Python vs Other Languages

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


# 2.6 Input and Output in Python
  - The `input()` function
  - Single input, Multiple input
  - Vulnerability in `input()` (Python 2.x)
  - The `print()` function
    - New line
    - Parameters: `end`, `sep`
  - `raw_input()` (Note: Python 2.x)
  - Output formatting

# 2.7 Working with Python Functions
  - `type()` function
  - `id()` function

---




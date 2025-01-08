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

3. **Machine Languages**  
   - **Fortran**.

4. **Assembly Languages**  
   - **Lotus 1-2-3**, **Turbo Pascal**.

5. **Logic Programming Languages**  
   - **Prolog**, **ASP**, **Datalog**.

6. **Data-oriented Languages**  
   - **Clarion**, **Gremlin**, **Wolfram Language**.

7. **Business-oriented Languages**  
   - **SQL**, **COBOL**.

8. **Object-oriented Languages**  
   - **Java**, **Python**, **Ruby**.

9. **Scripting Languages**  
   - **Perl**, **PHP**, **JavaScript**.

10. **Declarative Languages**  
    - **Prolog**, **Lisp**, **Haskell**.

11. **Document Formatting Languages**  
    - **TeX**, **PostScript**.

12. **World Wide Web Display Languages**  
    - **HTML**, **XML**, **CGI**.

13. **Front-end Coding Languages**  
    - **HTML**, **CSS**, **JavaScript**.

14. **Database Programming Languages**  
    - **C++**, **COBOL**, **Java**, **Perl**.

15. **Compiled Languages**  
    - **C++**, **ALGOL**, **ActionScript**.

16. **Back-end Coding Languages**  
    - **Python**, **Ruby**, **Java**.

17. **System Languages**  
    - **Swift**, **Rust**, **C++**, **Nim**.

18. **Algorithmic Languages**  
    - **Fortran**, **ALGOL**, **Lisp**, **C**.

19. **Command-line Interface Languages**  
    - **Batch**, **CLIST**, **TACL**, **4DOS**.

20. **Visual Languages**  
    - **Grasshopper**, **GameMaker Language**, **XOD**, **ToonTalk**.

21. **Interpreted Languages**  
    - **Apache Ant**, **JavaScript**, **PostScript**, **Windows PowerShell**.

22. **Esoteric Languages**  
    - **Beatnik**, **INTERCAL**, **Piet**, **Whitespace**.

23. **Multiparadigm Languages**  
    - **ALF**, **C++**, **ECMAScript**, **Python**.

24. **Imperative Languages**  
    - **MATLAB**, **ECMAScript**, **Perl**, **Python**.

25. **Dataflow Languages**  
    - **Analytica**, **Lucid**, **Oz**, **Ballerina**.

26. **Concurrent Languages**  
    - **Ada**, **ChucK**, **Java**, **Oz**.

27. **Reflective Languages**  
    - **Cobra**, **ECMAScript**, **Prolog**, **Ruby**.

28. **Fourth-generation Languages**  
    - **ABAP**, **FOCUS**, **OpenEdge ABL**, **DataFlex**.  


---


# 2.5 Variables and Data Types

## Identifiers
A name in Python is program is called identifier. It can be class name or function name or module name or variable name.

- Rules to define identifiers in Python:
  1. The only allowed characters in python are 
    - alphabet symbols(either lower case or upper case)
    - digits (0-9)
    - underscore symbol(_)
    By mistake if we are using any other symbol like $ then we will get syntax error.
    - cash = 10 ✅
    - ca$h = 10 ❌

  2. Identifier should not starts with digit
    - 123total ❌ 
    - total123 ✅

  3. Identifiers are case sensitive (python is case senstive). 
    
    ```python 
    total = 10
    TOTAL = 999
    print(total) # 10
    print(TOTAL) # 999
    ```

## Identifier
  - Alphabet Symbols (Either Upper case OR Lower case)
  - If identifier start with underscore(_) then it indicates its private.
  - Identifier should not start with digits.
  - Identifiers are case sensitive.
  - we cannot use reserve words as identifiers
    Ex: def = 10 ❌
  - There is no length limit for Python identifiers. But not recommended to use too length identifiers.
  - Dollar ($) Symbol is not allowed in Python. 


### Exercise
  - 123total
  - total123
  - java2python
  - ca$h
  - _abc_abc
  - def
  - if

**Note:** 
1. If identifier starts with _ symbol then it indicates that it is private.
2. If identifier starts with __ (two underscore symbols) indicating that strongly private identifier.
3. If the identifier starts and ends with two underscore symbols then the identifier is language defined special name, which is also known as magic methods.

Example:
  `__add__`



, Literals, Operators


  - Variables and Assignments in Python vs Other Languages

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




### **2.5 Variables and Data Types**

#### **Identifiers, Literals, Operators**

- **Python**:
  - Variables in Python are dynamically typed. You can assign any type of value to a variable without declaring its type.
    ```python
    x = 10  # Integer
    x = "Hello"  # String
    ```

- **Optional in Python**:
  - Python allows flexible identifiers (e.g., using `_` for private variables).
    ```python
    _private_var = 5
    ```

- **Other Languages**:
  - **Java, C**: Variables need to be explicitly declared with a type.
    - **Java**:
      ```java
      int x = 10;
      String name = "Alice";
      ```

    - **C**:
      ```c
      int x = 10;
      char name[] = "Alice";
      ```

  - **JavaScript**: Uses `var`, `let`, or `const` for variable declaration and is loosely typed (similar to Python).
    ```javascript
    let x = 10;  // Number
    x = "Hello"; // String
    ```

#### **Variables and Assignments in Python vs Other Languages**

- **Python**:
  - Python uses **dynamic typing**, meaning you don’t need to explicitly declare variable types.
    ```python
    a = 10  # integer
    b = "Hello"  # string
    ```

- **Other Languages**:
  - **Java/C**: Require explicit variable declarations.
    - **Java**:
      ```java
      int a = 10;
      String b = "Hello";
      ```
    - **C**:
      ```c
      int a = 10;
      char b[] = "Hello";
      ```

  - **JavaScript**: Variables are dynamically typed, but use `var`, `let`, or `const` for declaration.
    ```javascript
    let a = 10;  // number
    let b = "Hello";  // string
    ```

---

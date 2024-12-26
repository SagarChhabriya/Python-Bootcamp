# 1. Getting Started

## 1.1 Introduction

### 1.1.1 Introduction to Python

- **History & Origins**  
    Python is a widely used high-level programming language for general-purpose programming, created by Guido van Rossum in 1989 while working at the National Research Institute in the Netherlands.Officially, Python was made available to the public in 1991. The official Date of Birth for Python is February 20, 1991.

    Python features a dynamic type system and automatic memory management and supports multiple programming paradigms, including object-oriented, imperative, functional programming, and procedural styles. It has a large and comprehensive standard library.

    The name Python was selected from the TV show `The Complete Monty Python's Circus` which was braodcasted in BBC from 1969 to 1974. Guido developed Python language by taking almost all programming features from different languages.
  
  1. Functional Programming Features from C
  2. Object Oriented Programming Features from C++
  3. Scripting Language Features from Perl and Shell Script
  4. Modular Programming Features from Modula-3




  Two major versions of Python are currently in active use:
  - Python 3.x is the current version and is under active development.
  - Python 2.x is the legacy version and will receive only security updates until 2020. No new features will be implemented. Note that many projects still use Python 2, although migrating to Python 3 is getting easier.



- **Why Python?**

  Python has become one of the most popular and widely used programming languages due to several key advantages:

  1. **Easy to Learn and Use**: Python has a simple and readable syntax, which makes it an excellent choice for beginners. It allows new developers to focus on learning programming concepts rather than dealing with complex syntax.

  2. **Versatile and Flexible**: Python can be used for a wide range of applications, from web development and data analysis to machine learning and automation. Its flexibility allows developers to use it for almost any type of programming task.

  3. **Large Community and Libraries**: Python has a massive community of developers who contribute to a vast collection of open-source libraries and frameworks. This means you can find pre-written code to speed up development for nearly any project.

  4. **Cross-Platform Compatibility**: Python is platform-independent, which means you can write a program on one operating system (Windows, macOS, Linux) and run it on another without modification.

  5. **Strong Support for Integration**: Python can easily integrate with other languages like C, C++, Java, and .NET, and it can also be used to interface with databases, web services, and other applications.

  6. **Excellent for Data Science and AI**: With libraries like NumPy, Pandas, and TensorFlow, Python has become a go-to language for data scientists and machine learning practitioners.

  7. **Open-Source and Free**: Python is open-source, meaning it is free to use and distribute. The open-source nature encourages collaboration and continuous improvements to the language.

  In short, Python is a powerful yet easy-to-use language that is suitable for both beginners and professionals, making it a preferred choice for developers worldwide.


### 1.1.2 Python's Popular Applications
  - **What is Python Used For?**
  
    Python is a versatile language and can be used for a wide variety of applications, including:
  
    1. **Web Development**: Using frameworks like Django and Flask, Python is widely used to build dynamic and interactive websites.
    2. **Data Science & Machine Learning**: Libraries such as Pandas, NumPy, SciPy, and TensorFlow make Python an excellent choice for data analysis, machine learning, and AI.
    3. **Automation & Scripting**: Python is popular for automating repetitive tasks, writing scripts, and performing system administration tasks.
    4. **Game Development**: Python is also used in game development, particularly with libraries like Pygame.
    5. **Scientific Computing**: Python is widely used in scientific and numeric computing, with tools like SymPy for symbolic mathematics and Matplotlib for plotting.
    6. **Desktop GUI Applications**: Python can be used to develop desktop applications with GUI, using frameworks such as Tkinter and PyQt.
    7. **Cybersecurity and Networking**: Python plays a vital role in penetration testing, building security tools, and handling network-related tasks.

### 1.1.3 Python's Strengths and Weaknesses

  - **Advantages of Python**
  
    Python has a number of key strengths that make it highly popular:
  
    1. **Easy Syntax**: Python has a readable and simple syntax, which is beginner-friendly.
    2. **Extensive Libraries**: Python has an extensive standard library and a rich ecosystem of third-party libraries.
    3. **Cross-Platform**: Python is cross-platform, meaning you can run the same code on various operating systems with minimal modification.
    4. **Large Community**: Python's large and active community provides plenty of support, documentation, and resources.
    5. **Interpreted Language**: Python is an interpreted language, which means you can test code snippets interactively and develop quickly.
    6. **Open Source**: Python is open-source, so it’s free to use and distribute.

  - **Disadvantages of Python**
  
    Despite its advantages, Python has some weaknesses:
  
    1. **Slower Execution**: As an interpreted language, Python can be slower compared to compiled languages like C or Java.
    2. **Not Ideal for Mobile Development**: While Python can be used for mobile apps, it's not as commonly used for mobile development as languages like Swift or Kotlin.
    3. **Memory Consumption**: Python’s memory consumption is high due to its dynamic typing and garbage collection.
    4. **Weak in Multithreading**: Python’s Global Interpreter Lock (GIL) can limit the performance of multithreaded programs, especially in CPU-bound tasks.

### 1.1.4 Python Basics: Understanding Core Concepts

  - **Namespace and Scope**
  
    Sure! Let's simplify the explanation by relating the concepts of **heap**, **stack**, and **namespace** in simple terms.

### Stack and Heap:
- **Stack**: Think of the stack as a pile of plates in a cafeteria. Each time you call a function in Python, it adds a plate to the pile with the variables that function needs. When the function is done, the plate is taken off the pile. 
  - **What goes on the stack?** Small, temporary things like numbers or simple variables that exist only while the function is running.
  - **When is it removed?** As soon as the function finishes, the stack removes those variables.

- **Heap**: The heap is more like a storage room for big things, like furniture. When you create complex objects (like lists or dictionaries), they are placed in the heap. These things stay in the storage room until you're done with them, and Python decides to clean them up.
  - **What goes in the heap?** Large objects that need to stay in memory, like lists, dictionaries, or objects you create in your program.
  - **When is it removed?** It stays in memory until Python is finished with it and does automatic cleanup.

### Namespaces:
A **namespace** is like a **label** or **name tag** that helps you find things. It’s like when you give a name to a plate (in the stack) or a piece of furniture (in the heap) so you can remember what it is.

- **In Python**, namespaces keep track of where each variable is, whether it’s inside a function, inside a class, or globally available. 
- When you use a variable, Python looks in the appropriate **namespace** to find where it’s stored.

### Connecting the Stack, Heap, and Namespace:
- When you create a **variable** in Python, the **namespace** gives it a name (like "x" or "my_list").
- If the variable is a simple number or string, it’s stored on the **stack**.
- If the variable is a more complex object (like a list or dictionary), it’s stored in the **heap**.
- The **namespace** keeps track of which name refers to which object, and it helps Python know where to look for the object when you use that name.

### Simple Example:

```python
x = 5  # 'x' is a name, and its value (5) is stored in the stack
def example():
    y = [1, 2, 3]  # 'y' is a name, and the list [1, 2, 3] is stored in the heap
    print(x)  # Looks in the global namespace for 'x'
    print(y)  # Looks in the local namespace for 'y'
```

- The **namespace** maps the names (`x` and `y`) to their **values** (like `5` or the list `[1, 2, 3]`).
- `x` is a simple value, so it’s stored in the **stack**.
- `y` refers to a list, which is a complex object, so the list is stored in the **heap**, but the name `y` itself is in the **stack**.

### In Short:
- The **stack** is for quick, temporary storage, like small numbers or simple values.
- The **heap** is for bigger things, like lists or objects that need to stay in memory longer.
- A **namespace** helps Python know what each name refers to and where it can find the data in the stack or heap.


- **Scope** refers to the region in the code where a particular namespace is accessible. The most common scopes in Python are:
      1. **Global scope**: The outermost scope accessible throughout the program.
      2. **Local scope**: Refers to variables inside a function.
      3. **Enclosing scope**: The scope of any enclosing functions in nested functions.
      4. **Built-in scope**: Contains built-in functions and objects like `print()` and `len()`.

  - **Program Structure**
  
    Python programs are typically structured using functions, classes, modules, and packages:
    
    1. **Functions**: Code blocks that can be called with arguments and return values.
    2. **Classes**: Python supports object-oriented programming (OOP), and classes are the blueprint for creating objects.
    3. **Modules**: A module is a file containing Python code that defines functions, classes, or variables. It allows for code reuse.
    4. **Packages**: A package is a collection of Python modules, typically organized into a directory hierarchy, that provides additional functionality.





## 1.1.5 Getting Started with Python Development

### Installing Python
You can download and install either version of Python [here](https://www.python.org/downloads/). See Python 3 vs. Python 2 for a comparison between them. In addition, some third-parties offer re-packaged versions of Python that add commonly used libraries and other features to ease setup for common use cases, such as math, data analysis, or scientific use. See [the list at the official site](https://www.python.org/download/alternatives/).

To confirm that Python was installed correctly, you can verify it by running the following command in your favorite terminal. (If you are using Windows OS, you need to add the path of Python to the environment variable before using it in the command prompt):

```bash
python --version
```

If you have installed Python 3, but `$ python --version` outputs a Python 2 version, it means you also have Python 2 installed. This is often the case on MacOS and many Linux distributions. In that case, use the Python 3 interpreter.

### Interactive Shell vs Script Files

- **Interactive Shell:**
An interactive shell refers to a command-line interface (CLI) or a terminal where commands are executed one at a time, interactively. Users type commands and get immediate feedback. It's ideal for testing small pieces of code, debugging, or interacting directly with a system. Examples of interactive shells include the Python interactive shell, Bash, or PowerShell.

- **Script Files:**
A script file is a text file that contains a series of commands or code written in a programming or scripting language. These commands are executed in sequence when the script is run, typically by invoking the file with an interpreter (e.g., running a Python script with `python script.py`). Scripts are commonly used for automation, batch processing, and executing predefined tasks.

---

### Key Differences:
- **Interactive Shell** is for immediate, single-line command execution with instant results.
- **Script Files** are for writing reusable, multi-line commands that can be executed as a whole.

---

### Examples

#### 1. **Python (Interactive Shell)**

In an interactive Python shell, you type one command at a time:

```python
>>> x = 10
>>> y = 5
>>> print(x + y)
15
```

This is done interactively where results are displayed immediately after each line of code.

#### 2. **Python (Script File)**

In a Python script (e.g., `script.py`), the code is written in a file and executed as a whole:

```python
# script.py
x = 10
y = 5
print(x + y)
```

To run this script, you use a command like `python script.py`, and the output will be `15`.

#### 3. **Bash (Interactive Shell)**

In an interactive Bash shell, you type commands one by one:

```bash
$ echo "Hello, World!"
Hello, World!
```

#### 4. **Bash (Script File)**

A Bash script file (e.g., `script.sh`) contains a sequence of commands:

```bash
#!/bin/bash
echo "Hello, World!"
echo "This is a Bash script"
```

To run the script, use `bash script.sh`.

#### 5. **JavaScript (Interactive Shell)**

In a browser's developer tools or a Node.js interactive shell, you can execute JavaScript commands:

```javascript
> let x = 5;
> let y = 10;
> x + y
15
```

#### 6. **JavaScript (Script File)**

A JavaScript file (e.g., `script.js`) would contain multiple commands:

```javascript
// script.js
let x = 5;
let y = 10;
console.log(x + y);
```

Run the script using Node.js with the command `node script.js`.

#### 7. **PowerShell (Interactive Shell)**

In PowerShell, you can interactively execute commands like:

```powershell
PS C:\> $x = 10
PS C:\> $y = 5
PS C:\> $x + $y
15
```

#### 8. **PowerShell (Script File)**

A PowerShell script (e.g., `script.ps1`) will contain commands to be executed together:

```powershell
# script.ps1
$x = 10
$y = 5
Write-Output ($x + $y)
```

You would run this script using `.\script.ps1`.

---

### In Short

- **Interactive Shell**: Used for quick, one-off commands with immediate feedback. Ideal for testing and debugging.
- **Script Files**: Used for writing a sequence of commands to automate tasks or perform repeated operations. Scripts are executed as a whole.

### Choosing an IDE or Text Editor
- **Local**: VS Code, PyCharm, Anaconda, other.
- **Cloud**: Google Colab, Replit, other.

### 1.1.6 Python Internals
- Understanding the Python Virtual Machine (PVM)

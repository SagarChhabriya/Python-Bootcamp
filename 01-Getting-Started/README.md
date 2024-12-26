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

### 1.1.2 Python's Popular Applications
  - What is Python Used For?

- **1.1.3 Python's Strengths and Weaknesses**
  - Advantages of Python
  - Disadvantages of Python

- **1.1.4 Python Basics: Understanding Core Concepts**
  - Namespace and Scope
  - Program Structure

Here is the syntax for your `.md` (Markdown) file, incorporating all the content and structure you've provided:


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

### To Summarize

- **Interactive Shell**: Used for quick, one-off commands with immediate feedback. Ideal for testing and debugging.
- **Script Files**: Used for writing a sequence of commands to automate tasks or perform repeated operations. Scripts are executed as a whole.

### Choosing an IDE or Text Editor
- **Local**: VS Code, PyCharm, Anaconda, other.
- **Cloud**: Google Colab, Replit, other.

### 1.1.6 Python Internals
- Understanding the Python Virtual Machine (PVM)
```

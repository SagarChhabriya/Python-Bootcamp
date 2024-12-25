# 1. Getting Started

- **1.1 Introduction to Python**
  - History & Origins
  - Why Python?

- **1.2 Python's Popular Applications**
  - What is Python Used For?

- **1.3 Python's Strengths and Weaknesses**
  - Advantages of Python
  - Disadvantages of Python

- **1.4 Python Basics: Understanding Core Concepts**
  - Namespace and Scope
  - Program Structure

- **1.5 Getting Started with Python Development**
  - Installing Python
  - Interactive Shell vs Script Files
  - Choosing an IDE or Text Editor

- **1.6 Python Internals**
  - Understanding the Python Virtual Machine (PVM)

---

# 2. Python Fundamentals

- **2.1 Basic Syntax**
  - Indentation (No semicolon, no parentheses)
  - Python Character Set
  - Python Tokens, Keywords, PEP8

- **2.2 Flow of the Python Program**
  - Understanding program execution flow

- **2.3 Working with Interactive Mode**
  - Evaluating expressions

- **2.4 Working with Script Mode**
  - Running and creating Python scripts

- **2.5 Variables and Data Types**
  - Identifiers, Literals, Operators
  - Variables and Assignments in Python vs Other Languages

- **2.6 Input and Output in Python**
  - The `input()` function
  - Single input, Multiple input
  - Vulnerability in `input()` (Python 2.x)
  - The `print()` function
    - New line
    - Parameters: `end`, `sep`
  - `raw_input()` (Note: Python 2.x)
  - Output formatting

- **2.7 Working with Python Functions**
  - `type()` function
  - `id()` function


---
# 3. Introduction to Data Handling

- **3.1 Data Types in Python**
  - Static vs Dynamic Typing
  - Numbers
  - Boolean
  - Strings

- **3.2 Type Conversion**
  - Implicit and Explicit Conversion

- **3.3 Constants in Python**
  - Understanding Constants (Best practices)

- **3.4 Special Data Types**
  - `None`

- **3.5 Sequences in Python**
  - Lists
  - Tuples

- **3.6 Sets and Dictionaries**
  - Sets
  - Frozensets
  - Dictionaries

- **3.7 Maps and Data Structures**
  - Introduction to Mapping Types

---

# 4. Operators

- **4.1 Arithmetic Operators**
  - Addition, Subtraction, Multiplication, Division, etc.

- **4.2 Relational Operators**
  - Comparison Operators: `==`, `!=`, `>`, `<`, `>=`, `<=`

- **4.3 Logical Operators**
  - `and`, `or`, `not`

- **4.4 Membership Operators**
  - `in`, `not in`

- **4.5 Identity Operators**
  - `is`, `is not`

- **4.6 Bitwise Operators**
  - `&`, `|`, `^`, `<<`, `>>`, `~`

- **4.7 Assignment Operators**
  - `=`, `+=`, `-=`, `*=`, `/=`, etc.

- **4.8 Operators Precedence**
  - Order of operations in Python

- **4.9 Evaluating Expressions**
  - How expressions are evaluated in Python

- **4.10 Type Casting**
  - Implicit and Explicit Type Conversion

- **4.11 Miscellaneous Operators**
  - Division operator (`/` vs `//`)
  - **Operator Overloading**  
    - How operators are overloaded in Python

- **4.12 Inplace vs Standard Operators**
  - Difference between In-place Operators (`+=`, `*=`) and standard operators

- **4.13 Comparing `==` vs `is`**
  - Understanding equality vs identity

- **4.14 Membership and Identity Operators**
  - Differences between `in`, `not in`, `is`, `is not`

---


# 5. Debugging

- **5.1 Types of Errors**
  - Syntax Errors
  - Runtime Errors
  - Semantic Errors

- **5.2 Locating and Resolving Errors**
  - How to identify and troubleshoot errors in Python code

- **5.3 Introduction to Exception Handling**
  - More on errors using the Exception Handling module
  - `try`, `except`, `else`, `finally`

- **5.4 Common Debugging Techniques**
  - Using print statements
  - Using a debugger (e.g., `pdb`)
  - IDE Debugging Tools

- **5.5 Best Practices for Debugging**
  - Writing clean code to minimize errors
  - Using logging for better error tracking


---

# 6. String Manipulation

- **6.1 Introduction to Python Strings**
  - Immutable Nature of Strings (Mutation in strings)

- **6.2 Accessing String Elements**
  - Accessing Individual Characters
  - Using Positive and Negative Indexing

- **6.3 String Operators**
  - Concatenation (`+`), Repetition (`*`)

- **6.4 String Slicing**
  - How to slice strings
  - Syntax: `string[start:end:step]`

- **6.5 Common String Functions and Methods**
  - `upper()`, `isupper()`, `lower()`, `islower()`
  - `count()`, `strip()`, `replace()`, `join()`, `split()`
  - `substring()`, `index()`
  
- **6.6 Working with String Formatting**
  - String formatting using f-strings, `format()`, and `%` formatting


---


# 7. List Manipulation

- **7.1 Introduction to Python Lists**
  - Characteristics and Use of Lists in Python

- **7.2 Creating Lists**
  - Different Ways to Create Lists (e.g., using literals, constructors)

- **7.3 Accessing List Elements**
  - Indexing (Positive and Negative Indexing)
  - Accessing Individual Elements

- **7.4 Modifying Lists**
  - Joining Lists
  - Replicating Lists
  - List Slicing

- **7.5 Common List Methods**
  - `append()`, `pop()`, `sort()`, `count()`, `index()`, `insert()`, `remove()`
  - Prepending Elements (using `insert()` or list concatenation)

- **7.6 List Comprehension**
  - Syntax and Examples of List Comprehension

- **7.7 List Mutation**
  - How Lists are Mutable (Changing Elements in Place)

- **7.8 Packing and Unpacking Lists**
  - Packing multiple elements into a list and unpacking them into variables

- **7.9 Limitations of Lists**
  - Immutable elements, fixed size, and performance considerations

- **7.10 Iteration over Lists**
  - Using `for` loops and comprehensions to iterate through lists

- **7.11 Membership Operators**
  - Using `in` and `not in` to check membership

- **7.12 List Concatenation**
  - Joining multiple lists with `+` or `extend()`

- **7.13 Multi-dimensional Lists**
  - Creating and accessing multi-dimensional (nested) lists

- **7.14 Deleting Elements**
  - Using `del`, `pop()`, and `remove()` to delete list elements

- **7.15 Reassigning List Elements**
  - Reassigning and modifying values in a list at specific indexes

---


# 8. Tuples

- **8.1 Introduction to Tuples**
  - Characteristics and Use of Tuples in Python

- **8.2 Creating Tuples**
  - Different Ways to Create Tuples (e.g., using literals, constructors)

- **8.3 Single-item and Multiple-item Tuples**
  - Creating Tuples with a Single Element
  - Creating Tuples with Multiple Elements

- **8.4 Packing and Unpacking Tuples**
  - Packing Multiple Values into a Tuple
  - Unpacking Tuple Elements into Variables

- **8.5 Accessing Tuple Elements**
  - Indexing (Positive and Negative Indexing)
  - Accessing Individual Elements

- **8.6 Modifying Tuples**
  - Joining Tuples
  - Replicating Tuples
  - Tuple Slicing

- **8.7 Limitations of Tuples**
  - Immutable Nature (Cannot be Changed After Creation)

- **8.8 Tuple Functions and Methods**
  - Common Tuple Methods: `count()`, `index()`

- **8.9 Deleting Elements**
  - Deleting Tuples with `del`

- **8.10 Reassigning Tuples**
  - Reassigning Whole Tuples (Tuples are Immutable)

---

# 9. Dictionaries

- **9.1 Introduction to Dictionaries**
  - Characteristics and Use of Dictionaries in Python

- **9.2 Properties of Dictionaries**
  - Uniqueness of Keys, Values, and Their Structure

- **9.3 Accessing Values in Dictionaries**
  - Accessing Elements using Keys
  - Using `get()` for Safe Access

- **9.4 Methods in Dictionaries**
  - Common Methods: `keys()`, `values()`, `items()`, `get()`, `pop()`, `clear()`, `copy()`
  - Merging Dictionaries

- **9.5 Dictionary Comprehension**
  - Syntax and Examples of Dictionary Comprehension

- **9.6 Mutation in Dictionaries**
  - How Dictionaries are Mutable (Modifying Values in Place)

- **9.7 Packing and Unpacking Dictionaries**
  - Packing Key-Value Pairs into a Dictionary
  - Unpacking with `**` Operator

- **9.8 Limitations of Dictionaries**
  - Dictionaries are unordered (in versions prior to Python 3.7)
  - Restrictions on Key Types (Hashable Types Only)

- **9.9 Deleting Elements in Dictionaries**
  - Using `del`, `pop()`, and `clear()` for Deletion

- **9.10 Membership in Dictionaries**
  - Checking Membership with `in` and `not in` Operators

---

# 10. Set and Frozenset

- **10.1 Introduction to Set and Frozenset**
  - Characteristics and Differences Between Set and Frozenset

- **10.2 Creating Sets and Frozensets**
  - Different Ways to Create Sets and Frozensets

- **10.3 Accessing Elements in Sets**
  - How to Access Elements in Sets (Note: Sets are unordered)

- **10.4 Joining Sets**
  - Set Operations: Union (`|`), Intersection (`&`), Difference (`-`)

- **10.5 Replicating and Slicing Sets**
  - Slicing (Note: Not supported for sets directly due to unordered nature)
  - Replicating Sets

- **10.6 Mutation in Sets**
  - Modifying Sets: Adding and Removing Elements (`add()`, `remove()`, `discard()`, `pop()`)

- **10.7 Packing and Unpacking Sets**
  - Packing Sets (Adding Multiple Items)
  - Unpacking Sets Using `*`
  
- **10.8 Limitations of Sets and Frozensets**
  - Sets: Unordered and Mutable
  - Frozensets: Immutable, Hashable Nature


---
# 11. Nested Data Structures

- **11.1 Introduction to Nested Data Structures**
  - Understanding Nested Structures and Their Use Cases

- **11.2 Arrays**
  - Definition and Characteristics of Arrays
  - Arrays as a Data Structure in Python

- **11.3 Array of Arrays**
  - Creating and Working with Nested Arrays (Lists of Lists)

- **11.4 Arrays of Dictionaries**
  - Using Arrays (Lists) to Store Dictionaries
  - Accessing Dictionary Elements within Arrays

- **11.5 Arrays of Tuples**
  - Storing Tuples in Arrays (Lists)
  - Accessing Tuple Elements within Arrays

- **11.6 Dictionaries**
  - Definition and Characteristics of Dictionaries
  - Using Dictionaries as Nested Structures

- **11.7 Arrays as Values in Dictionaries**
  - Using Lists as Values in Dictionaries
  - Accessing Lists from Dictionary Keys

- **11.8 Tuples as Values in Dictionaries**
  - Using Tuples as Values in Dictionaries
  - Accessing Tuples from Dictionary Keys

- **11.9 Dictionaries as Values in Arrays**
  - Storing Dictionaries as Elements in Arrays
  - Accessing Dictionary Values within Arrays


---

# 12. Program Control Flow

- **12.1 Introduction to Program Control Flow**
  - Overview of Conditional Statements and Loops

- **12.2 Conditional Statements**
  - **12.2.1 The `if` Statement**
    - Syntax and Example
  - **12.2.2 The `if-else` Statement**
    - Syntax and Example
  - **12.2.3 The `if-elif` Statement**
    - Syntax and Example
  - **12.2.4 Nested `if` Statements**
    - When and How to Use Nested `if` Statements

- **12.3 Python Indentation**
  - Importance of Indentation in Python

- **12.4 Looping and Iteration**
  - **12.4.1 The `for` Loop**
    - Syntax and Example
  - **12.4.2 The `for in` Loop**
    - Iterating Over Sequences (Lists, Strings, etc.)
  - **12.4.3 The `while` Loop**
    - Syntax and Example
  - **12.4.4 The `else` Statement with Loops**
    - How `else` Works with `for` and `while` Loops
  - **12.4.5 Looping Over Lists**
    - Example: Iterating Through List Elements
  - **12.4.6 Looping Over Strings**
    - Example: Iterating Through String Characters
  - **12.4.7 Nested Loops**
    - Using Loops Within Loops

- **12.5 Loop Control Statements**
  - **12.5.1 `break` Statement**
    - Exiting Loops Early
  - **12.5.2 `continue` Statement**
    - Skipping the Current Iteration

- **12.6 The `range()` Function**
  - **12.6.1 Introduction to `range()`**
    - Basic Syntax and Usage
  - **12.6.2 Types of `range()` Function**
    - Different Ways to Use `range()`
  - **12.6.3 Use of `range()` in Loops**
    - Using `range()` to Generate Sequences
  - **12.6.4 `range()` vs `xrange()`**
    - Differences between `range()` and `xrange()` in Python 2.x and Python 3.x

- **12.7 Switch Case (Simulated in Python)**
  - Python doesn't have a direct `switch` statement, but it can be simulated with `if-elif` statements

- **12.8 Python Iterators**
  - What Iterators Are and How They Work

- **12.9 Python Generators**
  - Introduction to Generators and `yield`

---

# 13. Introduction to Functions

- **13.1 Built-In Functions**
  - Introduction to Python's Built-in Functions
  - Examples: `map()`, `zip()`, `reduce()`, `filter()`, `any()`, `chr()`, `ord()`, `sorted()`, `globals()`, `locals()`, `all()`, etc.

- **13.2 Introduction to Functions**
  - What Are Functions and Why Are They Used?

- **13.3 Structure of Python Functions**
  - Defining Functions: Syntax and Structure
  - Example of a Simple Function

- **13.4 Types of Functions**
  - **13.4.1 User-Defined Functions (UDFs)**
    - Creating and Using User-Defined Functions
    - Structure of a Python Program with Respect to UDFs
    - Invoking UDFs
  - **13.4.2 Recursion Functions**
    - Understanding Recursion in Python Functions

- **13.5 Function Parameters**
  - **13.5.1 Default Parameters / Optional Parameters**
    - How to Define Parameters with Default Values
  - **13.5.2 Non-default Parameters**
    - Parameters Without Default Values
  - **13.5.3 Named/Keyword Parameters**
    - How to Pass Parameters by Name
  - **13.5.4 Non-keyword Arguments**
    - Passing Arguments Without Specifying Parameter Names
  - **13.5.5 Arbitrary Arguments (`*args` and `**kwargs`)**
    - Using `*args` for Variable-Length Arguments
    - Using `**kwargs` for Arbitrary Keyword Arguments

- **13.6 Function Execution**
  - **13.6.1 Flow of Execution in Functions**
    - How Python Executes Functions and Flow Control

- **13.7 Return Statements**
  - Using `return` to Exit a Function and Return Values
  - Returning Multiple Values from a Function

- **13.8 Lambda Functions**
  - Introduction to Lambda Functions (Anonymous Functions)
  - Syntax and Example of Lambda Functions

- **13.9 Functional Programming Tools**
  - **13.9.1 `map()`**
    - Using `map()` to Apply Functions to Iterable
  - **13.9.2 `filter()`**
    - Using `filter()` to Filter Iterables
  - **13.9.3 `reduce()`**
    - Using `reduce()` for Accumulating Results Across an Iterable

- **13.10 Advanced Function Concepts**
  - **13.10.1 Python Closures**
    - Understanding Closures and Their Use
  - **13.10.2 Function Decorators**
    - What Are Decorators and How They Work
  - **13.10.3 Decorators with Parameters**
    - Creating and Using Decorators That Accept Parameters
  - **13.10.4 Memoization Using Decorators**
    - Caching Function Results with Decorators for Performance
  - **13.10.5 Partial Functions**
    - Understanding Partial Functions in Python

- **13.11 Special Python Function Concepts**
  - **13.11.1 `yield` Instead of `return`**
    - Introduction to `yield` for Generators
  - **13.11.2 First-Class Functions**
    - How Functions Are Treated as First-Class Objects in Python
  - **13.11.3 Precision Handling**
    - Handling Precision with Python Functions (e.g., `round()`)

- **13.12 Miscellaneous Function-Related Topics**
  - **13.12.1 `help()` Function**
    - Using `help()` for Getting Information About Functions and Modules
  - **13.12.2 `__import()__` Function**
    - Dynamic Importing of Modules in Python
  - **13.12.3 Coroutines in Python**
    - Understanding and Using Coroutines in Python
  - **13.12.4 Python Bit Functions on `int`**
    - Functions like `bit_length()`, `to_bytes()`, and `from_bytes()`
  - **13.12.5 Using Collections as Function Parameters**
    - Passing Collections (like lists, dictionaries) to Functions

---
# 14. Project-I

- **14.1 Rock Paper Scissors Game**
  - Overview of the game mechanics
  - User input and random choice generation
  - Displaying results and handling user decisions
  - Keeping track of scores

- **14.2 Grading Calculator**
  - Understanding the grading system
  - Taking user input for marks/grades
  - Calculating grades based on predefined thresholds
  - Displaying the final grade

- **14.3 Unit Converter**
  - Overview of units (e.g., length, weight, temperature)
  - Creating a menu for selecting the conversion type
  - Taking user input for values and conversion units
  - Displaying the result of the conversion

- **14.4 Number Guessing Game**
  - Explaining the mechanics of the guessing game
  - Generating a random number within a given range
  - User input and providing feedback (too high, too low, correct)
  - Setting up a loop for multiple attempts
  - Keeping track of the number of attempts

---
# 15. File Operations

- **15.1 Introduction to File Operations**
  - Understanding Files in Python
  - Text vs. Bytes Files

- **15.2 File Modes**
  - **15.2.1 Writing Modes**: `w`, `w+`, `wb`
  - **15.2.2 Reading Modes**: `r`
  - **15.2.3 Choosing the Appropriate Mode**: When to Use Each Mode

- **15.3 Opening a File**
  - Using `open()` to Access Files
  - File Object and File Handle

- **15.4 Reading Files**
  - Reading Entire File Content: `read()`
  - Reading Line by Line: `readline()` and `readlines()`
  - Iterating Over File Content

- **15.5 Writing Files**
  - Writing to a File: `write()` and `writelines()`
  - Writing in Text and Binary Format

- **15.6 File Methods**
  - Common File Methods: `seek()`, `tell()`, `flush()`, `close()`

- **15.7 Using the `with` Keyword**
  - Automatically Managing File Resources with `with` (Context Manager)

- **15.8 Working with Specific File Formats**
  - **15.8.1 TXT Files**
    - Basic Operations on Plain Text Files
  - **15.8.2 CSV Files**
    - Reading CSV Files with `csv.reader()`
    - Writing to CSV Files with `csv.writer()`
    - `DictReader` and `DictWriter` for Working with CSV as Dictionaries
    - Handling `writerow()` and `writerows()` Methods
  - **15.8.3 MS Excel Files**
    - Using Python Libraries like `openpyxl` or `pandas` to Read/Write Excel Files
    - Working with `.xls` and `.xlsx` formats
  - **15.8.4 JSON Files**
    - Parsing JSON Files with `json.load()` and Writing with `json.dump()`
    - Converting Python Objects to JSON Format and Vice Versa
  - **15.8.5 XML Files**
    - Parsing XML Files with Libraries like `ElementTree`
    - Working with XML Nodes and Creating XML Structures

- **15.9 Parsing and Node Creation**
  - Extracting Data from Files (like XML, JSON)
  - Creating Nodes and Structuring Data in Files


---
# 16. Advanced Python

- **16.1 Introduction to Object-Oriented Programming (OOP)**
  - Overview of OOP Concepts
  - Comparison with Procedure-Oriented Programming (POP)

- **16.2 Core Features of OOP**
  - **16.2.1 Classes and Objects**
    - Creating Classes and Objects
    - Classes as User-Defined Data Types
    - Creating Objects by Passing Values
  - **16.2.2 Encapsulation**
    - Hiding Data and Methods
    - Public and Private Members (Accessors and Modifiers)
    - Accessor Methods (Getters/Setters)
  - **16.2.3 Abstraction**
    - Hiding Implementation Details
    - Abstract Classes and Methods
    - Interfaces vs Abstract Classes

- **16.3 Inheritance in OOP**
  - **16.3.1 Types of Inheritance**
    - Single, Multiple, Multilevel, Hierarchical, Hybrid Inheritance
  - **16.3.2 Constructor in Inheritance**
    - Constructors in Child Classes
    - Overriding Superclass Constructors
  - **16.3.3 Super() Method**
    - Using `super()` to Call Methods and Constructors in Parent Classes
  - **16.3.4 Method Resolution Order (MRO)**
    - How Python Resolves Method Calls in Inheritance

- **16.4 Polymorphism in OOP**
  - **16.4.1 Method Overloading**
    - Defining Methods with the Same Name but Different Signatures
  - **16.4.2 Operator Overloading**
    - Overloading Operators to Define Custom Behavior
  - **16.4.3 Method Overriding**
    - Overriding Parent Class Methods in Child Classes

- **16.5 Advanced OOP Concepts**
  - **16.5.1 Inner Classes**
    - Creating and Using Inner Classes
  - **16.5.2 Passing Members Between Classes**
    - Passing Members of One Class to Another Class
  - **16.5.3 Duck Typing Philosophy**
    - Understanding Python’s Approach to Object Behavior

- **16.6 Working with Classes and Objects**
  - **16.6.1 `__name__=="__main__"`**
    - Understanding the Special Name Variable
  - **16.6.2 Types of Variables in Classes**
    - Instance Variables, Class Variables, Static Variables
  - **16.6.3 Class Methods and Static Methods**
    - Defining and Using Class and Static Methods
  - **16.6.4 Dunder Methods (Magic Methods)**
    - Common Dunder Methods: `__init__()`, `__str__()`, `__repr__()`, `__del__()`, and others

- **16.7 Class Properties and Attributes**
  - **16.7.1 Class and Instance Attributes**
    - Distinction Between Class and Instance Attributes
  - **16.7.2 Changing Class Members**
    - Modifying Class and Instance Attributes
  - **16.7.3 Private and Public Variables**
    - Access Modifiers and Encapsulation

- **16.8 Miscellaneous Advanced Python Topics**
  - **16.8.1 Constructors and Destructors**
    - Understanding `__init__()` and `__del__()`
  - **16.8.2 First-Class Functions**
    - Treating Functions as Objects in Python
  - **16.8.3 Meta Programming with Metaclasses**
    - Understanding Metaclasses and Their Role in Customizing Class Creation
  - **16.8.4 Reflection**
    - Inspecting and Modifying Python Classes and Objects at Runtime
  - **16.8.5 Garbage Collection**
    - Python’s Garbage Collection Mechanism and Memory Management



---

# 17. Exception Handling

- **17.1 Types of Errors in Python**
  - **17.1.1 Compile Time Errors**
    - Errors detected during code compilation (Syntax errors)
  - **17.1.2 Runtime Errors**
    - Errors that occur during program execution (e.g., division by zero, file not found)
  - **17.1.3 Logical Errors**
    - Errors that occur due to incorrect logic (e.g., wrong calculations or logic flaws)

- **17.2 Exceptions in Python**
  - Introduction to Exceptions: What are exceptions and why do they occur?

- **17.3 Exception Handling Mechanisms**
  - **17.3.1 try and except Clauses**
    - Syntax and Usage
    - Handling specific exceptions
  - **17.3.2 finally Clause**
    - Ensuring Cleanup, Even After Exception
    - Use Cases of `finally`
  - **17.3.3 else Clause**
    - Handling Code After try block if no Exception is Raised

- **17.4 Raising and Asserting Exceptions**
  - **17.4.1 `raise` Statement**
    - Raising Custom Exceptions
  - **17.4.2 `assert` Statement**
    - Debugging with Assertions

- **17.5 Logging Exceptions**
  - Using the `logging` Module to Record Errors
  - Benefits of Logging in Large Applications

- **17.6 Predefined Exceptions**
  - Common Built-in Exceptions: `ValueError`, `IndexError`, `KeyError`, etc.
  - Handling Predefined Exceptions

- **17.7 User-Defined Exceptions**
  - Creating Custom Exception Classes
  - Raising Custom Exceptions with the `raise` keyword

- **17.8 Cleanup Actions in Exception Handling**
  - How to Clean Up Resources After Exception Handling
  - The Role of `finally` in Cleanup Actions

- **17.9 NZEC Error**
  - Understanding Non-Zero Exit Code (NZEC)
  - Common Causes and Fixes for NZEC Errors

---

# **18.1 Testing**
- **18.1.1 Introduction to Software Testing**
- **18.1.2 Unit Testing in Python**
  - Introduction to `unittest`
  - Writing test cases
  - Assertions
- **18.1.3 Testing Frameworks**
  - `unittest`, `pytest`, `doctest`
- **18.1.4 Mocking and Patching**
  - Using `unittest.mock`
- **18.1.5 Test-Driven Development (TDD)**
- **18.1.6 Continuous Integration and Testing**
  - Integrating with CI tools
- **18.1.7 Test Coverage**
  - Tools for measuring coverage
- **18.1.8 Behavior-Driven Development (BDD)**
- **18.1.9 Integration Testing**
- **18.1.10 End-to-End (E2E) Testing**
- **18.1.11 Test Reports and Logging**
- **18.1.12 Best Practices in Testing**

---

# 19. Project-II

- **19.1 OOP-Based Application**
  - Overview of Object-Oriented Programming (OOP)
  - Designing the Project with OOP Concepts
  - Identifying Classes, Objects, and Methods for the Application
  - Using Inheritance, Polymorphism, and Encapsulation
  - Example Project: Build a Simple Banking System, Student Management System, or a Library Management System
  - Testing the OOP Application and Debugging Any Issues
  - Final Refinement and Code Optimization


# 20. Python Collections

- **20.1 Introduction to Python Collections**
  - Overview of Python's Built-in Collection Modules
  - Importance of Collections in Python Programming

- **20.2 Counters**
  - What is a Counter?
  - Creating a Counter Object
  - Counting Occurrences of Elements
  - Operations with Counters (e.g., most_common(), subtract())

- **20.3 OrderedDict**
  - What is an OrderedDict?
  - Key Differences Between OrderedDict and Regular Dictionaries
  - Operations on OrderedDict (e.g., popitem(), move_to_end())

- **20.4 DefaultDict**
  - Introduction to DefaultDict
  - How DefaultDict Differs from Regular Dicts
  - Setting Default Values Automatically for Missing Keys

- **20.5 ChainMap**
  - What is ChainMap?
  - Combining Multiple Dictionaries or Mappings
  - Benefits of Using ChainMap

- **20.6 NamedTuple**
  - What is a NamedTuple?
  - Creating and Using NamedTuple for Structuring Data
  - Benefits Over Regular Tuples

- **20.7 DeQue (Deque)**
  - Introduction to Deque
  - Differences Between List and Deque
  - Operations with Deque (e.g., append(), pop(), appendleft(), popleft())

- **20.8 Heap**
  - Introduction to Heap
  - Using heapq to Work with Heaps
  - Operations like heapify(), heappush(), and heappop()

- **20.9 UserDict (from collections module)**
  - What is UserDict?
  - Customizing Dictionary Behaviors Using UserDict
  - Extending UserDict for Custom Dictionary Classes

- **20.10 UserList (from collections module)**
  - What is UserList?
  - Customizing List Behaviors Using UserList
  - Extending UserList for Custom List Classes

- **20.11 UserString (from collections module)**
  - What is UserString?
  - Customizing String Behaviors Using UserString
  - Extending UserString for Custom String Classes

---
# 21. Modules and Packages

- **21.1 Introduction to Modules and Packages**
  - What are Modules and Packages?
  - Difference Between a Module and a Package

- **21.2 Built-in Modules**
  - Overview of Python's Built-in Modules
  - Commonly Used Built-in Modules (e.g., `os`, `sys`, `time`, `datetime`, `calendar`, `random`, etc.)
  - Working with Built-in Modules: Importing and Using

- **21.3 Installing External Modules using PIP**
  - Introduction to PIP (Python Package Index)
  - How to Install Python Modules using `pip`
  - Example: Installing Packages like `requests`, `numpy`, etc.

- **21.4 Importing Modules in Python**
  - **21.4.1 Basic Import Syntax**
    - Syntax: `import module_name`
  - **21.4.2 Importing Specific Functions or Classes**
    - Syntax: `from module_name import function_name`
  - **21.4.3 Importing All Functions from a Module**
    - Syntax: `from module_name import *`
  
- **21.5 Aliasing Modules**
  - Why Use Aliases for Modules?
  - Syntax: `import module_name as alias_name`
  - Example: `import numpy as np`

- **21.6 Reloading a Module**
  - Introduction to Module Reloading
  - Syntax: `import importlib; importlib.reload(module_name)`
  - Use Cases for Reloading Modules (e.g., during development)

- **21.7 Working with Specific Built-in Modules**
  - **21.7.1 `os` Module**
    - File and Directory Manipulation
    - Working with Paths and Environment Variables
  - **21.7.2 `time` and `datetime` Modules**
    - Time and Date Operations
    - Time Calculation and Formatting
  - **21.7.3 `calendar` Module**
    - Working with Calendars and Date Manipulation
  - **21.7.4 `sys` Module**
    - Accessing System Parameters and Functions

- **21.8 Circular Imports in Python**
  - Understanding Circular Imports
  - How Circular Imports Happen and How to Prevent Them
  - Best Practices for Importing to Avoid Circular Dependencies

- **21.9 User-Defined Modules**
  - Creating Your Own Modules
  - Organizing Code into Modules for Reusability
  - Importing Your Own Module

- **21.10 Structure of Python Modules**
  - Overview of a Typical Python Module
  - Defining Functions, Classes, and Variables in Modules
  - Using the `__name__` variable to Control Module Execution

---

# 22. Project-III

- **22.1 Introduction to Publishing Packages**
  - What is PyPI (Python Package Index)?
  - Why Publish Packages on PyPI?

- **22.2 Preparing Your Package for Distribution**
  - Structuring Your Project for PyPI
  - Setting up `setup.py`
  - Including `README.md` and other necessary files

- **22.3 Registering and Creating an Account on PyPI**
  - Step-by-Step Guide to Register on PyPI
  - Creating a PyPI Account

- **22.4 Building the Package**
  - Creating a Source Distribution
  - Building a Wheel File

- **22.5 Uploading Your Package to PyPI**
  - Using Twine for Uploading
  - Uploading Your Package to PyPI

- **22.6 Verifying the Upload**
  - How to Check if Your Package Was Successfully Published
  - Testing Package Installation via `pip`

---

# 23. Regular Expressions

- **23.1 Introduction to Regular Expressions**
  - What are Regular Expressions?
  - Syntax and Basics of Regular Expressions

- **23.2 Simple Character Matches**
  - Matching Literal Characters
  - Case Sensitivity in Regular Expressions

- **23.3 Special Characters in Regular Expressions**
  - Understanding Metacharacters (e.g., `.`, `^`, `$`, `[]`, `()`, etc.)

- **23.4 Character Classes**
  - Predefined Character Classes (e.g., `\d`, `\w`, `\s`, etc.)
  - Custom Character Classes (e.g., `[a-z]`, `[0-9]`, etc.)

- **23.5 Quantifiers**
  - Understanding Quantifiers (e.g., `*`, `+`, `?`, `{n}`, `{n,}`)

- **23.6 Forming Regular Expressions**
  - Combining Character Classes and Quantifiers
  - Constructing Regular Expressions for Practical Use

- **23.7 Anchors: Matching at the Beginning or End**
  - Anchors (`^` for start, `$` for end of string)
  - Examples of Anchored Matching

- **23.8 Greedy vs Non-Greedy Matches**
  - Difference Between Greedy and Non-Greedy Matching
  - Using `?` for Non-Greedy Matching

- **23.9 Compiling Regular Expressions**
  - How to Compile Regular Expressions for Efficiency
  - `re.compile()` Function

- **23.10 Grouping in Regular Expressions**
  - Using Parentheses for Grouping
  - Capturing and Non-Capturing Groups
  - Accessing Groups via `group()`

- **23.11 Match Objects**
  - What are Match Objects?
  - Accessing Information from Match Objects (e.g., `start()`, `end()`, `group()`)

- **23.12 Matching Functions: `match()`, `search()`, and `sub()`**
  - **`match()`**: Matching at the Beginning of the String
  - **`search()`**: Searching Anywhere in the String
  - **`sub()`**: Replacing Text Using Regular Expressions

- **23.13 Matching vs Searching**
  - Difference Between `match()` and `search()`
  - When to Use Each Function

- **23.14 Splitting a String Using Regular Expressions**
  - Using `re.split()` to Split Strings Based on Patterns

- **23.15 Replacing Text Using Regular Expressions**
  - Using `re.sub()` to Replace Text in a String Based on a Pattern

- **23.16 Flags in Regular Expressions**
  - What are Flags in Regular Expressions?
  - Common Flags (`re.IGNORECASE`, `re.DOTALL`, etc.)
  - Using Flags with Functions like `re.match()`, `re.search()`, `re.sub()`

---

# 24. Multithreading

- **24.1 Introduction to Multithreading**
  - What is Multithreading?
  - Advantages and Disadvantages of Multithreading

- **24.2 Differences Between Processes and Threads**
  - What is a Process?
  - What is a Thread?
  - Key Differences Between Processes and Threads

- **24.3 Concurrent Programming and the Global Interpreter Lock (GIL)**
  - What is Concurrent Programming?
  - Understanding GIL in Python and Its Impact on Multithreading

- **24.4 Uses of Threads**
  - When to Use Multithreading
  - Applications of Threads in Real-World Programs

- **24.5 Defining and Creating Threads**
  - Creating Threads Using `threading.Thread`
  - Overriding `run()` Method
  - Starting a Thread Using `start()`

- **24.6 Thread Class Methods**
  - `start()`, `join()`, `is_alive()`, `name`, `ident`
  - Thread Lifecycle and State

- **24.7 Single Tasking Using Threads**
  - Executing a Single Task in a Thread
  - Example of Single Task Execution

- **24.8 Multi-Tasking Using Multiple Threads**
  - Running Multiple Threads Simultaneously
  - Example of Multi-tasking with Threads

- **24.9 Thread Synchronization**
  - What is Thread Synchronization?
  - Synchronizing Threads Using Locks (e.g., `Lock`, `RLock`)
  - Using `threading.Lock` to Ensure Mutual Exclusion

- **24.10 Avoiding Deadlocks in a Program**
  - What is a Deadlock?
  - How Deadlocks Occur
  - Techniques to Avoid Deadlocks

- **24.11 Communication Between Threads**
  - Introduction to Thread Communication
  - Using `notify()` and `wait()` Methods for Thread Communication
  - Example: Thread Synchronization with `notify()` and `wait()`

- **24.12 Communication Using Queue**
  - Using `queue.Queue` for Thread Communication
  - Example: Producer-Consumer Problem with Queue

- **24.13 Daemon Threads**
  - What Are Daemon Threads?
  - Difference Between Daemon and Non-Daemon Threads
  - When to Use Daemon Threads

---

# 25. Network Programming

- **25.1 Introduction to Network Programming**
  - What is Network Programming?
  - Importance of Networking in Modern Applications
  - Overview of Network Communication

- **25.2 Protocols**
  - Definition of a Protocol
  - Types of Protocols: Communication Rules
  - Key Protocols Used in Network Programming

- **25.3 TCP/IP Protocol**
  - Introduction to TCP/IP
  - How TCP/IP Works
  - Applications of TCP/IP in Networking
  - Difference Between TCP and UDP

- **25.4 User Datagram Protocol (UDP)**
  - Introduction to UDP
  - Features of UDP
  - Comparison: TCP vs UDP
  - Use Cases of UDP

- **25.5 Sockets**
  - What is a Socket?
  - Socket Programming Basics
  - Socket API in Python
  - Types of Sockets: Stream and Datagram

- **25.6 Connecting to a Server**
  - Understanding Client-Server Architecture
  - Using Python to Connect to a Server
  - Creating a Client Socket and Connecting

- **25.7 Knowing IP Address**
  - How to Find Your IP Address
  - Resolving Hostnames to IP Addresses
  - Using `socket.gethostbyname()` in Python

- **25.8 Downloading a Web Page from the Internet**
  - Introduction to HTTP Protocol
  - Using Sockets to Fetch Data from a Web Server
  - Example: Downloading a Simple Web Page

- **25.9 Downloading an Image from the Internet**
  - Fetching Image Data Using HTTP and Sockets
  - Saving the Downloaded Image to Local File System
  - Example: Downloading and Saving an Image

- **25.10 TCP/IP Server and Client**
  - Building a TCP Server in Python
  - Building a TCP Client in Python
  - Client-Server Communication using TCP
  - Example: Simple Chat Application

- **25.11 UDP Server and Client**
  - Building a UDP Server in Python
  - Building a UDP Client in Python
  - Client-Server Communication using UDP
  - Example: Sending and Receiving Messages

- **25.12 File Server and Client**
  - Sending Files Over TCP or UDP
  - Building a File Server and Client in Python
  - Example: File Transfer using Sockets

- **25.13 Sending Data**
  - Methods to Send Data Over a Network
  - Sending Text and Binary Data via Sockets
  - Example: Sending Data from Client to Server

- **25.14 Receiving Data**
  - Receiving Data from Server to Client
  - Handling Data Reception with Sockets
  - Example: Client Receiving Data from Server

- **25.15 Sending a Simple Mail**
  - Introduction to Sending Email via Python
  - Using SMTP to Send Email
  - Example: Sending Email using `smtplib`


---


# 26. Database

- **26.1 Introduction to RDBMS**
  - What is RDBMS (Relational Database Management System)?
  - Features of RDBMS
  - Examples of Popular RDBMS (MySQL, PostgreSQL, Oracle, etc.)

- **26.2 Advantages of DBMS over Files**
  - Centralized Data Management
  - Data Integrity and Consistency
  - Querying and Reporting Capabilities
  - Security Features
  - Multi-user Support

- **26.3 Installation of MySQL**
  - Steps to Install MySQL on Windows/Linux/macOS
  - Setting Up MySQL Server
  - Testing the Installation

- **26.4 Creating MySQL Database Instances**
  - Introduction to Databases in MySQL
  - Creating a New Database in MySQL
  - Listing Databases and Checking Connections

- **26.5 Establishing Connection with MySQL**
  - Using Python to Connect to MySQL
  - Required Libraries (e.g., `mysql-connector-python`, `PyMySQL`)
  - Code Example: Establishing a Connection to MySQL

- **26.6 Executing SQL Queries**
  - Introduction to SQL Syntax
  - Executing SELECT, INSERT, UPDATE, DELETE Queries Using Python
  - Fetching Data from the Database (e.g., `fetchone()`, `fetchall()`)
  - Handling Errors in SQL Queries

- **26.7 Creating Tables using Python**
  - SQL Syntax for Creating Tables
  - Defining Columns and Data Types
  - Example: Creating a Simple Table using Python
  - Validating Table Creation

- **26.8 Inserting Rows into Table**
  - SQL Syntax for Inserting Data (`INSERT INTO`)
  - Inserting Multiple Rows Using Python
  - Using Parameterized Queries to Prevent SQL Injection

- **26.9 Deleting Rows from Table**
  - SQL Syntax for Deleting Rows (`DELETE`)
  - Deleting Specific Records Using Python
  - Ensuring Data Integrity

- **26.10 Updating Rows**
  - SQL Syntax for Updating Data (`UPDATE`)
  - Using Python to Update Specific Rows in the Table
  - Example: Updating User Information

- **26.11 Stored Procedures**
  - Introduction to Stored Procedures in MySQL
  - Creating and Calling Stored Procedures from Python
  - Advantages of Using Stored Procedures
  - Example: Writing and Calling a Stored Procedure in Python

---

# 27. Introduction to Frameworks

- **27.1 Desktop Applications**
  - Overview of Desktop Applications in Python
  - **27.1.1 QT**  
    - Introduction to QT for Desktop Applications  
    - Advantages of QT  
  - **27.1.2 PyGUI**  
    - Overview of PyGUI  
    - Features of PyGUI  
  - **27.1.3 Tkinter**  
    - Tkinter Basics  
    - Building Simple GUI with Tkinter  

- **27.2 Web Applications**
  - Overview of Web Frameworks in Python  
  - **27.2.1 Flask**  
    - Introduction to Flask  
    - Building a Simple Web Application with Flask  
  - **27.2.2 Django**  
    - Overview of Django  
    - Creating a Django Project and App  
    - Django ORM and Models  
  - **27.2.3 FastAPI**  
    - Introduction to FastAPI  
    - FastAPI for building APIs  
    - Async support in FastAPI

- **27.3 Web Development Fundamentals**
  - **27.3.1 HTML**  
    - Basics of HTML for Web Development  
  - **27.3.2 CSS**  
    - Styling Web Pages with CSS  
  - **27.3.3 Migrations**  
    - Database Migrations in Django and Flask  
  - **27.3.4 Views**  
    - Creating Views in Web Frameworks  
  - **27.3.5 MVC**  
    - Model-View-Controller Architecture  
  - **27.3.6 URLs**  
    - Defining and Mapping URLs in Flask/Django  
  - **27.3.7 Jinja Templating**  
    - Introduction to Jinja2 for HTML Templating  
  - **27.3.8 Database**  
    - Database integration in Flask/Django

---

# 28. Working with Audio and Images

- **28.1 Working with Audio Files**  
  - Playing Audio in Python  
  - Using libraries like `pydub`, `pygame`, and `wave`
  - Audio Processing and Effects  


- **28.2 Working with Image Files**  
  - Image Processing with Python  
  - Libraries: `Pillow`, `OpenCV`
  - Basic Image Operations (Resizing, Cropping, Filters)  
  - Image Conversion and Formats  

---

# 29. Project-IV

- **29.1 Flask Application**
  - Building a Flask Application with Web API  
  - Integration with Database (SQLAlchemy, SQLite)  
  - Authentication and Authorization  

---

# 30. Django REST Framework

- **30.1 Introduction to Django REST Framework (DRF)**
  - Setting up Django REST Framework  
  - Building REST APIs using DRF  
  - **30.1.1 JSON**  
    - Working with JSON in DRF  
    - Serializers in DRF  
  - **30.1.2 API Calls**  
    - Making API calls using DRF  
    - Authentication for APIs (Token-based, JWT)

---

# 31. AI, ML, and DS

- **31.1 Numpy**
  - Introduction to Numpy and its Role in Data Science  
  - **31.1.1 ndarray**  
    - Numpy Arrays and Array Creation  
    - Working with Numpy Arrays  
  - **31.1.2 Data Type Objects (dtype)**  
    - Understanding Numpy Data Types  
  - **31.1.3 Indexing and Slicing**  
    - Boolean and Fancy Indexing  
    - Slicing and Indexing with Numpy Arrays  
  - **31.1.4 Iterating Over Array**  
    - Iterating through Numpy Arrays  
  - **31.1.5 Binary Operations**  
    - Performing Binary Operations on Arrays  
  - **31.1.6 Linear Algebra**  
    - Matrix Operations and Linear Algebra in Numpy  
  - **31.1.7 Sorting, Searching, and Counting**  
    - Sorting and Searching in Numpy Arrays  

- **31.2 Pandas**
  - Introduction to Pandas for Data Analysis  
  - **31.2.1 Pandas DataFrame Creation**  
    - Creating DataFrames from Lists, Dicts, and CSV Files  
  - **31.2.2 read_csv()**  
    - Reading CSV Files into DataFrames  
  - **31.2.3 Rows and Columns**  
    - Accessing and Manipulating DataFrames  
  - **31.2.4 Indexing and Selecting**  
    - Indexing, Selecting, and Filtering Data  
  - **31.2.5 Boolean Indexing**  
    - Conditional Selection with Pandas  
  - **31.2.6 Conversion Functions**  
    - Converting Data Types in DataFrames  
  - **31.2.7 Working with Missing Data**  
    - Handling NaN and Missing Values in Pandas  
  - **31.2.8 Pandas Series**  
    - Working with Pandas Series  
  - **31.2.9 Data Analysis Using Pandas**  
    - Aggregating, Grouping, and Analyzing Data  

- **31.3 Scipy**
  - Introduction to Scipy for Scientific Computing  
  - Numerical Integration, Optimization, and Interpolation

- **31.4 Matplotlib, Seaborn, Plotly**
  - **31.4.1 Matplotlib**  
    - Creating Static, Animated, and Interactive Plots  
  - **31.4.2 Seaborn**  
    - Statistical Data Visualization with Seaborn  
  - **31.4.3 Plotly**  
    - Interactive Plots and Dashboards using Plotly

- **31.5 Sklearn, Pytorch, TensorFlow**
  - **31.5.1 Sklearn**  
    - Introduction to Scikit-Learn for Machine Learning  
    - Supervised and Unsupervised Learning Algorithms  
  - **31.5.2 Pytorch**  
    - Introduction to Pytorch for Deep Learning  
    - Building Neural Networks with Pytorch  
  - **31.5.3 TensorFlow**  
    - Introduction to TensorFlow for Machine Learning  
    - Building Deep Learning Models with TensorFlow  

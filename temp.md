# Core Python Syllabus

## 1. GETTING STARTED
- History & need of Python, Founder, Date of creation
- Popular Applications built using Python
- Advantages of Python
- Disadvantages of Python
- Namespace and Scope in Python
- Different versions and minor differences (2.x vs 3.x)
- Installing Python
- Program structure
- Interactive Shell
- Executable or script files
- User Interface or IDE
- Python Virtual Machine

## 2. PYTHON FUNDAMENTALS
- Basic Syntax (indentation, no semicolon, no parenthesis)
- Flow of the Python Program
- Working with Interactive mode (Evaluating expressions)
- Working with Script mode
- Python Character Set
- Python Tokens, Keywords, Pep8
- Identifiers, Literals, Operators
- Variables and Assignments in Python vs Other Languages
- Input and Output in Python
  - The `input()` function
    - Single input, Multiple input
    - Vulnerability in `input()` function - Python 2.x
  - The `print()` function
    - New line
    - Parameters: `end`, `sep`
    - `raw_input()`
    - Output formatting
  - `type()` function
  - `id()` function

## 3. INTRODUCTION TO DATA HANDLING
- Data Types (static vs dynamic)
- Numbers
- Bool
- Strings
- Type Conversion
- Constants
- None
- Sequence
- Maps
- Data Structures
  - Lists
  - Tuples
  - Dictionary
  - Set, and Frozenset

## 4. OPERATORS
- Arithmetic Operators
- Relational Operators
- Logical Operators
- Membership Operators
- Identity Operators
- Bitwise Operators
- Assignment Operators
- Operators Precedence
- Evaluating Expression
- Type Casting
- MISC
  - Division operator
  - Operator Overloading
  - Any and all operators in Python
  - Inplace and standard operators in Python
  - Equivalent operator (`==`) vs. membership operator (`is`)
  - Membership and Identity operators (`in`, `not in`, `is`, `is not`)

## 5. DEBUGGING
- Syntax Errors
- Runtime Errors
- Semantic Errors
- How to locate and resolve errors
- More on errors in the Exception Handling Module

## 6. STRING MANIPULATION
- Introduction to Python String (Mutation)
- Accessing Individual Elements
- String Operators
- String Slices
- String Functions and Methods
  - `upper`, `Isupper`, `lower`, `islower`, `count`, `strip`, `replace`, `join`, `split`, `substring`, `index(+ve, and -ve)`, and many more.

## 7. LIST MANIPULATION
- Introduction to Python List
- Creating List
- Accessing List
- Joining List
- Replicating List
- List Slicing
- List Methods
  - `Append`, `pop`, `prepend`, `sort`, `count`, `index(+ve, and -ve)`, `insert`, `remove`
- List Comprehension
- Mutation
- Packing and unpacking
- Limitations of List
- Iteration
- Membership
- Concatenation
- Multi-dimensional lists
- Deleting
- Reassigning

## 8. TUPLES
- Introduction to Tuple
- Creating Tuples
- Packing and unpacking tuples
- Single item and Multiple Item tuple
- Accessing Tuples
- Joining Tuples
- Replicating Tuples
- Tuple Slicing
- Mutation
- Deleting
- Reassigning
- Limitations of Tuple
- Tuple functions

## 9. DICTIONARIES
- Introduction to Dictionary
- Accessing values in dictionaries
- Properties
- Methods
  - `Keys`, `values`, `items`, `get`, merging, `pop`, `clear`, `copy`
- Dictionary Comprehension
- Mutation
- Packing and unpacking
- Limitation of Dictionaries
- Deleting
- Membership

## 10. SET AND FROZENSET
- Introduction to Set and Frozenset
- Creating Set and Frozenset
- Accessing and Joining
- Replicating and Slicing
- Mutation
- Packing and unpacking

## 11. NESTED DATA STRUCTURES
- Array
  - Array of Array
  - Array of dicts
  - Arrays of tuples
- Dictionary
  - Array as values
  - Tuple as value
  - Dictionary as values

## 12. PROGRAM CONTROL FLOW
- Conditional Statements: Simple, Multiple, Nesting
  - The `if` Statement
  - The `if-else` Statement
  - The `if-elif` Statement
  - Nested `if` Statements
  - Python Indentation
- Looping and Iteration
  - The `For` Loop
  - The `For in` Loop
  - The `While` Loop
  - Else statement with loop (for, while)
  - Loop over list
  - Loop over string
- Nested Loops
  - `Break` and `Continue`
- The `Range` Function
  - Introduction to `range()`
  - Types of `range()` function
  - Use of `range()` function
  - `range()` vs. `xrange()`
- Switch case
- Python Iterators
- Python Generators

## 13. INTRODUCTION TO FUNCTIONS
- Built-In Functions
  - Introduction to Functions
  - Using a Functions
  - Python Function Types
  - Structure of Python Functions
  - E.g. - `map`, `zip`, `reduce`, `filter`, `any`, `chr`, `ord`, `sorted`, `globals`, `locals`, `all`, etc.
- User Defined Functions
  - Structure of a Python Program w.r.t. UDF
  - Invoking UDF
  - Flow of Execution
  - Types of Functions
    - Default Parameters/Optional Parameters
    - Non-default Parameters
    - Named/Key-word Parameters
    - Non-Key word arguments
    - Arbitrary Arguments
  - `Return` statement
  - Arguments and Parameters (function signature)
  - Scope of Variables (global vs. local)
  - Recursion Function
  - Lambda function
    - Anonymous functions
    - `filter()`
    - `map()`
    - `reduce()`
- MISC
  - Write an empty Function in Python – `pass` statement
  - `Yield` instead of `return`
  - Return multiple values
  - Partial functions in Python
  - First Class functions in python
  - Precision Handling
  - `*args` and `**kwargs`
  - Python closures
  - Function Decorators
  - Decorators in Python
  - Decorators with parameter in python
  - Memoization using decorators in python
  - `Help` function in python
  - `__import()__` function
  - `range()` doesn’t return an iterator
  - Coroutine in Python
  - Python bit functions on int (`bit_length`, `to_bytes`, and `from_bytes`)
  - Collection as parameter

## 14. PROJECT-I
- Rock Paper Scissor Game
- Grading Calculator
- Unit Converter
- Number Guessing

## 15. FILE OPERATIONS
- Text and Bytes files
  - Modes (`w`, `w+`, `wb`, `r`)
  - `With` keyword
  - Opening a file
  - Reading and Writing Files
  - File methods
- Other File tools
  - TXT
  - CSV
    - Reader
    - Dict Reader
    - Writer
    - `Writerow`
    - `Writerows`
  - MS Excel files
  - JSON and XML
    - Parsing
    - Node Creation

## 16. ADVANCED PYTHON
- OOPS Concept
  - Procedure Oriented Approach
  - Features of OOPS
    - Classes and Objects
    - Encapsulation
    - Abstraction
    - Inheritance
    - Polymorphism
- Classes as User-Defined Data Type
  - Defining Classes
  - `Self` Variable
  - Types of Variables
  - Constructor
  - Namespaces
  - Types of methods
  - Passing members of one class to another class.
  - Inner class
- Inheritance
  - Constructor in inheritance
  - Overriding super class constructors and methods
  - `Super()` method
  - Types of inheritance
  - Method Resolution Order
  - Duck Typing Philosophy of Python
- Polymorphism
  - Method overloading
  - Operator overloading
  - Method overriding
- Abstraction and Interfaces
  - Abstract methods and classes
  - Interfaces
  - Abstract classes vs interface
- Objects as Instances of Classes
- If `__name__=="__main__"`
- Creating Class and Objects
- Creating Objects By Passing Values
- Variables & Methods in a Class
- Accessor
  - Private (`_`)
  - Public
- `Self` parameter
- Class Properties, and Dunder methods
- MISC
  - Class and static variable in Python
  - Class method and static method in Python
  - Changing class members
  - Constructors
  - Destructors
  - First class function
  - Meta Programming with metaclasses
  - Class and instance attribute
  - Reflection
  - Garbage Collection

## 17. EXCEPTION HANDLING
- Types of errors
  - Compile time errors
  - Runtime errors
  - Logical Errors
  - Exceptions
- Exception Handling (`try`, `except`, and `finally` clauses)
- `raise`, and `assert` statements
- Logging exceptions
- Pre-defined Exception
- User Defined
- Clean up action
- NZEC error

## 18. PROJECT-II
- OOP Based Application

## 19. PYTHON COLLECTIONS
- Counters
- OrderedDict
- Default Dict
- ChainMap
- NamedTuple
- DeQue
- Heap
- `Collections.UserDict`
- `Collections.UserList`
- `Collections.UserString`

## 20. MODULES AND PACKAGES
- Built-in Modules
  - Installing Modules using PIP
  - Importing Modules in Python Programs
  - Aliasing modules
  - Reloading a module
  - Working with Random Modules
  - E.g. - `builtins`, `os`, `time`, `datetime`, `calendar`, `sys`, etc.
  - Circular Import...
- User Defined Functions
  - Structure of Python Modules

## 21. PROJECT-III
- Publish a package in PyPI community

## 22. REGULAR EXPRESSIONS
- Regular expression introduction and syntax
- Simple character matches
- Special characters
- Character classes
- Quantifiers
- Forming regular expressions
- Matching at the beginning or end
- Greedy matches
- Compiling regular expressions
- Grouping
- Match objects
- `Match()`, `Search()` and `sub()` functions
- Matching vs searching
- Splitting a string
- Replacing text
- Flags

## 23. MULTITHREADING
- Differences between process and thread
- Concurrent programming and GIL
- Uses of threads
- Defining threads
- Thread class methods
- Single tasking using threads
- Multi-tasking using multiple threads
- Thread synchronization
- Avoiding deadlocks in a program
- Communication between threads
  - Communication using `notify()` and `wait()` methods
  - Communication using queue
- Daemon threads

## 24. NETWORK PROGRAMMING
- Introduction to Network programming
- Protocols
  - TCP/IP Protocol
  - User Datagram Protocol
- Sockets
- Connect to server
- Knowing IP Address
- Downloading a web page from the internet
- Downloading an image from the internet
- TCP/IP Server and client
- UDP Server and client
- File server
- File client
- Sending data
- Receiving data
- Sending a simple mail

## 25. DATABASE
- Introduction to RDBMS
- Advantages of DBMS over files
- Installation of MySQL
- Creating MySQL database instances
- Establishing connection with MySQL
- Executing SQL Queries
- Creating tables using Python
- Inserting Rows into table
- Deleting rows from table
- Updating rows
- Stored procedures

## 26. INTRODUCTION TO FRAMEWORKS
- Desktop Applications
  - QT
  - PyGUI
  - Tkinter
- Web Applications
  - Flask
  - Django
  - FastAPI
- Flask Framework
  - HTML
  - CSS
  - Migrations
  - Views
  - MVC
  - URLs
  - Jinja Templating
  - Database

## 27. WORKING WITH AUDIO AND IMAGES

## 28. PROJECT-IV
- Flask Application

## 29. DJANGO REST FRAMEWORK
- JSON
- API Calls

## 30. AI, ML and DS
- **Numpy**
  - `ndarray`
  - Array Creation
  - Data Type Objects (`dtype`)
  - Indexing
  - Slicing and Indexing (Boolean, Fancy)
  - Iterating Over Array
  - Binary Operations
  - Linear Algebra
  - Sorting, Searching, and Counting
- **Pandas**
  - Pandas Data Frame Creation
  - `read_csv()`
  - Rows and Columns
  - Indexing and Selecting
  - Boolean Indexing
  - Conversion Functions
  - Working with missing data
  - Pandas Series
  - Data Analysis Using Pandas
- **Scipy**
- **Matplotlib, Seaborn, Plotly**
- **Sklearn, Pytorch, TensorFlow**

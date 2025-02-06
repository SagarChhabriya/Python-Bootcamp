# Case-Match in Python (Structural Pattern Matching)

Introduced in **Python 3.10**, the `match` statement (also known as **structural pattern matching**) provides a powerful way to handle complex conditional logic. It is similar to `switch-case` in other languages but more flexible and expressive.


<span style="display: flex; justify-content: space-between; width: 100%; align-items: center;">
    <a href="../12-module-12-program-control-flow/session-12.0.md">
        <img src="https://img.shields.io/badge/Previous-Program_Flow_Control-blue" width="250" height="35">
    </a>
    <a href="../13-module-13-functions/README.md">
        <img src="https://img.shields.io/badge/Next-Functions-brightgreen" width="160" height="35">
    </a>
</span>
<br><br>

---

## **1. Basic Syntax of `match`**
- The `match` statement compares a value against a series of patterns and executes the corresponding block of code for the first matching pattern.

- **Syntax**:

  ```python
  match value:
      case pattern1:
          # Code to execute if pattern1 matches
      case pattern2:
          # Code to execute if pattern2 matches
      case _:
          # Default case (optional)
  ```

- **`match variable:`** – You begin by specifying the variable you want to check.
- **`case pattern:`** – The specific pattern you want to match.
- **`case _:`** – The underscore (`_`) is a catch-all or default case when no other patterns match. It's similar to `else` in an `if`-`elif`-`else` chain.


---

## **2. Matching Literals**
- You can match against specific literal values (e.g., integers, strings, booleans).
- **Example**:
  ```python
  def describe_number(num):
      match num:
          case 0:
              print("Zero")
          case 1:
              print("One")
          case _:
              print("Some other number")

  describe_number(0)  # Output: Zero
  describe_number(5)  # Output: Some other number
  ```

---

### 3. **Matching Types**

You can match by the type of the variable:

```python
x = 5

match x:
    case int():
        print("It's an integer")
    case str():
        print("It's a string")
    case _:
        print("Unknown type")
```

Output:
```
It's an integer
```


## **4. Matching Sequences**
- You can match against sequences like lists, tuples, or strings.
- **Example**:
    ```python
    x = [1, 2, 3]

    match x:
        case [1, 2, 3]:
            print("Matched the exact list [1, 2, 3]")
        case [1, _, _]:  # Matches lists starting with 1, followed by any two elements
            print("Starts with 1")
        case _:
            print("No match")
    ```

- **Example:** case-match through function
    ```python
    def process_sequence(seq):
        match seq:
            case [1, 2, 3]:
                print("Sequence matches [1, 2, 3]")
            case [x, y, z]:
                print(f"Sequence has three elements: {x}, {y}, {z}")
            case _:
                print("Unknown sequence")

    process_sequence([1, 2, 3])  # Output: Sequence matches [1, 2, 3]
    process_sequence([4, 5, 6])  # Output: Sequence has three elements: 4, 5, 6
    process_sequence([1, 2])     # Output: Unknown sequence
    ```

---

## **5. Matching with Wildcards**
- Use `_` as a wildcard to match any value.
- **Example**:
  ```python
  def process_data(data):
      match data:
          case [1, _, 3]:
              print("First and third elements are 1 and 3")
          case _:
              print("No match")

  process_data([1, 2, 3])  # Output: First and third elements are 1 and 3
  process_data([1, 9, 3])  # Output: First and third elements are 1 and 3
  process_data([2, 3, 4])  # Output: No match
  ```

---

## **5. Matching with Variables**
- You can capture parts of the matched pattern into variables.
- **Example**:
  ```python
  def process_point(point):
      match point:
          case (0, 0):
              print("Origin")
          case (x, 0):
              print(f"Point on X-axis at {x}")
          case (0, y):
              print(f"Point on Y-axis at {y}")
          case (x, y):
              print(f"Point at ({x}, {y})")

  process_point((0, 0))  # Output: Origin
  process_point((3, 0))  # Output: Point on X-axis at 3
  process_point((0, 4))  # Output: Point on Y-axis at 4
  process_point((2, 3))  # Output: Point at (2, 3)
  ```

---

## **6. Matching with Guards**
- Use `if` conditions (guards) to add additional constraints to patterns.
- **Example**:
  ```python
  def check_number(num):
      match num:
          case x if x > 0:
              print(f"Positive number: {x}")
          case x if x < 0:
              print(f"Negative number: {x}")
          case _:
              print("Zero")

  check_number(5)   # Output: Positive number: 5
  check_number(-3)  # Output: Negative number: -3
  check_number(0)   # Output: Zero
  ```

---

## **7. Matching Dictionaries**
- You can match against dictionaries and extract specific keys.
- **Example**:
  ```python
  def process_user(user):
      match user:
          case {"name": name, "age": age}:
              print(f"User {name} is {age} years old")
          case _:
              print("Invalid user data")

  process_user({"name": "Alice", "age": 25})  # Output: User Alice is 25 years old
  process_user({"name": "Bob"})              # Output: Invalid user data
  ```

---

## **8. Matching Classes**
- You can match against objects of custom classes.
- **Example**:
  ```python
  class Point:
      def __init__(self, x, y):
          self.x = x
          self.y = y

  def process_point(point):
      match point:
          case Point(x=0, y=0):
              print("Origin")
          case Point(x=x, y=0):
              print(f"Point on X-axis at {x}")
          case Point(x=0, y=y):
              print(f"Point on Y-axis at {y}")
          case Point(x=x, y=y):
              print(f"Point at ({x}, {y})")

  process_point(Point(0, 0))  # Output: Origin
  process_point(Point(3, 0))  # Output: Point on X-axis at 3
  process_point(Point(0, 4))  # Output: Point on Y-axis at 4
  process_point(Point(2, 3))  # Output: Point at (2, 3)
  ```

---

## **9. Matching Nested Structures**
- You can match against nested data structures like lists of lists or dictionaries of dictionaries.
- **Example**:
  ```python
  def process_nested(data):
      match data:
          case {"name": name, "scores": [math, science]}:
              print(f"{name} scored {math} in Math and {science} in Science")
          case _:
              print("Invalid data")

  process_nested({"name": "Alice", "scores": [90, 85]})  # Output: Alice scored 90 in Math and 85 in Science
  process_nested({"name": "Bob"})                       # Output: Invalid data
  ```

---

## **10. Combining Patterns**
- You can combine multiple patterns using `|` (OR operator).
- **Example**:
  ```python
  def check_value(value):
      match value:
          case 1 | 2 | 3:
              print("Value is 1, 2, or 3")
          case _:
              print("Value is something else")

  check_value(2)  # Output: Value is 1, 2, or 3
  check_value(5)  # Output: Value is something else
  ```

---

## **11. Default Case**
- Use `_` as the default case to handle unmatched patterns.
- **Example**:
  ```python
  def describe_value(value):
      match value:
          case 1:
              print("One")
          case 2:
              print("Two")
          case _:
              print("Unknown value")

  describe_value(1)  # Output: One
  describe_value(3)  # Output: Unknown value
  ```

---

## **12. Matching with `as` Keyword**
- Use `as` to bind a matched pattern to a variable.
- **Example**:
  ```python
  def process_data(data):
      match data:
          case [1, 2, 3] as seq:
              print(f"Matched sequence: {seq}")
          case _:
              print("No match")

  process_data([1, 2, 3])  # Output: Matched sequence: [1, 2, 3]
  process_data([4, 5, 6])  # Output: No match
  ```

---

## **13. Matching with `*` (Star Patterns)**
- Use `*` to match the remaining elements in a sequence.
- **Example**:
  ```python
  def process_list(lst):
      match lst:
          case [1, 2, *rest]:
              print(f"Starts with 1 and 2, rest: {rest}")
          case _:
              print("No match")

  process_list([1, 2, 3, 4])  # Output: Starts with 1 and 2, rest: [3, 4]
  process_list([1, 3, 4])     # Output: No match
  ```

---

## **14. Matching with `**` (Double Star Patterns)**
- Use `**` to match remaining key-value pairs in a dictionary.
- **Example**:
  ```python
  def process_dict(d):
      match d:
          case {"name": name, **rest}:
              print(f"Name: {name}, Other details: {rest}")
          case _:
              print("No match")

  process_dict({"name": "Alice", "age": 25, "city": "New York"})
  # Output: Name: Alice, Other details: {'age': 25, 'city': 'New York'}
  ```

---

## **15. Practical Use Cases**
- **Handling API Responses**:
  ```python
  def handle_response(response):
      match response:
          case {"status": "success", "data": data}:
              print(f"Data: {data}")
          case {"status": "error", "message": msg}:
              print(f"Error: {msg}")
          case _:
              print("Unknown response format")
  ```

- **Parsing Commands**:
  ```python
  def parse_command(cmd):
      match cmd.split():
          case ["go", direction]:
              print(f"Moving {direction}")
          case ["attack", target]:
              print(f"Attacking {target}")
          case _:
              print("Unknown command")
  ```

---

## **16. Limitations**
- **No Fall-Through**: Unlike `switch-case` in other languages, `match` does not allow fall-through behavior.
- **No Direct Comparison**: Patterns are matched structurally, not by direct comparison (e.g., `==`).

---


<span style="display: flex; justify-content: space-between; width: 100%; align-items: center;">
    <a href="../11-module-11-nested-data-structures/README.md">
        <img src="https://img.shields.io/badge/Previous-Nested_Data_Structures-blue" width="250" height="35">
    </a>
    <a href="../13-module-13-functions/REAMDE.md">
        <img src="https://img.shields.io/badge/Next-Functions-brightgreen" width="160" height="35">
    </a>
</span>
<br><br>
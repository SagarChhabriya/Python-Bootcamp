![](/Python-Bootcamp/03-module-03-Data-Handling/assets/01-variable-reference.png)
  

In Python, variables don't directly store data. Instead, they store **references** to data in memory. Here’s a simplified explanation with examples, along with how you can check memory locations using the `id()` function.

### 1. **Reassigning a Variable (First Example)**

When you assign a new value to a variable, it points to a new memory location, leaving the old value behind.

```python
a = 10   # a points to the value 10
print(id(a))  # Prints the memory location of 10
a = 20   # a now points to the value 20
print(id(a))  # Prints the memory location of 20
```

**Memory:**
```
a --> 10   (initially)
a --> 20   (after reassignment)
```

- `a` originally points to `10`, but after reassignment (`a = 20`), it now points to `20`, and the reference to `10` is lost.
- The `id()` function shows the memory address of the variable's value.

---

### 2. **Multiple Variables Pointing to the Same Value (Second Example)**

When two variables are assigned the same value, they both point to the same memory location.

```python
a = 10   # a points to the value 10
b = 10   # b also points to the value 10
print(id(a))  # Prints the memory location of 10
print(id(b))  # Prints the memory location of 10
```

**Memory:**
```
a --> 10
b --> 10
```

- Both `a` and `b` point to the same value `10` in memory. Instead of creating two separate copies of `10`, both variables reference the same memory location.
- The `id()` function shows that `a` and `b` have the same memory address because they point to the same value.

---

### Key Points:
- In Python, variables hold **references** to data, not the data itself.
- When you reassign a variable, it points to a new value, and the old value is discarded (unless other references still exist).
- If two variables share the same value, they may point to the same memory location to save space (for immutable data types like integers).
- The `id()` function can be used to confirm whether two variables point to the same memory location. If `id(a) == id(b)`, both variables are referencing the same memory.


---
In Python's `datetime` module, there are a few methods that you can use to get the current date and time, and they differ in the time zone and the specific information they return:

### 1. **`datetime.now()`**
   - **Returns:** The current local date and time based on the system's time zone.
   - **Use case:** If you want the current date and time in the **local time zone** (the time zone your computer is set to).
   
   Example:
   ```python
   from datetime import datetime
   local_time = datetime.now()
   print(local_time)  # Output will be in local time (e.g., '2025-02-02 14:30:00')
   ```

   - **Note:** If you want the result to be timezone-aware (i.e., it includes the time zone information), you can pass an optional argument specifying the time zone using `pytz` or the `timezone` module.

### 2. **`datetime.today()`**
   - **Returns:** Essentially **the same** as `datetime.now()` but without the option to specify a time zone.
   - **Use case:** It’s a shorthand for `datetime.now()`. It also returns the **current local date and time**.
   
   Example:
   ```python
   from datetime import datetime
   local_time = datetime.today()
   print(local_time)  # Output will be in local time (e.g., '2025-02-02 14:30:00')
   ```

   - **Note:** The main difference between `datetime.today()` and `datetime.now()` is that `today()` is always tied to your **system's local time zone**, whereas `now()` can also take into account specific time zone information if passed.

### 3. **`datetime.utcnow()`**
   - **Returns:** The current **UTC (Coordinated Universal Time)** date and time, with no time zone offset (i.e., it’s always in the UTC time zone).
   - **Use case:** Use this method when you need the **current time in UTC**, regardless of your local time zone.
   
   Example:
   ```python
   from datetime import datetime
   utc_time = datetime.utcnow()
   print(utc_time)  # Output will be in UTC time (e.g., '2025-02-02 12:30:00')
   ```

   - **Note:** `utcnow()` will return a **naive datetime object** without any time zone information. If you want a timezone-aware object, you can use `datetime.now(timezone.utc)` or add time zone info manually using libraries like `pytz`.

### Key Differences:

| Method             | Time Zone             | Returns                                                   |
|--------------------|-----------------------|-----------------------------------------------------------|
| `datetime.now()`   | Local system time zone | Current local date and time (can also be timezone-aware)  |
| `datetime.today()` | Local system time zone | Same as `datetime.now()`, returns local date and time     |
| `datetime.utcnow()`| UTC (no offset)        | Current date and time in UTC (naive datetime object)      |

### Example of Time Zone Awareness:
If you want to work with time zones, you can make a `datetime` object timezone-aware like this:

```python
from datetime import datetime, timezone

# UTC time with timezone info
utc_time = datetime.now(timezone.utc)
print(utc_time)  # Output will be in UTC with time zone information
```

### Summary:
- Use `datetime.now()` or `datetime.today()` for the **local time**.
- Use `datetime.utcnow()` for **UTC time**.


--- 
### **UTC**:

- **UTC** (Coordinated Universal Time) is the global time standard used to regulate clocks worldwide.
- It is **not a time zone**, but a reference for time zones around the world.
- UTC is based on atomic time, adjusted with **leap seconds** to stay in sync with Earth's rotation.

### Key Points:
1. **Global Reference**: Same worldwide, used to determine local times based on time zone differences.
2. **Time Zone Differences**:
   - Example: New York = **UTC - 5 hours**, London = **UTC + 0**, Paris = **UTC + 1**.
3. **Leap Seconds**: Adjusted to ensure UTC stays within 0.9 seconds of **Universal Time (UT1)**.
4. **No DST**: UTC does not change for Daylight Saving Time, remaining constant year-round.
5. **In Computing**: Commonly used in timestamps for consistency across systems globally.

### Example:
- **2025-02-02 12:00 UTC** = **2025-02-02 07:00 EST** (New York) = **2025-02-02 13:00 CET** (Paris).

### Summary:
- UTC is a global time standard, used to synchronize time zones without DST adjustments.
- It ensures consistency in global communication, science, and technology.


### 1. **Prime Meridian**:
   - **Imagine a line** that goes all the way around the Earth, dividing it into two halves. This line is called the **Prime Meridian**, and it's like the starting point for measuring how far east or west you are on Earth.
   - It starts at **Greenwich, England**, and goes all the way from the North Pole to the South Pole.

### 2. **Time Standard**:
   - A **time standard** is like a rule for keeping time the same everywhere. It tells us what "time" it is at certain places. 
   - The **UTC (Coordinated Universal Time)** is the most common time standard. It's the "universal clock" everyone around the world can agree on, so no matter where you are, you can know what time it is compared to everyone else.

### 3. **Time Zone**:
   - A **time zone** is like a region on Earth where the people use the same time. Imagine the Earth is like a big pizza, and each "slice" has its own time.
   - For example, **New York** is in a time zone that is 5 hours behind **UTC**, while **Paris** is 1 hour ahead of **UTC**.

### 4. **Atomic Clocks**:
   - An **atomic clock** is a special kind of clock that uses tiny particles (atoms) to measure time very, **very** accurately. 
   - It's like having a super-precise timer that’s so good, it can tell the exact time down to a billionth of a second!

### Summary:
- **Prime Meridian** is the starting line on Earth for measuring time and locations.
- **Time Standard** is a global rule for telling time.
- **Time Zone** is a region that follows the same local time.
- **Atomic Clocks** are super-precise clocks that measure time by looking at tiny particles.


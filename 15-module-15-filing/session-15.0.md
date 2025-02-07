# 15. File Operations

File operations in Python allow you to read from and write to files, enabling data persistence and manipulation.

---

## **15.1 Introduction to File Operations**
- **Understanding Files**:
  - Files are used to store data permanently.
  - Python supports both **text files** (human-readable) and **binary files** (machine-readable).
- **Text vs. Bytes Files**:
  - **Text Files**: Store data as strings (e.g., `.txt`, `.csv`).
  - **Binary Files**: Store data in binary format (e.g., `.jpg`, `.exe`).

---

## **15.2 File Modes**
- **File Modes** determine how files are opened. They determine the allowed operations (read, write, append, etc.) and the file type (text or binary).

### **15.2.1 Writing Modes**
- `w`: Write mode (overwrites the file or creates a new file).
  ```python
  with open("example.txt", "w") as file:
      file.write("Hello, World!")
  ```
- `w+`: Write and read mode. Creates a new file (or truncates an existing file) and allows both writing and reading.
  ```python
  with open("example.txt", "w+") as file:
      file.write("Hello, World!")
      file.seek(0)  # Move cursor to the beginning
      print(file.read())  # Output: Hello, World!
  ```
- `wb`: Write binary mode.
  ```python
  with open("example.bin", "wb") as file:
      file.write(b"Hello, World!")
  ```
  
  ```python
  with open('image.jpg', 'wb') as file:
      file.write(b'\x89PNG\r\n\x1a\n')  # Writing binary data
  ```

### **15.2.2 Reading Modes**
- `r`: Read mode (default mode). Opens the file for reading. The file must exist.
  ```python
  with open("example.txt", "r") as file:
      print(file.read())  # Output: Hello, World!
  ```

### **15.2.3 Choosing the Appropriate Mode**
- Use **`w`** or **`w+`** when you want to write data to a new or existing file.
- Use **`r`** when you need to read data from a file.
- Use **`rb`** and **`wb`** for binary files (e.g., images or audio).
- Use **`a`** or **`a+`** when you want to append to an existing file.


---

## **15.3 Opening a File**
To interact with a file, use the built-in `open()` function:

- **Using `open()`**:
  - Opens a file and returns a file object.
  - **Syntax**:
    ```python
    file = open("filename", "mode")
    ```
  - **Example**:
    ```python
    file = open("example.txt", "r")
    content = file.read()
    file.close()
    ```

- **File Object**: The object returned by `open()` is a file handle, and it represents the file.
- **File Handle**: The variable that stores the reference to the file is called the **file handle**.

Instead of manually managing the file handle, it’s better to use the **`with`** statement (context manager) to automatically handle closing the file.

---

## **15.4 Reading Files**

- **Reading Entire File Content**:
    ```python
    with open("example.txt", "r") as file:
        content = file.read()
        print(content)
    ```
- **Reading Line by Line**:
  - `readline()`: Reads one line at a time.
   
    ```python
    with open("example.txt", "r") as file:
        line = file.readline()
        print(line)
    ```

  - `readlines()`: Reads all lines into a list.
   
    ```python
    with open("example.txt", "r") as file:
        lines = file.readlines()
        print(lines)
    ```
- **Iterating Over File Content**:

    ```python
    with open("example.txt", "r") as file:
        for line in file:
            print(line.strip())  # Remove newline character
    ```
  
    ```python
    with open('example.txt', 'r') as file:
        for line in file:
            print(line, end='')
    ```
---

## **15.5 Writing Files**
To write to a file, use the `write()` and `writelines()` methods.

- **Writing to a File**:
  - `write()`: Writes a string to the file.
    ```python
    with open("example.txt", "w") as file:
        file.write("Hello, World!")
    ```
  - `writelines()`: Writes a list of strings to the file.
    ```python
    lines = ["Line 1\n", "Line 2\n", "Line 3\n"]
    with open("example.txt", "w") as file:
        file.writelines(lines)
    ```
    ```python
    with open('example.txt', 'w') as file:
        file.writelines(["Hello, ", "World!"])
    ```

- **Writing in Binary Format**:
  ```python
  with open("example.bin", "wb") as file:
      file.write(b"Binary data")
  ```

---

## **15.6 File Methods**
Python provides several useful methods to interact with files:

- **Common File Methods**:
  - `seek(offset)`: Moves the file cursor to a specific position in the file.
    ```python
    with open("example.txt", "r") as file:
        file.seek(5)  # Move cursor to the 5th byte
        print(file.read())  # Output: , World!
    ```
  - `tell()`: Returns the current position of the file cursor.

    ```python
      with open('example.txt', 'r') as file:
          print(file.tell())  # Returns the current position
    ```
   
    ```python
    with open("example.txt", "r") as file:
        file.read(5)
        print(file.tell())  # Output: 5
    ```

- **Combining tell() and seek()**:
    ```python
    data = "All students are STUPIDS"
    f = open("abc.txt","w")
    f.write(data)
    with open("abc.txt","r+") as f:
      text = f.read()
      print(text)
      print("The current cursor position: ", f.tell()) # 24

      f.seek(17)
      print("The current cursor position: ", f.tell())

      f.write("GEMS!")
      f.seek(0)
      text = f.read()
      
      print("Data after modification:",text)
      
    ```

  - `flush()`: Flushes the internal buffer.
    
    ```python
    with open('example.txt', 'w') as file:
        file.write("Hello!")
        file.flush()  # Forces the buffer to be written
    ```  
  - `close()`: Closes the file.
    ```python
    file = open('example.txt', 'r')
    content = file.read()
    file.close()  # Always close the file when done
    ```


---

## **15.7 Using the `with` Keyword**
The `with` statement is a context manager that ensures files are automatically closed when you're done working with them. Even in case of exceptions also.

- **Context Manager**:
  - Automatically handles file closing, even if an exception occurs.
  - **Example**:
    ```python
    with open("example.txt", "r") as file:
        print(file.read())
    ```


## 15.8 Python Delete File

### Delete a File

To delete a file, you must import the `os` module, and run its `os.remove()` function:

### Example: Remove the file "demofile.txt"

```python
import os
os.remove("demofile.txt")
```

### Check if File Exists

To avoid getting an error, you might want to check if the file exists before you try to delete it:

### Example: Check if file exists, then delete it

```python
import os

if os.path.exists("demofile.txt"):
    os.remove("demofile.txt")
else:
    print("The file does not exist")
```

### Delete Folder

To delete an entire folder, use the `os.rmdir()` method:

### Example: Remove the folder "myfolder"

```python
import os
os.rmdir("myfolder")
```

> **Note**: You can only remove empty folders.

---
<!-- 
## **15.8 Working with Specific File Formats**

### **15.8.1 TXT Files**
Plain text files are the simplest file format. You can perform standard reading and writing operations on them.

- **Basic Operations**:
  ```python
  with open("example.txt", "r") as file:
      print(file.read())
  # No need to manually close the file
  ```

It automatically calls `file.close()` when the block is exited, even if an error occurs within the block.  

### **15.8.2 CSV Files**
CSV files store tabular data and are often used for data exchange.

- **Reading CSV Files**:
  ```python
  import csv
  with open("example.csv", "r") as file:
      reader = csv.reader(file)
      for row in reader:
          print(row)
  ```
- **Writing to CSV Files**:
  ```python
  import csv
  data = [["Name", "Age"], ["Alice", 25], ["Bob", 30]]
  with open("example.csv", "w", newline="") as file:
      writer = csv.writer(file)
      writer.writerows(data)
  ```
  ```python
  import csv
  with open('data.csv', 'w', newline='') as file:
      writer = csv.writer(file)
      writer.writerow(['Name', 'Age'])
      writer.writerow(['Alice', 30])
  ```


- **Using `DictReader` and `DictWriter`**:
  ```python
  import csv
  with open('data.csv', 'r') as file:
      reader = csv.DictReader(file)
      for row in reader:
          print(row)  # Access data by column names
  ```

  ```python
  import csv
  with open("example.csv", "r") as file:
      reader = csv.DictReader(file)
      for row in reader:
          print(row["Name"], row["Age"])
  ```

### **15.8.3 MS Excel Files**
To work with Excel files, use libraries like `openpyxl` or `pandas`.

- **Using `openpyxl`**:
  ```python
  from openpyxl import Workbook
  wb = Workbook()
  ws = wb.active
  ws["A1"] = "Hello"
  wb.save("example.xlsx")
  ```
- **Using `pandas`**:
  ```python
  import pandas as pd
  df = pd.read_excel("example.xlsx")
  print(df)
  ```

### **15.8.4 JSON Files**
JSON files store data in a structured, readable format.
- **Parsing JSON Files** with `json.load()`:
  ```python
  import json
  with open("example.json", "r") as file:
      data = json.load(file)
      print(data)
  ```
- **Writing JSON** with `json.dump()`:
  ```python
  import json
  data = {"name": "Alice", "age": 25}
  with open("example.json", "w") as file:
      json.dump(data, file)
  ```

### **15.8.5 XML Files**
XML files store data in a hierarchical structure.
- **Parsing XML Files** with `ElementTree`
  ```python
  import xml.etree.ElementTree as ET
  tree = ET.parse("example.xml")
  root = tree.getroot()
  for child in root:
      print(child.tag, child.attrib)
  ```
- **Creating XML Structures**:
  ```python
  import xml.etree.ElementTree as ET
  root = ET.Element("root")
  child = ET.SubElement(root, "child")
  child.text = "Hello"
  tree = ET.ElementTree(root)
  tree.write("example.xml")
  ```

---

## **15.9 Parsing and Node Creation**
Parsing refers to extracting specific data from files (e.g., reading an XML file or extracting data from a JSON). You can also create nodes or elements in these files using libraries like `xml.etree.ElementTree` for XML files or `json` for JSON files.

- **Extracting Data from Files**:
  - Use libraries like `csv`, `json`, or `xml.etree.ElementTree` to parse data.
- **Creating Nodes and Structuring Data**:
  - Use libraries like `ElementTree` for XML or `json` for JSON to create structured data.

---
- **XML Node Creation Example:**
  ```python
  import xml.etree.ElementTree as ET
  root = ET.Element('root')
  node = ET.SubElement(root, 'node', id="1")
  node.text = 'Hello, XML!'
  tree = ET.ElementTree(root)
  tree.write('new_file.xml')
  ```

This would create an XML structure with a new `<node>` element under the root.


---


## 15.10 Advanced File Handling Techniques

### **15.10.1 File Iterators**
- Instead of manually reading lines using `readline()` or `readlines()`, Python’s file object itself is an iterator. This allows for memory-efficient line-by-line reading using a `for` loop:
  ```python
  with open('example.txt', 'r') as file:
      for line in file:
          print(line, end='')
  ```
  This is efficient for large files since it reads one line at a time rather than loading the entire file into memory.

---

### **15.10.2 File Locking**
- In a multi-process or multi-threaded environment, you might need to ensure that a file is not being modified by two processes at once. Python does not have built-in file locking, but you can use external libraries like `fcntl` (Unix-based systems) or `portalocker` (cross-platform).
  Example using `portalocker`:
  ```python
  import portalocker
  
  with open('example.txt', 'r') as file:
      portalocker.lock(file, portalocker.LOCK_EX)  # Exclusive lock
      content = file.read()
      portalocker.unlock(file)
  ```

---

### **15.10.3 Working with Temporary Files**
- The `tempfile` module can be used for creating temporary files that are automatically deleted once they are closed or deleted.
  ```python
  import tempfile

  with tempfile.NamedTemporaryFile(delete=False) as temp_file:
      temp_file.write(b'This is temporary data.')
      print(temp_file.name)  # Displays the name of the temporary file
  ```

---

### **15.10.4 File Paths and `os` and `pathlib` Modules**
- Use the `os` and `pathlib` modules for manipulating file paths in a platform-independent way. 
  - **`os.path`**: Legacy module for path manipulation.
  - **`pathlib`**: A more modern, object-oriented approach to path manipulation.
  
  Example with `pathlib`:
  ```python
  from pathlib import Path

  file_path = Path('example.txt')
  if file_path.exists():
      print(f"File {file_path} exists.")
  ```

  Example with `os.path`:
  ```python
  import os

  file_path = 'example.txt'
  if os.path.exists(file_path):
      print(f"File {file_path} exists.")
  ```

---

### **15.10.5 Handling Large Files Efficiently**
- When working with very large files (e.g., GBs of data), reading and writing in chunks is crucial. This can be done by specifying a chunk size when reading:
  ```python
  with open('large_file.txt', 'r') as file:
      while chunk := file.read(1024):  # Read 1 KB at a time
          process(chunk)  # Replace this with your processing function
  ```

- **Buffered I/O**: If you need more control over how data is read from disk, consider using buffered I/O for large files:
  ```python
  with open('large_file.txt', 'rb') as file:
      buffer = file.read(4096)  # Read in chunks of 4KB
      while buffer:
          process(buffer)
          buffer = file.read(4096)
  ```

---

### **15.10.6 Handling File Encoding**
- Text files may have different encodings. By default, Python opens files with the system’s default encoding (usually `UTF-8`), but you can specify an encoding using the `encoding` argument in the `open()` function:
  ```python
  with open('example.txt', 'r', encoding='utf-8') as file:
      content = file.read()
  ```

- If you're dealing with non-UTF encodings (e.g., `ISO-8859-1`, `latin1`, `cp1252`), specify the correct encoding.

---

### **15.10.7 File Compression**
- Python supports reading and writing compressed files like `.gz`, `.zip`, `.tar` using modules like `gzip`, `zipfile`, or `tarfile`.
  
  - **Using `gzip` for reading a compressed file**:
    ```python
    import gzip
    with gzip.open('example.txt.gz', 'rt', encoding='utf-8') as file:
        content = file.read()
    ```
  
  - **Writing compressed files**:
    ```python
    import gzip
    with gzip.open('example.txt.gz', 'wt', encoding='utf-8') as file:
        file.write("This is compressed text.")
    ```

  - **Using `zipfile` for creating a ZIP file**:
    ```python
    import zipfile
    with zipfile.ZipFile('example.zip', 'w') as zipf:
        zipf.write('example.txt', arcname='file_in_zip.txt')
    ```

---

### **15.10.8 File Permissions**
- File permissions are important, especially in multi-user environments. You can change file permissions using the `os.chmod()` function.
  Example to make a file read-only:
  ```python
  import os
  os.chmod('example.txt', 0o444)  # Read-only permissions
  ```

  - **Common permission modes**:
    - `0o777` - Read, write, execute for everyone.
    - `0o644` - Read/write for owner, read-only for others.

---

### **15.10.9 Error Handling with Files**
- Always use error handling when performing file operations to ensure the program doesn't crash when something goes wrong (e.g., file not found, permission issues).
  Example with `try-except`:
  ```python
  try:
      with open('non_existent_file.txt', 'r') as file:
          content = file.read()
  except FileNotFoundError:
      print("File not found.")
  except IOError as e:
      print(f"An I/O error occurred: {e}")
  ```

---

## **15.10.10 File Watching (Advanced)**
- In some applications, you may need to track changes to files in real-time (e.g., a log file or configuration file). This can be done using libraries like `watchdog`:
  ```bash
  pip install watchdog
  ```
  Example:
  ```python
  from watchdog.observers import Observer
  from watchdog.events import FileSystemEventHandler
  import time

  class MyHandler(FileSystemEventHandler):
      def on_modified(self, event):
          print(f'File {event.src_path} was modified')

  observer = Observer()
  observer.schedule(MyHandler(), path='.', recursive=False)
  observer.start()

  try:
      while True:
          time.sleep(1)
  except KeyboardInterrupt:
      observer.stop()
  observer.join()
  ```

---

### **15.10.11 File Integrity Check (Checksums and Hashing)**
- When working with critical files or when transferring files, it’s a good idea to compute a hash (checksum) of the file to verify its integrity. You can use libraries like `hashlib` to compute the hash of a file:
  ```python
  import hashlib

  def get_file_hash(file_path):
      hash_md5 = hashlib.md5()
      with open(file_path, 'rb') as file:
          for chunk in iter(lambda: file.read(4096), b""):
              hash_md5.update(chunk)
      return hash_md5.hexdigest()

  print(get_file_hash('example.txt'))
  ```



## **15.10.12 File Existence and Permissions**
- **Checking if a File Exists**:
  ```python
  import os
  if os.path.exists("example.txt"):
      print("File exists")
  ```
- **Checking File Permissions**:
  ```python
  import os
  if os.access("example.txt", os.R_OK):
      print("File is readable")
  ```

### **15.10.13 File Metadata**
- **Getting File Size**:
  ```python
  import os
  size = os.path.getsize("example.txt")
  print(f"File size: {size} bytes")
  ```
- **Getting File Modification Time**:
  ```python
  import os
  mtime = os.path.getmtime("example.txt")
  print(f"Last modified: {mtime}")
  ```

### **15.10.14 File and Directory Operations**
- **Renaming Files**:
  ```python
  import os
  os.rename("old_name.txt", "new_name.txt")
  ```
- **Deleting Files**:
  ```python
  import os
  os.remove("example.txt")
  ```
- **Creating Directories**:
  ```python
  import os
  os.mkdir("new_directory")
  ```
- **Listing Directory Contents**:
  ```python
  import os
  contents = os.listdir(".")
  print(contents)
  ```

---

## **15.11 Best Practices for File Handling**
- **Always Use `with`**:
  - Ensures files are properly closed, even if an error occurs.
- **Handle Exceptions**:
  - Use `try-except` blocks to handle file-related errors.
  ```python
  try:
      with open("example.txt", "r") as file:
          print(file.read())
  except FileNotFoundError:
      print("File not found")
  except IOError:
      print("An error occurred while reading the file")
  ```
- **Use Absolute Paths**:
  - Avoid issues with relative paths by using absolute paths.
  ```python
  import os
  file_path = os.path.abspath("example.txt")
  with open(file_path, "r") as file:
      print(file.read())
  ```

---
 -->

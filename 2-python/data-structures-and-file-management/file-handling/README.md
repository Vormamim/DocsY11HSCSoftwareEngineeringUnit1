---
icon: book-open
---

# File Handling

Python provides built-in functions to **read from** and **write to** text files.

### **Reading from a File**

| Function                                  | Description                                                                          |
| ----------------------------------------- | ------------------------------------------------------------------------------------ |
| `open("filename.txt", "r")`               | Opens a file in **read** mode.                                                       |
| `file.read()`                             | Reads the entire file as a **single string**.                                        |
| `file.readline()`                         | Reads **one line** at a time.                                                        |
| `file.readlines()`                        | Reads **all lines** and stores them in a **list**.                                   |
| `with open("filename.txt", "r") as file:` | Best practice for handling files (auto-closes file).                                 |
| `.strip()`                                | Removes **leading** and **trailing** whitespace or newline characters from a string. |

#### **Example:**

```python
with open("students.txt", "r") as file:
    content = file.read()
print(content)  # Prints entire file as a string
```

***

### **Writing to a File**

| Function                           | Description                                                     |
| ---------------------------------- | --------------------------------------------------------------- |
| `open("filename.txt", "w")`        | Opens a file in **write** mode (erases existing content).       |
| `open("filename.txt", "a")`        | Opens a file in **append** mode (adds content without erasing). |
| `file.write(text)`                 | Writes a **string** to the file.                                |
| `file.writelines(list_of_strings)` | Writes **multiple lines** from a list.                          |

#### **Example:**

```python
with open("students.txt", "w") as file:
    file.write("Alice\nBob\nCharlie\n")  # Writes names to file
```

***

### **Closing a File**

| Function       | Description                                             |
| -------------- | ------------------------------------------------------- |
| `file.close()` | Closes the file (not needed if using `with open(...)`). |

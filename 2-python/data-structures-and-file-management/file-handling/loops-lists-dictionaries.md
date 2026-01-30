---
icon: book-open
---

# Loops, Lists, Dictionaries

The following examples show you how to manipulate files further using **for loops, list comprehension** and **dictionaries.**

## **For Loops**

For loops help iterate over data in **lists** and **files**.

| Syntax                               | Description                                                 |
| ------------------------------------ | ----------------------------------------------------------- |
| `for item in sequence:`              | Loops through **items** in a sequence (list, string, etc.). |
| `for i in range(start, stop, step):` | Loops a specific number of times, **from start to stop**.   |

#### **Example:**

```python
# Loop through a list
names = ["Alice", "Bob", "Charlie"]
for name in names:
    print(name)  # Prints each name in the list
```

***

## **List Comprehension**

List comprehensions allow you to create new lists from existing ones, often in a **single line**.

| Syntax                                           | Description                                                             |
| ------------------------------------------------ | ----------------------------------------------------------------------- |
| `[expression for item in iterable]`              | Creates a list with an expression applied to each item in the iterable. |
| `[expression for item in iterable if condition]` | Creates a list with a conditional check.                                |

#### **Examples:**

```python
# List comprehension to create a new list with items in uppercase
names = ["Alice", "Bob", "Charlie"]
uppercase_names = [name.upper() for name in names]  
print(uppercase_names)  # ['ALICE', 'BOB', 'CHARLIE']

# List comprehension with condition (only names longer than 3 characters)
long_names = [name for name in names if len(name) > 3]
print(long_names)  # ['Alice', 'Charlie']
```

***

## **Dictionaries**

Dictionaries store data as **key-value pairs**. Useful for mapping relationships, like student names to ages.

| Syntax                                | Description                                             |
| ------------------------------------- | ------------------------------------------------------- |
| `dict = {key1: value1, key2: value2}` | Creates a dictionary with **key-value pairs**.          |
| `dict[key]`                           | Accesses the **value** associated with a **key**.       |
| `dict[key] = value`                   | Adds or updates a **key-value** pair in the dictionary. |
| `.items()`                            | Returns the dictionary as **key-value pairs**.          |
| `.keys()`                             | Returns the **keys** from the dictionary.               |
| `.values()`                           | Returns the **values** from the dictionary.             |

#### **Example:**

```python
# Creating a dictionary of students
student_dict = {"Alice": 15, "Bob": 14, "Charlie": 16}
print(student_dict["Alice"])  # Prints 15 (Alice's age)
```

### **Iterating Over Dictionaries**

To loop through a dictionary, you can use `for` loops with `.items()`, `.keys()`, or `.values()`.

#### **Example:**

```python
# Iterate through key-value pairs
for name, age in student_dict.items():
    print(f"{name} is {age} years old")
```

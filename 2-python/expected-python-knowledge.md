---
icon: book-open
---

# Expected Python Knowledge

From the course specifications, you are expected to be understand the following skills in Python by the end of your HSC. They have been broken down further for clarity, so make sure you have a read of the following and use your time wisely at the beginning of the course to get your head around some of this!

## Programming Fundamentals

### Control Structures

* **Conditional Statements**: Understand how to use `if`, `elif`, and `else` statements to control the flow of a program.
* **Loops**: Master the use of `for` loops and `while` loops for repeating tasks.
* **Loop Control Statements**: Learn about `break`, `continue`, and `pass` to manage the behavior of loops.
* **Comprehensions**: Use **list** comprehensions and **dictionary** comprehensions for creating new sequences.
* **Error Handling**: Implement `try` and `except` to manage exceptions.

### Variables

* **Global Variables**: Variables defined outside of a function and accessible from anywhere in the code. Understand their scope and usage.
* **Local Variables**: Variables defined within a function or block, accessible only within that function. Comprehend their scope and limitations.
* **The `global` Keyword**: Learn how to declare a variable as global within a function to modify it outside of the function's local scope.

### Simple and Structured Data Types

#### **Simple Data Types**

* **Integers (`int`)** – Whole numbers (e.g., `10`, `-5`, `42`)
* **Floating-point numbers (`float`)** – Decimal numbers (e.g., `3.14`, `-0.5`, `2.0`)
* **Booleans (`bool`)** – `True` or `False`
* **Strings (`str`)** – Text data enclosed in quotes (e.g., `"Hello"`, `'Python'`)

#### **Structured Data Types**

* **Lists (`list`)** – Ordered, mutable collection (e.g., `[1, 2, 3]`, `["apple", "banana"]`)
* **Tuples (`tuple`)** – Ordered, immutable collection (e.g., `(1, 2, 3)`, `("red", "blue")`)
* **Dictionaries (`dict`)** – Key-value pairs (e.g., `{"name": "Alice", "age": 25}`)
* **Sets (`set`)** – Unordered, unique elements (e.g., `{1, 2, 3}`)

### Functions

* **Defining a function** – Use `def` keyword (`def function_name():`).
* **Calling a function** – Use the function name followed by `()`.
* **Parameters** – Pass values into a function (`def greet(name):`).
* **Return statement** – Send a value back using `return`.
* **Default parameters** – Provide a default value (`def greet(name="Guest")`).

### Modules and Libraries

* **Modules** – Files containing Python code (`.py`) that can be imported.
* **Importing Modules** – Use `import module_name`.
* **Using `from` Import** – Import specific functions or classes (`from module import function`).
* **Built-in Modules** – Pre-installed modules like `math`, `random`, `datetime`.
* **Third-Party Libraries** – Installed using `pip` (e.g., `numpy`, `pandas`).
* **Creating a Module** – Write functions in a `.py` file and import them.
* **Packages** – Collections of modules organised in directories with `__init__.py`.

### File Handling

* **Opening a File** – Use `open("filename", "mode")`.
* **Modes** – `'r'` (read), `'w'` (write), `'a'` (append), `'x'` (create).
* **Reading a File** – Use `.read()`, `.readline()`, or `.readlines()`.
* **Writing to a File** – Use `.write("text")`.
* **Appending to a File** – Use mode `'a'` to add content without deleting existing data.
* **Closing a File** – Always use `.close()` or `with open() as f:` for automatic closing.
* **Handling Exceptions** – Use `try-except` to catch file errors.

***

## Object-Oriented Programming

### Classes, Objects, Attributes and Methods

* **Classes** – Blueprints for creating objects (`class ClassName:`).
* **Objects** – Instances of a class (`obj = ClassName()`).
* **Attributes** – Variables stored in an object (`self.attribute = value`).
* **Methods** – Functions inside a class (`def method(self):`).
* **`__init__` Method** – Constructor for initialising attributes.
* **`self` Keyword** – Refers to the instance of the class.
* **Creating & Using Objects** – Instantiate and access attributes/methods.
* **Inheritance** – A class can inherit attributes and methods from another class (`class Child(Parent):`).
* **Polymorphism** – Different classes can have methods with the same name but different behavior.
* **Encapsulation** – Restrict direct access to data using private/protected attributes (`_protected`, `__private`).




























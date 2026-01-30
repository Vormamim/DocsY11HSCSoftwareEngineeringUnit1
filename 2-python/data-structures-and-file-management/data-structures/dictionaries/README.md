---
icon: book-open
---

# Dictionaries

A **dictionary** in Python is a data structure that stores an **unordered collection of items**.

Unlike lists or tuples, which are indexed by a range of numbers, dictionaries are organised by **key-value pairs**.

Each key in a dictionary is mapped to a specific value, allowing you to associate related data in a way that makes it easy to look up values based on their corresponding keys.

One of the key characteristics of dictionaries is that the **keys must be unique and immutable**, meaning that each key can only appear once in a dictionary, and it must be a type that does not change, such as a string, number, or tuple. The values, however, can be of any type and can even be duplicated.

To create a dictionary, place **comma-separated key-value pairs** inside curly braces `{}`, with a colon `:` separating each key from its associated value.

```python
student_grades = {'Alice': 85, 'Bob': 92, 'Charlie': 78} 
```

Alternatively, you can create an empty dictionary using empty curly braces `{}` and then add key-value pairs to it as needed.

***

## Mutability

Dictionaries in Python are **mutable**, which means you can change, add, or remove key-value pairs after the dictionary has been created. This mutability makes dictionaries an excellent choice for situations where the data may need to be updated or expanded over time.

***

## Key Features

1. Dictionaries are particularly useful when you need to **associate pairs of items**.
2. One of the standout features of dictionaries is their ability to provide **fast access to data**. By using a key, you can quickly retrieve the corresponding value without needing to search through all the items, as you would with a list.

***

## Dictionary Methods

**`get()`**: returns the value associated with a specified key. If the key is not found, it returns a default value (which you can specify) instead of raising a `KeyError`.

```python
student_grades = {'Alice': 85, 'Bob': 92}
grade = student_grades.get('Alice')  # Output: 85
missing_grade = student_grades.get('Charlie', 'Not Found')  # Output: 'Not Found'
```

**`keys()`**: returns a view object that contains a list of all the keys in the dictionary.

```python
student_grades = {'Alice': 85, 'Bob': 92}
all_keys = student_grades.keys()  # Output: dict_keys(['Alice', 'Bob'])
```

**`values()`**: returns a view object that contains a list of all the values in the dictionary.

```python
student_grades = {'Alice': 85, 'Bob': 92}
all_values = student_grades.values()  # Output: dict_values([85, 92])
```

**`items()`**: returns a view object that contains a list of all the key-value pairs in the dictionary as tuples.

```python
student_grades = {'Alice': 85, 'Bob': 92}
all_items = student_grades.items()  # Output: dict_items([('Alice', 85), ('Bob', 92)])
```

**`update()`**: updates the dictionary with the key-value pairs from another dictionary or an iterable of key-value pairs. If a key already exists, its value is updated; if the key doesn't exist, it is added.

```python
student_grades = {'Alice': 85, 'Bob': 92}
new_grades = {'Charlie': 78, 'Bob': 95}
student_grades.update(new_grades)
# Output: {'Alice': 85, 'Bob': 95, 'Charlie': 78}
```

**`pop()`**: removes the key-value pair associated with a specified key and returns the value. If the key is not found, it raises a `KeyError` unless you provide a default value.

```python
student_grades = {'Alice': 85, 'Bob': 92}
removed_value = student_grades.pop('Bob')  # Output: 92
# student_grades is now {'Alice': 85}
```

**`popitem()`**: removes and returns the last key-value pair inserted into the dictionary. Dictionaries maintain insertion order, so `popitem()` will return items in LIFO (last-in, first-out) order.

```python
student_grades = {'Alice': 85, 'Bob': 92}
last_item = student_grades.popitem()  # Output: ('Bob', 92)
# student_grades is now {'Alice': 85}
```

**`clear()`**: removes all key-value pairs from the dictionary, leaving it empty.

```python
student_grades = {'Alice': 85, 'Bob': 92}
student_grades.clear()
# student_grades is now {}
```

**`setdefault()`**: returns the value of a specified key. If the key does not exist, it inserts the key with the specified default value and returns that default value.

```python
student_grades = {'Alice': 85, 'Bob': 92}
grade = student_grades.setdefault('Charlie', 78)  # Adds 'Charlie' with value 78
# student_grades is now {'Alice': 85, 'Bob': 92, 'Charlie': 78}
```

**`copy()`**: returns a shallow copy of the dictionary. This means that the new dictionary is a copy of the original, but if the dictionary contains nested objects, they are not copied.

```python
student_grades = {'Alice': 85, 'Bob': 92}
grades_copy = student_grades.copy()
```

**`fromkeys()`**: creates a new dictionary with specified keys, all set to a specified default value.

```python
keys = ['Alice', 'Bob', 'Charlie']
default_value = 0
new_dict = dict.fromkeys(keys, default_value)
# Output: {'Alice': 0, 'Bob': 0, 'Charlie': 0}
```

#### Looping through a Dictionary

```python
for key, value in student.items():
    print(f"{key}: {value}")
```


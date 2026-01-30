---
icon: book-open
---

# Tuples

So we've looked at lists and dictionaries - but what about tuples and sets?&#x20;

A **tuple** in Python is a fundamental data structure that shares similarities with lists. Like lists, tuples are **ordered collections** of items, meaning the elements within a tuple are stored in a specific sequence, and each element can be accessed using an index.

However, what sets tuples apart is their **immutability**. This characteristic means that once a tuple is created, the elements within it cannot be altered, added to, or removed. This immutability can be advantageous in situations where you want to ensure that a collection of items remains constant throughout the execution of a program.

Another common use of tuples is in functions that need to return multiple values. Since tuples can group multiple values into a single return statement, they provide a convenient way to return multiple pieces of data at once without risking unintended modifications to those values later in the program.

Creating a tuple in Python is straightforward. You simply place the values you want to include in the tuple, separated by commas, within parentheses.

```python
# A tuple containing the integers 1, 2, and 3 in that specific order.
my_tuple = (1, 2, 3) 
```

If you need a tuple with a single item, a comma must follow the item inside the parentheses (e.g. **`single_item_tuple = (5,)`**). Without the comma, Python would interpret the expression as a simple integer within parentheses rather than a tuple.

***

## Immutability

The immutability of tuples is a defining characteristic that distinguishes them from other data structures like lists.

Once a tuple is created, its content is fixed; you cannot change, add, or remove items.

This makes tuples an excellent choice for data that should remain constant, ensuring that the integrity of the data is maintained throughout the execution of a program. For example, if you have a collection of values that represent fixed settings or configurations, storing them in a tuple guarantees that these values will not be altered inadvertently.

***

## Key Features

1. Tuples support **indexing**, meaning you can access specific elements within a tuple by their position, just like with lists.
2. Tuples also support **slicing**, which allows you to extract a subset of elements from a tuple. For example, **`my_tuple[1:3]`** would return a new tuple containing the second and third elements.



## Examples

### Basic Operations

| Coordinate | Value |
| ---------- | ----- |
| X          | 3     |
| Y          | 5     |

***

```python
# 1. Create a tuple to represent the coordinates of a point.
# Tuples are created using parentheses '()'.

coordinates = (3, 5)

# 2. Access the X and Y values from the tuple using indexing.
# Tuples support indexing just like lists.
x = coordinates[0]
y = coordinates[1]

# 3. Try changing a value in the tuple (This will raise an error since tuples are immutable).
# coordinates[0] = 4  # Uncommenting this line will result in an error.

# 4. Create a new tuple by concatenating two tuples.
# Concatenation of tuples can be done using the '+' operator.
new_coordinates = coordinates + (7, 9)
print(new_coordinates)  # Output: (3, 5, 7, 9)
```

***

### Multiple Data Types

| Field   | Value        |
| ------- | ------------ |
| Name    | Alice        |
| Age     | 25           |
| Address | 1234 Elm St. |

```python
# 1. Create a tuple to store a user's profile information.
# A tuple can contain mixed data types such as strings, integers, etc.

user_profile = ("Alice", 25, "1234 Elm St.")

# 2. Access each element in the tuple using indexing.
# Print each part of the user's profile.
name = user_profile[0]
age = user_profile[1]
address = user_profile[2]

print("Name:", name)
print("Age:", age)
print("Address:", address)

# 3. Try to change a value in the tuple (This will raise an error since tuples are immutable).
# user_profile[1] = 26  # Uncommenting this line will result in an error.

# 4. Create a new tuple by concatenating the user's profile with additional information (e.g., phone number).
new_profile = user_profile + ("555-1234",)
print(new_profile)  # Output: ('Alice', 25, '1234 Elm St.', '555-1234')
```


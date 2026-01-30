---
icon: book-open
---

# Lists

In Python, a list is an ordered collection of items, where each item can be of any data type, including integers, strings, or even other lists. This structure allows you to store multiple related values in one place, making it a fundamental tool in programming.

Lists are especially useful when dealing with a collection of items where the order is important, and this order might need to change over time.

Additionally, lists are ideal for situations where duplicate values are expected and need to be stored.

Python lists support a variety of operations such as indexing, which allows you to access specific elements by their position in the list, and slicing, which lets you retrieve a portion of the list.

To create a list, simply place a series of comma-separated values inside square brackets `[]`. In Python, when you include letters or characters in a list, they need to be enclosed in either single ' ' or double " " quotation marks.

```python
# Creates a list containing two integers and two characters.
my_list = [1, 2, 'a', 'b'] 
```

In a Python list, each individual item within the list is referred to as an element. These elements can be of any data type, including numbers, strings, or even other lists, and they are stored in a specific order.

To access or modify an element, you use its position within the list, which is known as its index. The index is a numerical value that uniquely identifies the position of each element in the list. Importantly, Python lists are zero-indexed, meaning that the indexing begins at 0. This means the first element in the list has an index of 0, the second element has an index of 1, and so on.

***

## Mutability

Lists in Python are mutable, which means that you can modify the content of a list after it has been created, unlike some other data structures where changes would require the creation of a new instance.

Lists come with built-in methods like **`append()`**, which adds an item to the end of the list, **`remove()`**, which deletes a specific item, **`pop()`**, which removes and returns the last item, and **`extend()`**, which adds multiple items from another list.

The mutability of lists is a key feature that distinguishes them from other collections like tuples. You can easily add, change, or remove items after the list has been created. This flexibility makes lists one of the most powerful and commonly used data structures in Python.

```python
# Creating a list
my_list = [1, 2, 3, 4]

# Modifying the list
my_list.append(5)        # Adds 5 to the end of the list
my_list[0] = 10          # Changes the first item to 10
my_list.remove(3)        # Removes the item with value 3

# Printing the list
print(my_list)
```

***

## List Methods

**append()**: Adds an element to the end of the list.

```python
my_list = [1, 2, 3]
my_list.append(4)
print(my_list)  # Output: [1, 2, 3, 4]
```

**remove()**: Removes the first occurrence of a specified element from the list.

```python
my_list = [1, 2, 3, 2]
my_list.remove(2)
print(my_list)  # Output: [1, 3, 2]
```

**pop()**: Removes and returns the element at the specified index (or the last element if no index is provided).

```python
my_list = [1, 2, 3]
popped_item = my_list.pop()
print(popped_item)  # Output: 3
print(my_list)      # Output: [1, 2]
```

**extend()**: Adds all the elements from another list (or any iterable) to the end of the current list.

```python
my_list = [1, 2, 3]
my_list.extend([4, 5])
print(my_list)  # Output: [1, 2, 3, 4, 5]
```

**index()**: Returns the index of the first occurrence of a specified element in the list.

```python
my_list = [1, 2, 3, 2]
index = my_list.index(2)
print(index)  # Output: 1
```

**insert()**: Inserts an element at a specified position in the list.

```python
my_list = [1, 2, 4]
my_list.insert(2, 3)
print(my_list)  # Output: [1, 2, 3, 4]
```

**sort()**: Sorts the elements of the list in ascending order by default.

```python
my_list = [3, 1, 2]
my_list.sort()
print(my_list)  # Output: [1, 2, 3]
```

**reverse()**: Reverses the order of the elements in the list.

```python
my_list = [1, 2, 3]
my_list.reverse()
print(my_list)  # Output: [3, 2, 1]
```

**count()**: Returns the number of times a specified element appears in the list.

```python
my_list = [1, 2, 2, 3]
count = my_list.count(2)
print(count)  # Output: 2
```

**clear()**: Removes all elements from the list.

```python
my_list = [1, 2, 3]
my_list.clear()
print(my_list)  # Output: []
```

**`max()`**: Finds the maximum value in a given iterable, such as a list, tuple, or set.

```python
numbers = (5, 12, 8, 3, 15)
highest = max(numbers)
print(highest)  # Output: 15
```

**`min()`**: Finds the minimum value in a given iterable, such as a list, tuple, or set.

```python
numbers = (5, 12, 8, 3, 15)
lowest = min(numbers)
print(lowest)  # Output: 3
```


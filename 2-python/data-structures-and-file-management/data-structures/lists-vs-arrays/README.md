---
icon: book-open
---

# Lists vs Arrays

Now the focus on arrays in the syllabus may cause a bit of confusion, as Python tends to use lists instead.

The following breaks down the differences between lists and arrays in Python.

| Feature             | Lists                                  | Arrays (array module or NumPy)                                   |
| ------------------- | -------------------------------------- | ---------------------------------------------------------------- |
| **Data Type**       | Can store mixed data types             | Typically stores a single data type                              |
| **Flexibility**     | Can hold numbers, strings, other lists | Requires all elements to be of the same type                     |
| **Performance**     | Slower for numerical operations        | Faster for numerical operations                                  |
| **Memory Usage**    | Uses more memory                       | More memory-efficient for large data sets                        |
| **Indexing**        | Supports indexing and slicing          | Supports indexing and slicing (NumPy has more advanced indexing) |
| **Operations**      | General-purpose operations             | Supports mathematical and vectorised operations (NumPy)          |
| **Library Needed?** | No (built-in)                          | Yes (`array` module or `numpy`)                                  |

### **Example of a List**

```python
my_list = [1, "apple", 3.14, [5, 6]]  # Stores different types of data
print(my_list[1])  # Output: apple
```

### **Example of an Array (`array` module)**

```python
import array
my_array = array.array('i', [1, 2, 3, 4])  # Only stores integers
print(my_array[1])  # Output: 2
```

## **When to Use Each?**

Use **lists** when working with different types of data.

Use **arrays** when working with large numerical datasets for better performance.

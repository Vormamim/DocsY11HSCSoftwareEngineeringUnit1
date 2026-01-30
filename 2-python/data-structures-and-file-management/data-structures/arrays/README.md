---
icon: book-open
---

# Arrays

In Python, an **array** is a data structure that stores a collection of elements, where each element is of the same data type. Unlike lists, which can hold mixed data types, arrays are designed to be more memory-efficient and optimised for numerical operations.

Arrays are particularly useful when working with large datasets that involve mathematical computations, as they allow for faster processing compared to lists. This efficiency comes from how arrays store data in contiguous memory locations, making operations like addition, multiplication, and other calculations significantly faster.

Python does not have a built-in array type like some other languages, but you can create arrays using the `array` module or libraries like NumPy, which is commonly used for scientific computing.

To create an array using Python’s built-in `array` module, you first need to import it. Then, you specify a type code (which defines the data type) and provide the initial elements inside parentheses.

```python
# Creates an array of integers
import array
my_array = array.array('i', [1, 2, 3, 4])
```

In the above example, `'i'` is the type code that indicates the array will store integers. Unlike lists, all elements in this array must be integers, and adding a different data type would result in an error.

For more advanced numerical operations, the **NumPy** library is widely used. NumPy arrays (called `ndarray`) provide powerful tools for handling large datasets efficiently.

```python
# Creates a NumPy array with four integers
import numpy as np
my_numpy_array = np.array([1, 2, 3, 4])
```

NumPy arrays support vectorised operations, meaning you can apply mathematical functions to all elements at once without using loops, making them much faster than lists for numerical tasks.

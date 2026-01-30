---
icon: clipboard-list-check
---

# Activities

{% hint style="warning" %}
## Appending an Array

Check this link:

[https://www.tutorialspoint.com/numpy/numpy\_append.htm](https://www.tutorialspoint.com/numpy/numpy_append.htm)
{% endhint %}

Create a Folder and open in VS code. Create and complete the following programs:

<details>

<summary>1 - Basic_List_Operations.py</summary>

```python
# 1. Create a list named 'students' with at least 4 student names.
students = ['Alice', 'Bob', 'Charlie', 'Diana']

# 2. Print the first and last student's name using indexing.
# Remember that the first item has an index of 0.

# 3. Add a new student to the end of the list.
# Use append() to add a new name to the list.

# 4. Remove the second student from the list.
# Use pop()to delete an element by index.

# 5. Print the updated list.

```



</details>

<details>

<summary>2 - Array_Module.py</summary>

```python
import array  # Import the array module

# 1. Create an array named 'scores' that stores five test scores (integers).
scores = array.array('i', [85, 90, 88, 92, 87])

# 2. Print the third score in the array.
# Arrays use indexing just like lists.

# 3. Change the second score to a new value.
# Modify an element by accessing it through its index.

# 4. Add a new score to the array.
# Use append() to add a new element.

# 5. Print the updated array.
# Should show: array('i', [85, 95, 88, 92, 87, 93])

```



</details>

<details>

<summary>3 - Nested_List_or_Matrix.py</summary>

```python
# 1. Create a nested list named 'grades' where each inner list represents a student.
#    Each student should have grades for Math, Science, and English.
grades = [
    [85, 90, 88],  # Student 1's grades: Math, Science, English
    [78, 82, 85],  # Student 2's grades: Math, Science, English
    [92, 89, 91]   # Student 3's grades: Math, Science, English
]

# 2. Print the grades of the second student.
# Access the second student (index 1), then print their grades.

# 3. Change the Math grade of the first student.
# Modify the first grade in the first student's list.

# 4. Add a new student with grades.
# Add a new list to the 'grades' list to represent a new student's grades.

# 5. Print the updated list.

```



</details>

<details>

<summary>4 - Multidimensional_Arrays.py</summary>

```python
import numpy as np  # Import NumPy library

# 1. Create a 2D NumPy array named 'matrix' with 3 rows and 3 columns of numbers.
matrix = np.array([
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
])

# 2. Print the entire second row.
# The second row is at index 1 (remember, indexing starts at 0).
# Output will be [4, 5, 6]

# 3. Change the value in the first row, second column.
# The first row is at index 0, second column is at index 1.


# 4. Add a new row to the matrix.
# Use np.append to add a row to the existing matrix.
# use this code: new_row = np.array([10, 11, 12])
# use this code: matrix = np.append(matrix, [new_row], axis=0)

# 5. Print the updated matrix.

```



</details>

<details>

<summary>5 - sales_array.py</summary>

Use arrays to store and manipulate the following monthly sales revenue (dollars) for a company over two years.

| **Year** | **January** | **February** | **March** | **April** | **May** | **June** | **July** | **August** | **September** | **October** | **November** | **December** |
| -------- | ----------- | ------------ | --------- | --------- | ------- | -------- | -------- | ---------- | ------------- | ----------- | ------------ | ------------ |
| 2015     | 1000        | 1100         | 1200      | 1300      | 1400    | 1500     | 1600     | 1700       | 1800          | 1900        | 2000         | 2100         |
| 2016     | 1050        | 1150         | 1250      | 1350      | 1450    | 1550     | 1650     | 1750       | 1850          | 1950        | 2050         | 2150         |

```python
import numpy as np  # Import NumPy library

# 1. Create a 2D NumPy array to represent sales data for each year.
# Each row represents a year, and each column represents a month's sales.

sales_data = np.array([
    [1000, 1100, 1200, 1300, 1400, 1500, 1600, 1700, 1800, 1900, 2000, 2100],  # 2015 sales data
    [1050, 1150, 1250, 1350, 1450, 1550, 1650, 1750, 1850, 1950, 2050, 2150],  # 2016 sales data
])

# 2. Print the sales for the second year (index 1).
 # Output will be the sales for 2016

# 3. Change the sales for July in the first year (2015) to a new value.
# Set July sales for 2015 to 1650

# 4. Add a new row for another year (2017).
# Note: NumPy arrays have fixed size, so to add new rows, use np.append or recreate the array.

# 5. Print the updated sales data.
```

## NOTE: To append an array:

[https://www.tutorialspoint.com/numpy/numpy\_append.htm](https://www.tutorialspoint.com/numpy/numpy_append.htm)

</details>

<details>

<summary>6 - contact_list.py</summary>

Use lists to store and manipulate a contact list for a phone app. Each contact has a name, phone number, and email address.

| **Name** | **Phone Number** | **Email Address**                             |
| -------- | ---------------- | --------------------------------------------- |
| Alice    | 555-1234         | [alice@email.com](mailto:alice@email.com)     |
| Bob      | 555-5678         | [bob@email.com](mailto:bob@email.com)         |
| Charlie  | 555-8765         | [charlie@email.com](mailto:charlie@email.com) |
| Diana    | 555-4321         | [diana@email.com](mailto:diana@email.com)     |

```python
# 1. Create a list named 'contacts' with at least 4 contacts.
# Each contact will be represented as a list with name, phone, and email.

contacts = [
    ['Alice', '555-1234', 'alice@email.com'],
    ['Bob', '555-5678', 'bob@email.com'],
    ['Charlie', '555-8765', 'charlie@email.com'],
    ['Diana', '555-4321', 'diana@email.com']
]

# 2. Print the details of the second contact.
# Output will be: ['Bob', '555-5678', 'bob@email.com']

# 3. Update the phone number of the third contact.

# 4. Add a new contact to the list.

# 5. Print the updated contact list.
```

</details>

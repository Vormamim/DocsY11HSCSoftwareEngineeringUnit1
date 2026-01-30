---
icon: book-open
---

# Sets

A **set** in Python is a powerful and versatile data structure that represents an **unordered collection** of unique items. Unlike lists or tuples, where the order of elements matters, the items in a set have no specific order.

This unordered nature makes sets ideal for situations where the sequence of items is irrelevant, and only the presence or absence of elements matters.

One of the key characteristics of sets is that they only allow **unique** items, meaning that no two elements within a set can be identical. This uniqueness is enforced automatically by the set itself, making it an excellent choice for tasks where duplicate values need to be avoided.

Creating a set in Python is simple and can be done in two main ways: by placing comma-separated values inside curly braces `{}` or by using the `set()` function.

```python
# A set containing four unique elements: 1, 2, 3, and 4. 
{1, 2, 3, 4} 
```

If you attempt to create a set with duplicate values, such as `{1, 2, 2, 3}`, Python will automatically remove the duplicates, and the resulting set will be `{1, 2, 3}`.

Alternatively, you can create a set from an existing iterable, such as a list or a string, by passing it to the `set()` function.

```python
# A set identical to the one created with curly braces. 
set([1, 2, 3, 4])

# A set created from an existing array.
my_array = [1, 2, 3, 4]
set(my_array)
```

This method is particularly useful when you need to remove duplicates from a list or other collection.

***

## Unique Elements

Sets are particularly useful in scenarios where the uniqueness of elements is crucial.

For example, if you have a list of items and you want to ensure that there are no duplicates, converting the list into a set will automatically filter out any repeated elements.

Sets are also widely used for performing mathematical operations like **unions**, **intersections**, and **differences**. These operations allow you to combine or compare sets in ways that are both efficient and easy to understand. For instance, you can quickly find the common elements between two sets using the intersection operation, or determine which elements are unique to one set by using the difference operation.

***

## Key Features

1. Sets have some limitations due to their unordered nature. Sets do not support **indexing** or **slicing**, which means you cannot access elements by their position or extract a subset of elements using a range of indices.
2. Sets providing highly efficient methods for **checking membership**, **adding new items**, and **removing items**.
   * the `in` keyword can be used to quickly check if a particular element exists within a set,
   * the `add()` method allows you to insert new elements.
   * the `remove()` method lets you delete elements from a set, provided they exist within it. These operations are generally faster with sets than with other data structures like lists, especially when working with large collections of data.
3. Sets in Python are **mutable**, meaning you can add or remove items after the set has been created. However, while the set itself is mutable, the items within it must be **immutable**. This means that you can add elements like numbers, strings, or tuples to a set, but you cannot add lists or other sets because they are mutable. This restriction ensures that the set remains consistent and that its elements can be reliably hashed, which is essential for the set's efficient operation.

## Examples

### Student IDs

| Student ID |
| ---------- |
| 101        |
| 102        |
| 103        |
| 104        |

```python
# 1. Create a set of student IDs. 
# Use curly braces {} to create a set, which automatically ensures uniqueness.

student_ids = {101, 102, 103, 104}

# 2. Add a new student ID to the set.
# Use add() to insert a single element to the set.
student_ids.add(105)

# 3. Remove a student ID from the set.
# Use discard() to remove an element. If the element is not present, discard() does nothing.
student_ids.discard(102)

# 4. Check if a specific student ID exists in the set.
# Use the 'in' keyword to check if an element is in the set.
print(103 in student_ids)  # Output: True

# 5. Print the updated set.
print(student_ids)  # Output might be: {101, 103, 104, 105}
```

***

### Set Operations

**Group A (Set 1):**

| Student ID |
| ---------- |
| 101        |
| 102        |
| 103        |

**Group B (Set 2):**

| Student ID |
| ---------- |
| 103        |
| 104        |
| 105        |

```python
# 1. Create two sets representing the students in Group A and Group B.
group_a = {101, 102, 103}
group_b = {103, 104, 105}

# 2. Find the union of both sets (students in either group or both).
# Use the '|' operator or the union() method to get all unique students from both groups.
union_group = group_a | group_b
print("Union of Group A and Group B:", union_group)

# 3. Find the intersection of both sets (students in both groups).
# Use '&' operator or intersection() method to get common students.
intersection_group = group_a & group_b
print("Intersection of Group A and Group B:", intersection_group)

# 4. Find the difference of Group A and Group B (students only in Group A).
# Use '-' operator or difference() method to get students in Group A but not in Group B.
difference_group = group_a - group_b
print("Difference of Group A and Group B:", difference_group)
```

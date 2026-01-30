---
icon: book-open
---

# Test Data

In the Software Development Life Cycle (SDLC), testing and debugging are critical phases that ensure the software functions as intended and is free of defects.

## Boundary Testing

Boundary value testing is a technique used to identify errors at the boundaries of input ranges.

For instance, if a program accepts numbers between 1 and 100, boundary value testing would check inputs like 1, 100, and slightly beyond these limits (e.g., 0 and 101) to ensure the software handles these extreme values correctly. This approach helps uncover issues that may not be evident when testing within the normal range of inputs.

### Example of Boundary Testing

```python
def is_valid_age(age):
    return 18 <= age <= 60  # Valid range: 18-60

# Test cases
print(is_valid_age(17))  # ❌ Boundary case (just below valid)
print(is_valid_age(18))  # ✅ Lower boundary
print(is_valid_age(60))  # ✅ Upper boundary
print(is_valid_age(61))  # ❌ Boundary case (just above valid)

```

## Path Coverage

Path coverage testing, on the other hand, focuses on ensuring that all possible paths through the code are executed at least once. This technique is vital for identifying logic errors or conditions that might not be triggered under normal circumstances.

For example, consider a program with a loop that executes a set of instructions only if a certain condition is met. Path coverage testing would involve creating test cases that ensure both the condition being true and false are tested, covering all possible execution paths within the program.

### Example of Path Coverage

```python
def check_discount(age):
    if age < 18:
        return "Child Discount"
    elif age >= 65:
        return "Senior Discount"
    else:
        return "No Discount"

# Test cases covering all paths
print(check_discount(10))  # ✅ Child Discount (Path 1)
print(check_discount(30))  # ✅ No Discount (Path 2)
print(check_discount(70))  # ✅ Senior Discount (Path 3)
```

## Faulty and Abnormal Data

Faulty and abnormal data testing is used to evaluate how well a program handles invalid or unexpected inputs. This type of testing ensures that the software doesn't crash or produce incorrect results when it encounters data outside the expected parameters.

For instance, if a program expects a user to enter an integer and the user inputs a string or a special character instead, the program should respond gracefully, perhaps by displaying an error message or requesting valid input.

### Example of Faulty and Abnormal Data

```python
def divide(a, b):
    if b == 0:
        return "Error: Division by zero"
    return a / b

# Test cases
print(divide(10, 2))   # ✅ Normal case
print(divide(5, 0))    # ❌ Abnormal case (division by zero)
print(divide("10", 2)) # ❌ Faulty case (wrong data type)
```


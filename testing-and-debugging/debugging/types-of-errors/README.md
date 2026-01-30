---
icon: book-open
---

# Types of Errors

## Syntax Errors

Syntax errors occur when the code violates the rules of the programming language, such as missing semicolons, incorrect use of operators, or improperly structured statements. These errors prevent the code from running and are usually identified by the compiler or interpreter, which provides feedback on where the issue lies in the code.

```python
# Syntax error: Missing closing parenthesis
print("Hello, world!"
```

## Logical Errors

Logical errors occur when the code is syntactically correct but does not produce the expected result. These errors arise from mistakes in the program's logic, such as incorrect conditions in loops or faulty calculations. Logical errors are often more challenging to detect because the code runs without crashing, but it does not behave as intended, leading to incorrect outputs or unintended behaviour.

```python
# Logical error: Incorrect sum calculation
a = 5
b = 10
result = a - b  # Should be addition instead of subtraction
print(result)  # Expected: 15, but it prints -5
```

## Runtime Errors

Runtime errors occurs while the program is running. These errors can result from issues like dividing by zero, accessing out-of-bounds array elements, or trying to use null references. Runtime errors cause the program to crash or behave unpredictably and require careful examination of the code's execution to identify the problem.

```python
# Runtime error: Division by zero
a = 10
b = 0
result = a / b  # Division by zero will cause a runtime error
print(result)
```

```python
# Runtime error: AttributeError
my_str = "hello"
print(my_str.append(" world"))  # 'str' object has no attribute 'append'
```

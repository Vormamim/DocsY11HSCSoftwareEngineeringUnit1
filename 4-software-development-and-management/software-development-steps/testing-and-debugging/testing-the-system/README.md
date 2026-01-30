---
icon: book-open
---

# Testing the System

Testing in software engineering is the process of systematically evaluating a software application to ensure it meets the specified requirements and functions as expected.

The primary goal of testing is to identify and fix defects or issues in the software before it is deployed to end-users.

Testing ensures that the software is reliable, performs well, and provides a positive user experience by verifying that each component and the system as a whole operate correctly under various conditions.

There are three levels of testing a system:

* **Unit Testing:** Tests individual functions using basic assertions.
* **Integration Testing:** Tests how different functions or modules interact by combining them.
* **System Testing:** Tests the entire system as a whole, ensuring everything works together as expected.

## Unit Testing

Unit testing is the most granular level of testing, focusing on individual components or functions within a software application. Each unit, typically a single function or method, is tested in isolation to verify that it behaves as intended.

Unit testing helps developers identify issues early in the development process, ensuring that the smallest building blocks of the software are correct before they are integrated with other parts of the application. This type of testing is usually automated, allowing developers to run tests frequently as they make changes to the code.

### Example: Unit Testing

```python
# Function to be tested
def add_numbers(a, b):
    return a + b

# Unit tests (without using classes)
def test_add_positive_numbers():
    assert add_numbers(2, 3) == 5, "Test failed: 2 + 3 should be 5"

def test_add_negative_numbers():
    assert add_numbers(-2, -3) == -5, "Test failed: -2 + -3 should be -5"

def test_add_mixed_numbers():
    assert add_numbers(-2, 3) == 1, "Test failed: -2 + 3 should be 1"

# Run the tests
test_add_positive_numbers()
test_add_negative_numbers()
test_add_mixed_numbers()

print("All unit tests passed!")

```

***

## Integration Testing

Integration testing comes after unit testing and involves combining individual units or components of the software to test how they work together. The goal is to ensure that these combined parts interact correctly and produce the desired outcomes.

Integration testing helps identify issues that may arise when different components are integrated, such as data passing between modules, communication errors, or unexpected behaviors. It is a critical step in ensuring that the different parts of the software system function together as a cohesive whole.

### Example of Integration Testing

```python
# user_module.py
def get_user_data(username):
    user_data = {
        "john": {"password": "1234", "email": "john@example.com"},
        "mary": {"password": "5678", "email": "mary@example.com"}
    }
    return user_data.get(username, None)

# login_module.py (same as before)
from user_module import get_user_data

def user_login(username, password):
    user_data = get_user_data(username)
    if user_data and user_data["password"] == password:
        return "Login Successful"
    else:
        return "Login Failed"

# Integration tests (without using classes)
def test_valid_login():
    result = user_login("john", "1234")
    assert result == "Login Successful", f"Test failed: Expected 'Login Successful' but got {result}"

def test_invalid_login():
    result = user_login("john", "wrongpassword")
    assert result == "Login Failed", f"Test failed: Expected 'Login Failed' but got {result}"

def test_user_not_found():
    result = user_login("nonexistent", "password")
    assert result == "Login Failed", f"Test failed: Expected 'Login Failed' but got {result}"

# Run the tests
test_valid_login()
test_invalid_login()
test_user_not_found()

print("All integration tests passed!")

```

***

## System Testing

System testing is the level of testing where the entire software application is tested as a complete system. This type of testing verifies that the software meets the specified requirements and functions correctly in its intended environment.

System testing includes testing the software's functionality, performance, security, and compatibility with other systems or devices.

It is the final testing phase before the software is released, ensuring that it operates as expected under real-world conditions and is ready for deployment to end-users.

### Example of System Testing

```python
# Full login system: user_module.py + login_module.py

# user_module.py (same as before)
def get_user_data(username):
    user_data = {
        "john": {"password": "1234", "email": "john@example.com"},
        "mary": {"password": "5678", "email": "mary@example.com"}
    }
    return user_data.get(username, None)

# login_module.py (same as before)
from user_module import get_user_data

def user_login(username, password):
    user_data = get_user_data(username)
    if user_data and user_data["password"] == password:
        return "Login Successful"
    else:
        return "Login Failed"

# System tests (without using classes)
def test_login_system():
    result1 = user_login("john", "1234")
    assert result1 == "Login Successful", f"Test failed: Expected 'Login Successful' but got {result1}"

    result2 = user_login("john", "wrongpassword")
    assert result2 == "Login Failed", f"Test failed: Expected 'Login Failed' but got {result2}"

    result3 = user_login("nonexistent", "password")
    assert result3 == "Login Failed", f"Test failed: Expected 'Login Failed' but got {result3}"

# Run the system test
test_login_system()

print("All system tests passed!")

```


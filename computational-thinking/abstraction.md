---
icon: book-open
---

# Abstraction

**Abstraction** in software design is the practice of hiding unnecessary details and exposing only the essential features of a system. It helps simplify complex systems by focusing on **what** a component does rather than **how** it does it.

For example:

* In **Object-Oriented Programming (OOP)**, abstraction is achieved using **classes and interfaces** to define behaviors without revealing implementation details.
* In **DFDs**, higher levels (like Level 0) show broad system functions, while deeper levels break them into detailed processes.

Abstraction improves **clarity, maintainability, and scalability** by reducing complexity and emphasizing key functionalities.

## Example - User Authentication System

For example, when designing a user authentication system, you focus on what the system **needs to achieve** (e.g., verifying user credentials) rather than the intricate details of how passwords are stored and verified. By abstracting these details, you can streamline the development process and create a more efficient system.

* The **`authenticate_user`** function focuses on the high-level goal of verifying user credentials without worrying about how this verification is done.
* The function **`verify_credentials`** handles the process of checking if the provided credentials match the stored ones, but it abstracts away the details of how passwords are retrieved and compared.
* **`get_stored_password`** and **`compare_passwords`** are further abstractions that hide the details of how passwords are retrieved from storage and how they are compared.
* The **`main`** function represents the point where the authentication process is initiated, abstracting all the underlying complexity.

Define the high-level goal of the authentication system - the system needs to verify user credentials

```python
def authenticate_user(username, password):
    # Call a function to verify the credentials
    if verify_credentials(username, password):
        return "Authentication Successful"
    else:
        return "Authentication Failed"
```

Abstract the details of how credentials are verified into a separate function.

```python
def verify_credentials(username, password):
    # Call a function to retrieve the stored password for the user
    stored_password = get_stored_password(username)  
     
    # Call a function to compare the provided password with the stored password
    if compare_passwords(stored_password, password):
        return True
    else:
        return False
```

Abstract the retrieval of the stored password.

```python
def get_stored_password(username):
    # (Details of how the password is retrieved from the database are hidden)
    return retrieved_password_from_database(username)
```

Abstract the comparison of passwords.

```python
def compare_passwords(stored_password, provided_password):
    # (Details of how passwords are hashed and compared are hidden)
    return compare_hashes(stored_password, hash_password(provided_password))
```

High-level function that calls authenticate\_user and handles the result

```python
def main(): 
	username = input("Enter your username: ") 
	password = input("Enter your password: ") 
	result = authenticate_user(username, password) 
	print(result)
```

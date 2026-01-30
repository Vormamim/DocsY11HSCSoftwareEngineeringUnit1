---
icon: clipboard-list-check
---

# Activities

1. **Compare** boundary testing, path coverage testing and faulty and abnormal data testing.

{% hint style="warning" %}
### Compare

* Show how things are similar or different.
{% endhint %}

2. Write **test cases** for **boundary values** for the following:

```python
def is_safe_temperature(temp):
    return 0 <= temp <= 100

# TODO: Write test cases for boundary values

```

3. Write **test cases** for **path coverage** for the following:

```python
def ticket_price(age):
    if age < 5:
        return "Free"
    elif 5 <= age <= 17:
        return "$5"
    elif 18 <= age <= 64:
        return "$10"
    else:
        return "Senior Discount - $7"

# TODO: Write test cases for all paths

```

4. Write **test cases** for **faulty and abnormal data** for the following:

```python
def divide_numbers(a, b):
    try:
        return a / b
    except ZeroDivisionError:
        return "Error: Cannot divide by zero"
    except TypeError:
        return "Error: Invalid input, numbers required"

# TODO: Write test cases for abnormal and faulty inputs

```


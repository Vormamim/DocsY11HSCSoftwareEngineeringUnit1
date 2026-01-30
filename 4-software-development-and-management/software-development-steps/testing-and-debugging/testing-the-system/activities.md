---
icon: clipboard-list-check
---

# Activities

1. **Compare** unit testing, integration testing and system testing.

{% hint style="warning" %}
### Compare

* Show how things are similar or different.
{% endhint %}

2. Modify the functions to use unit testing, integration testing and system testing below.
   * First, create a new folder in **Visual Studio Code.**&#x20;
   * Create a file called **`inventory_management.py`**
   * **Copy the code block below, then save the file.**

{% code title="inventory_management.py" %}
```python
# Dictionary to store product quantities
inventory = {}

# Function to add products to the inventory
def add_product(product, quantity):
    if product in inventory:
        inventory[product] += quantity
    else:
        inventory[product] = quantity

# Function to sell products (decrease product quantity)
def sell_product(product, quantity):
    if product in inventory and inventory[product] >= quantity:
        inventory[product] -= quantity
    else:
        return "Insufficient stock"

# Function to check if a product is available
def check_availability(product):
    return inventory.get(product, 0)

# Function to get total inventory value (simple example assuming fixed price for each product)
def total_inventory_value():
    prices = {
        'apple': 1.0,
        'banana': 0.5,
        'cherry': 1.5
    }
    total_value = 0
    for product, quantity in inventory.items():
        total_value += quantity * prices.get(product, 0)
    return total_value

```
{% endcode %}

* Now, create a new file in the same folder called **`main.py`**

{% hint style="warning" %}
**Any area that includes the comment `"# TODO:"` requires your attention.**

**In UNIT TESTING, "Assert" lines have been commented out. Uncomment each one (remove #), ONE AT A TIME, to test how it works.**

**For the functions AT THE BOTTOM of `main.py` comment all of them out EXCEPT FOR ONE AT A TIME.**

**Try `unit_test()` first, then `integration_test()`, then `system_test()`**
{% endhint %}

{% code title="main.py" %}
```python
from inventory_management import *

# -------------------------------------------
# Unit Testing
# -------------------------------------------
def unit_test():
    """Test individual functions in isolation."""
    
    # Test adding products
    add_product('apple', 50)  # Adding 50 more apples
    add_product('banana', 20)  # Adding 20 more bananas

    
    # Test selling products
    result = sell_product('apple', 10)
    # assert result is None, f"Expected None but got {result}"  # No error should occur
    # assert check_availability('apple') == 40, "Apple stock should be 40 after selling 10."

    # Test insufficient stock. Trying to sell more than available - if you sell more than 20, this SHOULD NOT present an error.
    result = sell_product('banana', 200)  # Selling 200 should not raise an error - if it does, the sell_product function needs fixing.
    # assert result == "Insufficient stock", f"Expected 'Insufficient stock' but got {result}."

    # TODO: Test selling a non-existent product (e.g., 'grape') and check behavior.
    # For example, it should return "Insufficient stock" or similar.

# -------------------------------------------
# Integration Testing
# -------------------------------------------
def integration_test():
    """Test how different functions from the Inventory Management module work together."""
    
    # Add products to inventory
    add_product('apple', 50)
    add_product('banana', 30)

    # Sell some products
    sell_product('apple', 10)
    sell_product('banana', 5)

    # Check stock after selling
    apple_stock = check_availability('apple')
    banana_stock = check_availability('banana')

    # Print results for verification
    print("\n----- Integration Test Results -----")
    print(f"Apple stock after sale: {apple_stock} (Expected: 40)")  # 50 - 10
    print(f"Banana stock after sale: {banana_stock} (Expected: 25)")  # 30 - 5

    # TODO: Test checking availability of a non-existent product (e.g., 'mango', should return 0).
    
    # TODO: Test total inventory value after sales
    print(f"Total inventory value: {total_inventory_value()} (Expected: 70)")

# -------------------------------------------
# System Testing
# -------------------------------------------
def system_test():
    """Test the system as a whole."""
    
    # Run through the entire process: adding, selling, checking availability
    add_product('apple', 50)
    add_product('banana', 30)
    sell_product('apple', 10)
    sell_product('banana', 5)

    # Check final availability and inventory value
    apple_stock = check_availability('apple')
    banana_stock = check_availability('banana')
    inventory_value = total_inventory_value()

    print("\n----- System Test Results -----")
    print(f"Apple stock: {apple_stock} (Expected: 40)")  # 50 - 10
    print(f"Banana stock: {banana_stock} (Expected: 25)")  # 30 - 5
    print(f"Total inventory value: {inventory_value} (Expected: 70)")  # (40 * 1.0) + (25 * 0.5)
    
    # TODO: Add tests for boundary conditions such as no stock or empty inventory.
    # For example, check if the inventory value is 0 when no products exist.

# -------------------------------------------
# Running the Tests
# -------------------------------------------
if __name__ == "__main__":
    # Run all tests - UNCOMMENT EACH FUNCTION ONE AT A TIME!
    print("Running Unit Test...")
    unit_test()

    # print("\nRunning Integration Test...")
    # integration_test()

    # print("\nRunning System Test...")
    # system_test()
```
{% endcode %}

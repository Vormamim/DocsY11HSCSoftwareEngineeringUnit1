---
icon: book-open
---

# Example: Payment Program

## Scenario:

We have two Python modules:

1. **orders.py** – Handles order creation.
2. **payments.py** – Processes payments.

When an order is placed, it sends the order details to the payment module for processing.

### Step 1: Define the `payments` Module

`payments.py`

```python
def process_payment(order_id, amount):
    print(f"Processing payment of ${amount} for Order {order_id}")
    return f"Payment for Order {order_id} successful"

```

### **Step 2: Integrate with the `orders` Module**

`orders.py`

```python
from payments import * #Import the payments module

def place_order():
    order_id = 101
    amount = 50.00
    confirmation = payments.process_payment(order_id, amount)  #Integration happens here
    print(confirmation)

place_order() #Run the function to simulate order placement

```

### Expected Output:

```
Processing payment of $50.0 for Order 101
Payment for Order 101 successful
```


---
icon: clipboard-list-check
---

# Activities

1. Copy the following into a new Python file:

{% code title="discount.py" %}
```python
def calculate_total(price, quantity):
    total = price * quantity  # Line 3
    return total  # Line 4

def apply_discount(total, discount):
    return total - (total * discount)  # Line 6

def main():
    price = 100
    quantity = 5
    discount = 10  #
    total = calculate_total(price, quantity)  # Line 10
    total_after_discount = apply_discount(total)  # Line 11
    print(f"Total after discount: {total_after_discount}")  # Line 12

main()
```
{% endcode %}

2. **Set Up Debugging Mode**

* Open the **Run and Debug** panel (`Ctrl + Shift + D`).
* Click **"Run and Debug"** and choose **"Python File"**.

3. **Add Breakpoints**

* Click to the left of the line numbers to set breakpoints at:
  * **Line 3** (where `total` is calculated)
  * **Line 6** (where discount is applied)
  * **Line 10** (when `calculate_total` is called)
  * **Line 11** (when `apply_discount` is called)

4. **Run the Debugger**

* Press `F5` to start debugging.
* Use `F10` to **step over** each line and inspect variables in the **Variables** panel.
* Use the **Debug Console** to check variable values.

5. I**dentify** the mistakes, correct them, and rerun the program to verify your fix.

{% hint style="success" %}
## **Submit when Finished**

Submit a **screenshot** of your debug log to Google Classroom when you are finished.
{% endhint %}


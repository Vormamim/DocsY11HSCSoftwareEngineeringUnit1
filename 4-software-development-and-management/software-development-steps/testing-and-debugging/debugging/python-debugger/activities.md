---
icon: clipboard-list-check
---

# Activities

**Copy the following into a new Python file:**

```python
import pdb

def calculate_total(price, quantity):
    total = price * quantity  # Line 3
    return total  # Line 4

def apply_discount(total, discount):
    return total - (total * discount)  # Line 6

def main():
    price = 100
    quantity = 5
    discount = 0.1  # 10% discount
    total = calculate_total(price, quantity)  # Line 10
    total_after_discount = apply_discount(total, discount)  # Line 11
    print(f"Total after discount: {total_after_discount}")  # Line 12

pdb.set_trace()  # Pause the program here

main()
```

1.  **Breakpoint and Next (n)**

    1. Run the above code. When the debugger starts running, type '**n**' and press enter on each line until you are finished debugging.
    2. **Describe** what happened.


2. **Single Line Stepping (s)**
   1. Run the above code. When the debugger starts running, type '**s**' and press enter on each line until you are finished debugging.
   2. **Describe** what happened.

{% hint style="warning" %}
### **Describe**

* Provide characteristics and features.
{% endhint %}

3. **Compare** the **next** **(n)** command with the **step** **(s)** command.

{% hint style="warning" %}
### Compare

* Show how things are similar or different.
{% endhint %}

4.  **Watch, whatis and print (p)**

    1. Run the above code. When the debugger starts running, type **'s'** and press **enter** for **8 lines in a row.**&#x20;
    2. Then, type '**whatis total'**
    3. Then, type **'p total'**
    4. **Describe** what happened.


5. **Compare whatis** and **print (p)** commands.

{% hint style="success" %}
## **Submit when Finished**

Submit a **screenshot** of the above to Google Classroom when you are finished.#&#x20;
{% endhint %}




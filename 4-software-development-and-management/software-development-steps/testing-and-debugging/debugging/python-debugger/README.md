---
icon: book-open
---

# Python Debugger

We're going to first start by looking at the standard Python Debugger, then the VS Code debugger.

## Python Debugger Commands

When using the Python Debugger, enter one of these 3 commands.

* **`n` (next)**: Executes the next line of code (steps over function calls).
* **`s` (step)**: If you were to use this instead of `n`, it would step into the function call.
* **`c` (continue)**: Continues the program execution without stopping.
* **p (print)**: Prints the value of a variable or expression. Example: `p total` to print the value of the `total` variable.
* **whatis**: Prints the type of a variable. Example: `whatis total` to check the type of the `total` variable (e.g., `int`, `float`, etc.).

## Breakpoints

Breakpoints are a fundamental debugging tool that allows a programmer to pause the execution of a program at a specific point in the code. This pause enables the developer to inspect the current state of the program, including the values of variables and the flow of execution. By strategically placing breakpoints in the code, a programmer can isolate and examine sections of the program where issues are suspected, making it easier to identify and fix errors.

#### **Python:**

```python
import pdb  # Import the Python debugger

def add(a, b):
    result = a + b 
    pdb.set_trace()  # Pause the program here and start the debugger
    return result 

x = 2 
y = 3  
sum_result = add(x, y)  
print(sum_result)  
```

#### **Debugger:**

```
> <your_file>.py(6)add()
-> return result
(Pdb) p result
5
(Pdb) n
> <your_file>.py(8)<module>()
-> print(sum_result)
(Pdb) c
5
```

## Single Line Stepping

Single line stepping is another essential debugging technique that works hand-in-hand with breakpoints. Once the program is paused at a breakpoint, single line stepping allows the developer to execute the program one line at a time. This step-by-step execution helps the programmer closely monitor the behaviour of the program, observe changes in variables, and understand the flow of control through the code. Single line stepping is particularly useful for identifying logical errors, as it provides a clear view of how each line of code affects the program's state.

#### Python

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

#### Debugger

```
> <your_file>.py(12)<module>()
-> main()
(Pdb) s
> <your_file>.py(4)main()
-> price = 100
(Pdb) s
> <your_file>.py(5)main()
-> quantity = 5
(Pdb) s
> <your_file>.py(6)main()
-> discount = 0.1
(Pdb) s
> <your_file>.py(7)main()
-> total = calculate_total(price, quantity)
(Pdb) s
> <your_file>.py(3)calculate_total()
-> total = price * quantity
(Pdb) s
> <your_file>.py(4)calculate_total()
-> return total
(Pdb) s
> <your_file>.py(8)main()
-> total_after_discount = apply_discount(total, discount)
(Pdb) s
> <your_file>.py(6)apply_discount()
-> return total - (total * discount)
(Pdb) s
> <your_file>.py(9)main()
-> print(f"Total after discount: {total_after_discount}")
(Pdb) s
Total after discount: 450.0
> <your_file>.py(10)<module>()
-> 
(Pdb) 
```

Watches are a feature that allows developers to keep track of specific variables or expressions as the program runs. By setting up watches, a programmer can monitor the values of these variables in real-time, even as the program continues to execute. This is invaluable when trying to understand how certain values change over time or when debugging complex conditions that depend on multiple variables. Watches provide a dynamic view of the program's internal state, making it easier to identify when and where things go wrong.

#### Python

```python
import pdb

def calculate_total(price, quantity):
    total = price * quantity  # Line 3
    return total  # Line 4

def main():
    price = 50
    quantity = 3
    total = calculate_total(price, quantity)  # Line 7
    print(total)  # Line 8

pdb.set_trace()  # Pause the program here

main()
```

#### Debugger

```
(Pdb) s
--Call--
> <your_file_path>(3)calculate_total()
(Pdb) s
--Line 4--
> <your_file_path>(4)calculate_total()
(Pdb) s
--Return--
> <your_file_path>(4)calculate_total() 15
(Pdb) s
--Return--
> <your_file_path>(7)main()
(Pdb) s
--Line 8--
> <your_file_path>(8)main()
(Pdb) s
--Return--
> <your_file_path>(8)main()
(Pdb) s
--Return--
> <your_file_path>(8)main()
(Pdb) p total
15
(Pdb) whatis total
int
```

## Interfaces between Functions

Functions often interact with one another by passing data or calling each other’s methods. The interface between functions refers to the way these functions communicate, including the parameters they accept, the values they return, and the side effects they produce. When debugging, it is important to ensure that data passed between functions is correct and consistent, as errors in these interfaces can lead to unexpected behaviour and bugs. Understanding these interfaces helps developers trace the flow of data through the program and identify where issues may arise.


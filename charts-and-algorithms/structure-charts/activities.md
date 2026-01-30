---
icon: clipboard-list-check
---

# Activities

{% hint style="warning" %}
To create Structure Charts, try PowerPoint or LucidChart. I found PowerPoint easier for this one but it's up to you!
{% endhint %}

1. **Create a structure chart for the following programs.**&#x20;
   1. **Calculator Program:**

<pre class="language-python"><code class="lang-python"><strong>def main():
</strong>    num1 = float(input("Enter first number: "))
    num2 = float(input("Enter second number: "))
    operation = input("Enter operation (+, -, *, /): ")
    
    if operation == "+":
        result = add(num1, num2)
    elif operation == "-":
        result = subtract(num1, num2)
    elif operation == "*":
        result = multiply(num1, num2)
    elif operation == "/":
        result = divide(num1, num2)
    else:
        print("Invalid operation")
        return

    print(f"The result is: {result}")

def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "Error: Cannot divide by zero"
    return x / y

main()
</code></pre>

**b. Shopping Cart Program:**

<pre class="language-python"><code class="lang-python">def main():
    cart = []
    total_price = 0

    while True:
        print("\nShopping Cart Menu:")
        print("1. Add item to cart")
        print("2. Remove item from cart")
        print("3. View cart")
        print("4. Checkout")
        choice = input("Choose an option: ")

        if choice == "1":
            item, price = add_item()
            cart.append((item, price))
        elif choice == "2":
            remove_item(cart)
        elif choice == "3":
            view_cart(cart)
        elif choice == "4":
            total_price = checkout(cart)
            print(f"Total price: ${total_price:.2f}")
            break
        else:
            print("Invalid choice. Try again.")

def add_item():
    item = input("Enter item name: ")
    price = float(input("Enter item price: "))
    return item, price

<strong>def remove_item(cart):
</strong>    item = input("Enter item name to remove: ")
    for i in range(len(cart)):
        if cart[i][0] == item:
            cart.pop(i)
            print(f"{item} has been removed from your cart.")
            return
    print(f"{item} not found in your cart.")

def view_cart(cart):
    if not cart:
        print("Your cart is empty.")
    else:
        for item, price in cart:
            print(f"{item}: ${price:.2f}")

def checkout(cart):
    total = 0
    for item, price in cart:
        total += price
    return total

main()
</code></pre>


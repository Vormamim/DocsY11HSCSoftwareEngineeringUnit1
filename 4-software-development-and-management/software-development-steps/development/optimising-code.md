---
icon: book-open
---

# Optimising Code

It is important that when creating our code we are as efficient as possible. This not only saves time, but also saves storage and improves efficiency when running a program.

Look at the following for advice on how we can best optimise code - you may even find you come across functions you have not used before!

<table data-full-width="true"><thead><tr><th width="247">Code Practice</th><th width="348">Unoptimised</th><th>Optimised</th></tr></thead><tbody><tr><td><p><strong>Using List Comprehensions</strong></p><p>Instead of using loops to create or transform lists, use list comprehensions, which are more concise and often faster.</p></td><td><pre class="language-python"><code class="lang-python">squares = [] 
for i in range(10): 
    squares.append(i * i)
</code></pre></td><td><pre class="language-python"><code class="lang-python">squares = [i * i for i in range(10)]
</code></pre></td></tr><tr><td><p><strong>Using Generator Expressions for Large Data</strong></p><p>Generators are more memory-efficient than lists when dealing with large datasets because they generate items on the fly rather than storing them all in memory.</p></td><td><pre class="language-python"><code class="lang-python">squares = [i * i for i in range(1000000)]
</code></pre></td><td><pre class="language-python"><code class="lang-python">squares = (i * i for i in range(1000000))
</code></pre></td></tr><tr><td><p><strong>Using Built-In Functions</strong></p><p>Python's built-in functions are implemented in C and are highly optimised for performance.</p></td><td><pre class="language-python"><code class="lang-python">total = 0 
for num in range(1, 1001): 
    total += num
</code></pre></td><td><pre class="language-python"><code class="lang-python">total = sum(range(1, 1001))
</code></pre></td></tr><tr><td><p><strong>Avoiding Unnecessary List Copying</strong></p><p>When you slice a list, Python creates a new list object. To avoid unnecessary copying, work with the original list when possible.</p></td><td><pre class="language-python"><code class="lang-python">new_list = my_list[:]
</code></pre></td><td><pre class="language-python"><code class="lang-python">new_list = my_list
</code></pre></td></tr><tr><td><p><strong>Avoiding Global Variables</strong></p><p>Accessing global variables is slower than accessing local variables. It is often better to pass variables as arguments to functions instead of relying on global state.</p></td><td><pre class="language-python"><code class="lang-python">x = 10 
def add_to_x(y): 
    return x + y
</code></pre></td><td><pre class="language-python"><code class="lang-python">def add_to_x(x, y): 
    return x + y
</code></pre></td></tr><tr><td><p><strong>Using <code>join()</code> for String Concatenation</strong></p><p>Concatenating strings with <code>+</code> can be inefficient because it creates a new string object each time. Instead, use <code>join()</code> to concatenate a list of strings.</p></td><td><pre class="language-python"><code class="lang-python">words = ["Hello", "world", "from", "Python"]
sentence = ""
for word in words:
    sentence += word + " "
</code></pre></td><td><pre class="language-python"><code class="lang-python">words = ["Hello", "world", "from", "Python"]
sentence = " ".join(words)
</code></pre></td></tr><tr><td><p><strong>Using <code>enumerate()</code> for Indexed Iteration</strong></p><p>This technique avoids manual index management.</p></td><td><pre class="language-python"><code class="lang-python">i = 0
for item in my_list:
    print(i, item)
    i += 1
</code></pre></td><td><pre class="language-python"><code class="lang-python">for i, item in enumerate(my_list):
    print(i, item)
</code></pre></td></tr><tr><td><p><strong>Minimising Function Calls in Loops</strong></p><p>Repeated function calls in loops can slow down performance. Instead, store function results in a variable if they are called multiple times.</p></td><td><pre class="language-python"><code class="lang-python">for i in range(len(my_list)):
    print(len(my_list))
</code></pre></td><td><pre class="language-python"><code class="lang-python">list_length = len(my_list)
for i in range(list_length):
    print(list_length)
</code></pre></td></tr><tr><td><p><strong>Using <code>any()</code> and <code>all()</code></strong></p><p>These functions are useful for checking conditions in a collection and are faster than manually looping through each element.</p></td><td><pre class="language-python"><code class="lang-python">found = False
for item in my_list:
    if item > 10:
        found = True
        break
</code></pre></td><td><pre class="language-python"><code class="lang-python">found = any(item > 10 for item in my_list)
</code></pre></td></tr></tbody></table>

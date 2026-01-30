---
icon: book-open
---

# Integration

This is the part where you need to get all your functions from your **`module`** working in your **`main.py`** file.

Now, we can import each function **one by one**, but it is likely easier for you to import **all functions** from your module.

So at the **top of your `main.py` file,** you could add a line like the following for **one** **function:**

```python
from pokedex import search_pokemon
```

**However,** again, it is easier to import **all functions** from a module, which we can do with code like the following:

```python
from pokedex import * 
```

That will import **ALL** functions from the module so that you can use them as if they were in the same file. **Remember to store BOTH of these files in the SAME FOLDER if you want it to work!**

***

{% hint style="warning" %}
## Testing and Debugging - Don't Forget!

Don't forget to keep making regular commits to GitHub as part of your **Testing and Debugging** documentation.

[Click here to revisit those requirements again.](../testing-and-debugging/)
{% endhint %}

{% hint style="warning" %}
## PROJECT\_DOCUMENTATION.md

Remember to update your project documentation to include a code block of your integrated programs under the heading _**Integration**_**.**
{% endhint %}


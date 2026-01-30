---
icon: book-open
---

# Development

It is now time to start writing your code. You will be provided of examples to get you started.&#x20;

**You are welcome to use and editing the examples - there are no disadvantages in doing so. It depends on what you are wanting to do.**

This is the process  you are recommended to follow:

{% stepper %}
{% step %}
### Create UI in `main.py`

Inside a program called `main.py` create your User Interface. Define and run the main() function. For now, just focus on getting the UI working and **test each user choice with simple print statements to make sure the UI functions as intended.**
{% endstep %}

{% step %}
### Create Module for Functions in Separate .py file

Create a module (separate .py file) for functions and API call (e.g. `pokedex.py`) and keep main.py and this .py file in the same folder.&#x20;
{% endstep %}

{% step %}
### Test Your Functions

Make sure your functions work! Test them **inside the separate .py file, one at a time.**
{% endstep %}

{% step %}
### Commit to GitHub

Make sure to make regular commits to GitHub!&#x20;

**Check out the '**[**Testing and Debugging'**](../testing-and-debugging/) **section for what you may write in your commits.**
{% endstep %}

{% step %}
### Add Code Blocks to PROJECT\_DEVELOPMENT.md

Once you have finished your above files and they work, place them in code blocks under a heading of **Development** in your PROJECT\_DEVELOPMENT.md file.&#x20;
{% endstep %}
{% endstepper %}

***

{% hint style="warning" %}
## **Code Comments**

Remember to add comments to your code as you go - it is part of the assessment criteria!&#x20;

Also consider using Doc Strings to document your functions in more detail (they can be multi-line which is handy!).

For more information, [click this link to Comments vs DocStrings](comments-vs-docstrings.md).
{% endhint %}

***

## Computational Thinking

In the above, we are engaging in both **decomposition** and **abstraction.**&#x20;

<details>

<summary>Decomposition</summary>

**Decomposition is about breaking a complex system into smaller parts.**

By separating the UI from the backend logic (e.g., functions handling Pokémon data), you're decomposing the program into modules.

</details>

<details>

<summary><strong>Abstraction</strong></summary>

**Abstraction is about hiding complex details and exposing only what is necessary.**

The UI abstracts away the implementation details, allowing users to interact without seeing the inner workings.

</details>

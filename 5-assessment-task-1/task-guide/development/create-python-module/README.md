---
icon: book-open
---

# Create Python Module

Now we need to create our module where we will **import all of our functions from.**&#x20;

Essentially, you are just creating your functions in a **separate .py file**, so we do not clutte&#x72;**`main.py`.**

It must be in the **same folder.**&#x20;

**We will integrate them LATER -** in the **INTEGRATION** step!

The following is an example of the **`pokedex.py`** module.

<pre class="language-python" data-title="pokedex.py"><code class="lang-python">import requests # Must import requests so we can use API

# API Base URL for PokéAPI
API_URL = "https://pokeapi.co/api/v2/pokemon/"

# Dictionary to store collected Pokémon
pokedex = {}

def search_pokemon(name):
    """Search for a Pokémon by name or ID and return its details.""" # Triple quotes is a docstring - allows multiline comments!
    response = requests.get(f"{API_URL}{name.lower()}")
    if response.status_code == 200:
        data = response.json()
        return {
            "name": data["name"].capitalize(),
            "id": data["id"],
            "height": data["height"],
            "weight": data["weight"],
            "types": [t["type"]["name"] for t in data["types"]]
        }
    else:
        print("Pokémon not found.")
        return None

def add_pokemon(name):
    """Add a Pokémon to the Pokédex."""
    pokemon = search_pokemon(name)
    if pokemon:
        pokedex[pokemon["name"]] = pokemon
        print(f"{pokemon['name']} added to Pokédex.")

def view_pokedex():
    """Display all collected Pokémon."""
    if pokedex:
        for name, details in pokedex.items():
            print(f"{name} - ID: {details['id']}, Height: {details['height']}, Weight: {details['weight']}, Types: {', '.join(details['types'])}")
    else:
        print("Your Pokédex is empty.")

def remove_pokemon(name):
    """Remove a Pokémon from the Pokédex."""
    if name.capitalize() in pokedex:
        del pokedex[name.capitalize()]
        print(f"{name.capitalize()} removed from Pokédex.")
    else:
        print("Pokémon not found in your Pokédex.")

<strong>#&#x3C;------------------------------TEST YOUR FUNCTIONS BELOW------------------------------>
</strong>
</code></pre>

***

Now, with the above we have defined all functions and included the API call. Keep in mind some APIs such as WeatherAPI will require a key as well - a separate example will be provided.&#x20;

However, we now need to test each function. Rather than having to test each in the UI and spend forever, **it's often best to just run the functions below our code here.**

Here is an example of how you might test each function:

```python
#<------------------------------TEST YOUR FUNCTIONS BELOW------------------------------>
print(search_pokemon('Pikachu'))

```

As the search\_pokemon() function only returns a value and does not print if it is successful, we need to add the print statement to the function call to see what values it actually returns

***

```python
#<------------------------------TEST YOUR FUNCTIONS BELOW------------------------------>
add_pokemon('Pikachu')
```

This function actually has print statements, so we can test it just as above

***

```python
#<------------------------------TEST YOUR FUNCTIONS BELOW------------------------------>
add_pokemon('Pikachu')
view_pokedex()
remove_pokemon('Pikachu')
```

Some functions may depend on other functions being run first. For instance, we cannto view a pokemon in our pokedex or remove it **unless we add one first.**

***

```python
#<------------------------------TEST YOUR FUNCTIONS BELOW------------------------------>
view_pokedex()
remove_pokemon('Pikachu')
```

In saying that, **we still need to test both on their own** so we know that **all possible outcomes** will work.

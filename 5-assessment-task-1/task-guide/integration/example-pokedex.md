---
icon: book-open
---

# Example: Pokedex

## main.py:

The following code is an example of the updated **user interface code** from **main.py**, which now imports the **pokedex.py module.**

{% code title="main.py" %}
```python
from pokedex import * #Imports pokedex.py module

def main():
    while True:
        print("\nPokédex Menu:")
        print("1. Search Pokémon")
        print("2. Add Pokémon to Pokédex")
        print("3. View Pokédex")
        print("4. Remove Pokémon")
        print("5. Exit")
        choice = input("Choose an option: ")

        if choice == "1":
            name = input("Enter Pokémon name or ID: ")
            details = search_pokemon(name)
            if details:
                print(details)
        elif choice == "2":
            name = input("Enter Pokémon name to add: ")
            add_pokemon(name)
        elif choice == "3":
            view_pokedex()
        elif choice == "4":
            name = input("Enter Pokémon name to remove: ")
            remove_pokemon(name)
        elif choice == "5":
            print("Exiting Pokédex.")
            break
        else:
            print("Invalid choice. Please try again.")

if __name__ == "__main__":
    main()
```
{% endcode %}

## The Module:

The following is the **pokedex.py** module that **main.py** imports.

{% code title="pokedex.py" %}
```python
import requests

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
```
{% endcode %}


---
icon: book-open
---

# UI - main.py

Let's start with creating the UI. Remember that **you DO NOT need** to implement all functionality yet, it is **ONLY** about the **USER INTERFACE** at this point in time.

The following is a simple UI designed in the `main()` function.&#x20;

Here's what it may look like in the Pokedex example **(feel free to test and adapt this to your system if you would like).**&#x20;

```python
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
            print(f"Search for {name}'s details") #Replace with function later
        elif choice == "2":
            name = input("Enter Pokémon name to add: ")
            print(f"Add {name} to Pokedex") #Replace with function later
        elif choice == "3":
            print('View Pokedex') #Replace with function later
        elif choice == "4":
            name = input("Enter Pokémon name to remove: ")
            print(f'Remove {name} from Pokedex') #Replace with function later
        elif choice == "5":
            print("Exiting Pokédex.")
            break
        else:
            print("Invalid choice. Please try again.")

if __name__ == "__main__":
    main()
```




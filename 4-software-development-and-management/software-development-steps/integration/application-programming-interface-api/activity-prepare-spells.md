---
icon: clipboard-list-check
---

# Activity: Prepare Spells



Example of how to request spell data from a Dungeons and Dragons API, how to store in Pandas and how to plot using Matplotlib. This one is **more difficult** than the others.

Have a look through and consider the comments to see what it does.&#x20;

In short, the program can call the API to display and,search for spells, store specific spells into a dataframe, visualise spell levels based on that dataframe and exit the program. All this is run in a while loop after the API is called and will run until the user selects the exit option.

## Activity: Test

1. Copy the following code into a new VS Code file.

```python
# Import necessary libraries:
import requests  # For making HTTP requests to get data from an API
import pandas as pd  # For data manipulation and analysis
import matplotlib.pyplot as plt  # For visualizing data through charts

# Create an empty DataFrame with specific columns to store spell details
spell_df = pd.DataFrame(columns=['Name', 'Level', 'Index', 'URL'])

# Define a function to display spell information in a readable format
def display_spell(spell_data):
    print(f"Name: {spell_data['name']}")
    print(f"Level: {spell_data['level']}")
    print(f"Index: {spell_data['index']}")
    print(f"URL: {spell_data['url']}")
    print()  

# Define a function to store the selected spell into the DataFrame
def store_spell(spell_data):
    spell_df.loc[len(spell_df)] = {'Name': spell_data['name'], 
                                   'Level': spell_data['level'], 
                                   'Index': spell_data['index'], 
                                   'URL': spell_data['url']}

# Define a function to display all the spells stored so far
def display_stored():
    print('The following are the spells you have searched for so far.')
    spell_df.sort_values(by=['Name', 'Level'], inplace=True) # Sort the DataFrame by spell name and level for easy viewing
    print(spell_df)

# Define a function to visualize the levels of the stored spells
def visualise_level():
    try:
        print('Here is a visual representation of your spell levels: ')
        spell_df.sort_values(by=['Level', 'Name'], inplace=True)  # Sort the DataFrame by level and name to organize the plot

        # Create a bar chart with spell names on the x-axis and levels on the y-axis
        spell_df.plot(
            kind='bar',
            x='Name',
            y='Level',
            color='blue',
            alpha=0.3,
            title='Level of Spells'
        )

        plt.show() #Display the plot
    
    # Catch any error that occurs (such as an empty DataFrame)
    except:
        print('Oops! You need to prepare some spells first!')

# Define the main function that will run the program
def main():
    url = "https://www.dnd5eapi.co/api/spells" # Set the API endpoint URL for fetching D&D 5e spell data
    headers = {'Accept': 'application/json'} # Set headers for the API request

    response = requests.get(url, headers=headers) # Send a GET request to the API to retrieve the spell data

    # Check if the request was successful (status code 200 means OK)
    if response.status_code == 200:
        spells_data = response.json() # Parse the response data as JSON
        spells = spells_data['results'] # Extract the list of spells from the data
        print("Welcome to the D&D 5e Spellbook!")
        print(f"Total Spells: {spells_data['count']}\n")

        # Start an infinite loop to prompt the user for input
        while True:
            print("Commands:")
            print("1 - List all spells")  
            print("2 - Search for a spell by name")  
            print("3 - Display stored spells")  
            print("4 - Visualise Spells")  
            print("5 - Exit")

            # Prompt the user to input their choice
            choice = input("Enter your choice: ")

            # If the user chooses to list all spells
            if choice == '1':
                print("\nList of Spells:")
                # Iterate over all spells and display their details
                for spell in spells:
                    display_spell(spell)
            
            # If the user wants to search for a spell by name
            elif choice == '2':
                spell_name = input("Enter the spell name: ").lower() # Ask the user for a spell name (case-insensitive)
                matching_spells = [spell for spell in spells if spell_name in spell['name'].lower()] # Find all spells that contain the entered name
                print("\nMatching Spells:")

                # Display details of each matching spell
                for spell in matching_spells:
                    display_spell(spell)
                    choice = input('Would you like to prepare the spell? Y/N: ') # Ask the user if they want to store the spell
                    
                    if choice.lower() == 'y':
                        store_spell(spell)
                        print('Spell prepared.')
                    
                    elif choice.lower() == 'n':
                        print('Spell not prepared.')

                    else:
                        print('Invalid option. Spell not stored.')
            
            # If the user wants to display the stored spells
            elif choice == '3':
                display_stored()
            
            # If the user wants to visualize the spell levels
            elif choice == '4':
                visualise_level()
            
            # If the user wants to exit the program
            elif choice == '5':
                print("Goodbye!")
                break  # Exit the loop and end the program
            
            # If the user enters an invalid option
            else:
                print("Invalid choice. Please select a valid option.")

# Check if the script is being run directly (not imported)
if __name__ == "__main__":
    main()
```

2. Open a terminal (Terminal > New Terminal) and type the following:

```bash
pip install pandas requests matplotlib
```

3. **Test the code.**
4. Can you separate this into "main" for User Interface and into "spellbook.py" for functions? This would be a better example of integration and would clean up the code. Give it a try.

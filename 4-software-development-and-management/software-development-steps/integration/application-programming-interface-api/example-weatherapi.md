---
icon: book-open
---

# Example: WeatherAPI

The following program uses the WeatherAPI from weatherapi.com to fetch the current weather data for a given city.

{% embed url="https://www.weatherapi.com/" %}
Free weather API (account required)
{% endembed %}



```python
# Import the requests library to handle HTTP requests
import requests

# API key for WeatherAPI (must be filled in to work)
api_key = ""

# Base URL for WeatherAPI
base_url = "http://api.weatherapi.com/v1"

def fetch_weather(city_name):
    """
    Fetches the current weather data for a given city using WeatherAPI.
    """
    # Construct the complete API request URL
    complete_url = f"{base_url}/current.json?key={api_key}&q={city_name}"

    # Send an HTTP GET request to the API
    response = requests.get(complete_url)

    # Check if the request was successful (status code 200)
    if response.status_code == 200:
        # Return the JSON response as a Python dictionary
        return response.json()
    else:
        # Return None if there was an error with the request
        return None
    
def display_weather_info(weather_data):
    """
    Displays weather information from the API response.
    """
    if weather_data:
        # Extract relevant data from the API response
        location = weather_data["location"]["name"]  # City name
        region = weather_data["location"]["region"]  # Region/State
        country = weather_data["location"]["country"]  # Country
        temperature = weather_data["current"]["temp_c"]  # Temperature in Celsius
        condition = weather_data["current"]["condition"]["text"]  # Weather condition (e.g., Sunny, Rainy)

        # Print the weather details
        print(f"Weather in {location}, {region}, {country}:")
        print(f"Temperature: {temperature}°C")
        print(f"Condition: {condition}")
    else:
        # Print an error message if data could not be retrieved
        print("Error retrieving weather data.")

def main():
    """
    Main function to fetch and display weather information.
    """
    city_name = "Gosford"  # Example city, change as needed

    # Fetch weather data for the given city
    weather_data = fetch_weather(city_name)

    # Display the retrieved weather information
    display_weather_info(weather_data)

# Run the script
if __name__ == "__main__":
    main()
```

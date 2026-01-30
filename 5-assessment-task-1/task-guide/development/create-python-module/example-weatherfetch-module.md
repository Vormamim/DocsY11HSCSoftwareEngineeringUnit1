---
icon: book-open
---

# Example: WeatherFetch Module

This is some starter code which you could use if you want to use the WeatherAPI. You will need to sign up at [https://www.weatherapi.com/](https://www.weatherapi.com/) to get your API Key.

{% hint style="warning" %}
## API Key

Some APIs do not keep their API public and you will need to go on their website and sign up to receive a unique API key.&#x20;

Make sure you replace `"DEMO_KEY"` with a real key from the WeatherAPI in the **`API_KEY`** variable.&#x20;
{% endhint %}

<pre class="language-python" data-title="weatherfetch.py"><code class="lang-python"><strong># Import the requests library to handle HTTP requests
</strong>import requests

# API key for WeatherAPI (must be filled in to work)
api_key = "YOUR_KEY"

# Base URL for WeatherAPI
base_url = "http://api.weatherapi.com/v1"

def fetch_weather(city_name):
    """
    Fetches the current weather data for a given city using WeatherAPI.
    """
    # Construct the complete API request URL
    complete_url = f"{base_url}/current.json?key={api_key}&#x26;q={city_name}"

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

#&#x3C;--------------------------------------------TEST THE FUNCTIONS-------------------------------------------->
</code></pre>

## Testing the Above

```python
#<--------------------------------------------TEST THE FUNCTIONS-------------------------------------------->
city_name = "Gosford"  # Example city, change as needed

# Fetch weather data for the given city
weather_data = fetch_weather(city_name)

# Display the retrieved weather information
display_weather_info(weather_data)
```

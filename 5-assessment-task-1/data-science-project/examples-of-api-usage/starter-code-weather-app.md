---
icon: book-open
---

# Starter Code: Weather App

### **Weather App**

Develop a program that uses the **WeatherAPI** ([www.weatherapi.com](http://www.weatherapi.com)) to track and compare weather data. It should allow users to:

* **Fetch today’s weather** for a given location.
* **Store past weather data** using CSV files or local storage.
* **Compare weather data** from the same date in previous years.
* **Visualize trends** using charts or graphs.

```python
import requests
import csv

# API Base URL (requires a free API key from WeatherAPI)
API_KEY = "YOUR_API_KEY_HERE"
API_URL = "http://api.weatherapi.com/v1/current.json"

def get_weather(city):
    """Fetch current weather data for a given city."""
    response = requests.get(f"{API_URL}?key={API_KEY}&q={city}")
    if response.status_code == 200:
        data = response.json()
        print(f"Weather in {city}: {data['current']['temp_c']}°C, {data['current']['condition']['text']}")
        return data
    else:
        print("Error retrieving weather data.")
        return None

def load_historical_data(filename):
    """Load historical weather data from a CSV file."""
    historical_data = []
    try:
        with open(filename, newline='') as csvfile:
            reader = csv.DictReader(csvfile)
            for row in reader:
                historical_data.append(row)
    except FileNotFoundError:
        print("No historical data found.")
    return historical_data

get_weather("New York")
historical_weather = load_historical_data("weather_history.csv")

```


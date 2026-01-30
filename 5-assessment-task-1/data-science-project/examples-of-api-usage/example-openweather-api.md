---
icon: book-open
---

# Example: OpenWeather API

The following Python program open\_weather.py uses the OpenWeather API to tell the user current weather information.&#x20;

The beauty of using this is that OpenWeather frequently update their data so you do not need to constantly be downloading datasets and reimporting them.

**However,** please note you **MUST** get your own **API\_KEY** from the Open Weather Map website for this to work, and replace that in the code.&#x20;

{% hint style="warning" %}
**Unfortunately,** since this program was written in 2024, the API has been subscription walled. Whilst most API calls are free, a subscription is required :''(&#x20;
{% endhint %}





<pre class="language-python" data-full-width="true"><code class="lang-python"><strong>import requests
</strong>import json

# API Key for OpenWeatherMap
# Please note: You must go to openweather map and get you own API key.
<a data-footnote-ref href="#user-content-fn-1">api_key = '' # &#x3C;-- replace with your API key</a>

# Function to get current weather conditions and 5-day forecast
def get_weather(location): 
    # API endpoint for current weather
    current_weather_url = f'http://api.openweathermap.org/data/2.5/weather?q={location}&#x26;appid={api_key}&#x26;units=metric'
    # API endpoint for 5-day forecast
    forecast_url = f'http://api.openweathermap.org/data/2.5/forecast?q={location}&#x26;appid={api_key}&#x26;units=metric'

    # Make GET request to API
    current_weather_response = requests.get(current_weather_url)
    forecast_response = requests.get(forecast_url)

    # Parse JSON response
    current_weather_data = json.loads(current_weather_response.text) # &#x3C;-- convert JSON response to Python dictionary
    forecast_data = json.loads(forecast_response.text) # &#x3C;-- convert JSON response to Python dictionary

    # Extract current weather conditions
    current_temp = current_weather_data['main']['temp'] # &#x3C;-- extract temperature from dictionary
    current_weather = current_weather_data['weather'][0]['description'] # &#x3C;-- extract weather description from dictionary

    # Extract forecast for next 5 days
    forecast_list = forecast_data['list'] # &#x3C;-- extract list of forecasts from dictionary
    forecast = {} # &#x3C;-- create empty dictionary to store forecast
    for f in forecast_list: # &#x3C;-- loop through list of forecasts
        date = f['dt_txt'][:10] # &#x3C;-- extract date from forecast
        if date not in forecast: # &#x3C;-- check if date is already in forecast dictionary
            forecast[date] = { # 
                'temp': f['main']['temp'],
                'weather': f['weather'][0]['description'] # 
            }

    return current_temp, current_weather, forecast # &#x3C;-- return current weather conditions and 5-day forecast

# Get weather for a location
location = input("Enter a location: ") # &#x3C;-- get location from user
current_temp, current_weather, forecast = get_weather(location) # &#x3C;-- call get_weather function

# Print current weather conditions
print(f'Current temperature in {location}: {current_temp}') # &#x3C;-- print current temperature
print(f'Current weather in {location}: {current_weather}') # &#x3C;-- print current weather

# Print forecast for next 5 days
print("\n5-day forecast:") # &#x3C;-- print header
for date, weather in forecast.items(): # &#x3C;-- loop through forecast dictionary
    print(f'{date}: Temperature: {weather["temp"]}, Weather: {weather["weather"]}') # &#x3C;-- print date, temperature, and weather
</code></pre>



[^1]: You need to grab your own API key here!

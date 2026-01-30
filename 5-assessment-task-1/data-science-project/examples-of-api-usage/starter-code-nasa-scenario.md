---
icon: book-open
---

# Starter Code: NASA Scenario

### **Space Explorer**

Develop a program that retrieves and stores space-related data using the **NASA API** (api.nasa.gov). It should allow users to:

* **Fetch today's Astronomy Picture of the Day (APOD)** and display its description.
* **Retrieve data on planets and celestial bodies** from NASA's planetary API.
* **Store favorite celestial objects** in a local collection.
* **Compare characteristics** of stored celestial objects (e.g., size, distance from Earth).

```python
import requests

# NASA API Base URL
APOD_URL = "https://api.nasa.gov/planetary/apod"
API_KEY = "DEMO_KEY"  # Replace with your own API key from https://api.nasa.gov/

# Dictionary to store favorite celestial objects
favorites = {}

def get_apod():
    """Fetch NASA's Astronomy Picture of the Day (APOD)."""
    params = {"api_key": API_KEY}
    response = requests.get(APOD_URL, params=params)
    if response.status_code == 200:
        data = response.json()
        return {
            "title": data["title"],
            "date": data["date"],
            "explanation": data["explanation"],
            "image_url": data["url"]
        }
    else:
        print("Failed to fetch APOD.")
        return None

def add_favorite(name, details):
    """Store a celestial object in the favorites collection."""
    favorites[name] = details

```


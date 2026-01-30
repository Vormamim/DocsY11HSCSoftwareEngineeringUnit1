---
icon: book-open
---

# Installation

We're on the home stretch! Your program works and you just need to finish up a little documentation to make sure people can use it!

For installation, all we're going to include in this project is a **requirements.txt file** to assist users in installing dependencies and a **README.md file** to give users instructions necessary to run our software.

<details>

<summary>requirements.txt</summary>

If we are using any external Python modules not created by us (requests, pandas, matplotlib, numpy, etc), we need to make it easy for users to install them. To do this, we literally just store the names in a file in our Git Repository.

The following is an example for a program which requires **matplotlib** and **requests.** Make sure when you make yours, save it as **`requirements.txt`**

{% code title="requirements.txt" %}
```
matplotlib
requests
```
{% endcode %}

Users will then need to install these modules by writing the following into their terminal:

```bash
pip install -r requirements.txt
```

{% hint style="info" %}
## **requests Module**

Your program will most definitely require the `requests` library at the very least, as you need this module to make API calls.&#x20;
{% endhint %}

</details>

<details>

<summary>README.md</summary>

Here is an example for a weather program:

````markdown
# Weather Program

This Python program allows you to retrieve weather information from an external API. The program uses the `requests` library to fetch real-time weather data and `matplotlib` to visualise the weather conditions in a graphical format.

## Features
- Fetch weather data based on the user's location or a specified city.
- Display current weather conditions, including temperature, humidity, and weather description.
- Visualise weather data using a bar chart (e.g., temperature, humidity).

## Requirements
To run this program, you need to install the following dependencies:

- `matplotlib` for data visualisation.
- `requests` to make HTTP requests to the weather API.

### Install dependencies
To install the required dependencies, you can run:

```bash
pip install -r requirements.txt
````



</details>

{% hint style="warning" %}
## PROJECT\_DEVELOPMENT.md

Add a code block for each of these files into your project documentation and add under the heading _**Installation.**_&#x20;
{% endhint %}




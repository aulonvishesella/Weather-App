# Simple Weather Application 🌤️

# Before you get started ⏸️
* Get your free API key from the OpenWeatherMap website. Must create an account in order to do so.


# About 💻
A simple weather application that allows the user to check the weather forecast for a given city.

# What I learnt 🚀
* Python GUI development using `Tkinter`.
* Using `requests.get()` to get data from the OpenWeather API.
* Using `response.json()` used to access weather data in a JSON serialized format
* Formatting JSON objects extracted and displaying it on the UI 
 
 ```
 def format_response(weather_json):
    try:
        #format response to show name, temperature, description
        city = weather_json['name']
        conditions = weather_json['weather'][0]['description']
        temp = math.floor((weather_json['main']['temp']-32) * (5/9))
        final_str = 'City: %s \nConditions: %s \nTemperature (°C): %s' % (city, conditions, temp)
    except:
        final_str = 'There was a problem retrieving that information'
    return final_str
```



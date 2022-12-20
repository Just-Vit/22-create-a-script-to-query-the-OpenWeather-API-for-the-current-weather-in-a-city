# 22-create-a-script-to-query-the-OpenWeather-API-for-the-current-weather-in-a-city

Step 2 — Creating the City Weather Program

First, create and open a Python file called weather_bot.py with your preferred editor:

    nano w_1_api_good.py

Next, you’ll create a function to get the current weather in a city from the OpenWeather API. 

Let's review the code at your w_1_api_good.py file:

First, you import the requests library, so you are able to work with and make HTTP requests. Make sure to replace your_api_key with your own API key. The next line begins the definition of the function get_weather() to retrieve the weather of the specified city.

In this function, you construct the URL for the OpenWeather API. This URL returns the weather information (temperature, weather description, humidity, and so on) of the city and provides the result in JSON format. After that, you make a GET request to the API endpoint, store the result in a response variable, and then convert the response to a Python dictionary for easier access.

On the next line, you extract just the weather description into a weather variable and then ensure that the status code of the API response is 200 (meaning there were no issues with the request). Finally, you return the weather description.

If there is an issue with the request, the status code is printed out to the console, and you return None.

To test the script, call the get_weather() function with a city of your choice (for example, London) and print the result. Add the highlighted code following your function:

    weather1 = get_weather("London")
    print(weather1)

*****

To run your just created API request file, first activate your environment as shown in the previous repo:

    source my_env_weather/bin/activate

then run it with

    python w_1_api_good.py

you should have something look like:

    ┌──(my_env_weather)─(user㉿acer)-[~]
    └─$ python w_1_api_good.py            
    scattered clouds

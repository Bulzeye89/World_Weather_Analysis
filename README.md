# World_Weather_Analysis

## Overview 
### Background
PlanMyTrip is a travel advisory company that is looking to create an app that users can input preferred weathher for vacation spots and they will be presented a list of destinations with relevant weather data and hotel information.  They would like to beta test this process as well as add on a new feature allowing users to select up to four cities to create an travel itinerary and a travel route will be automatically generated.  

### Resources
-Data Source: [Weather_Database.csv](https://github.com/Bulzeye89/World_Weather_Analysis/blob/main/Weather_Database/Weather_Database.csv), [WeatherPy_vacation.csv](https://github.com/Bulzeye89/World_Weather_Analysis/blob/main/Vacation_Search/WeatherPy_vacation.csv)<br>
-Software: Python 3.7.11, Anaconda 4.12.0, JupyterLab 3.3.2

## Process
To generate possible cities for travel destinations, numpy's random feature was used to generate longitude and latitude sets.  From here, citipy was used to find the closest city to each set of coordinates.  The next step was to use an API call to OpenWeathermap to obtain the below info for each city in our data set which allowed a dataframe to be created.  
- City title
- City Country
- Latitude and Longitude
- Percent Humidity
- Percent Cloudienss
- Wind Speed
- Current Weather Description

<br>

At this point, beta testers would be able to input minimum and maximum temperature preferences and based on their inputs, a map would be generated with potential cities.  Using a Google Maps and Places Api call, this map would have hotel information as well as weather information for each city that was within the parameters of the user's temperature preferences.  



<p float="left">
<img src="https://github.com/Bulzeye89/World_Weather_Analysis/blob/main/Vacation_Search/WeatherPy_vacation_map.png" 
</p>  



Lastly, users would be able to create a travel itinerary by selecting 4 different cities and have a travel route created for them with the use of Google Maps Directions API.  This would be limited to cities that have a driving, biking, or walking route; otherwise users would just receive travel routes not available message.  An example below of a travel itinerary for the southeast United States that was created for testing can be seen below.  
  
<p float="left">
<img src="https://github.com/Bulzeye89/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map.png" 
</p>  

  
  

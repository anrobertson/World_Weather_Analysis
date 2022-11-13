# World_Weather_Analysis

## Overview of Analysis
My project for this week required me to enhance the PlnaMyTrip app that we acquired weather description data for. The modification will allow users to select citites and creaate a list of potential hotels to stay at and a travel route between them!

### Retrieving the Weather Data
The project called to retrieve the weather data description of each city. I imported the initial libraries to our workbook and used the np.random.uniform to generate a set of 2,000 random latitudes and longitudes. I then retrieved the nearest city for each latitude and longitude pairing by using the for loop and found 717 cities available to choose from.

I imported the API key and retrieved the latitude, longitude, max temp., percentage of humidity, percentage of cloudiness, wind speed and the data description. After calling for the information, I had 660 cities to choose from. I exported that file into a WeatherPy_Database.csv and brought that over into the Vacation_Search notebook.

### Creating a Customer Travel Destinations Map
I placed a float() input code for the custumor to be able to input the desired minimum temperature and the maximum temperature and created a new data frame and then dropped the NaNs from that data frame. It was then time to add another column which I labled "Hotel Name" and used the key "lodging" to pull hotels from the cities I gathered.

After cleaning that data frame with the dropna(), I was able to take that information and create another csv file to bring into the final notebook.

### Create a Travel Itinerary Map

The final step was to create the travel itinerary map. I imported the csv file and created a marker layer for the map. To run the test I picked four different cities that were close by to each other and used the .to_numpy to gather the latitude-longitude pairs as tuples and created a data frame for each city.

I then utilized the gmaps documentation to create routes to each hotel selected. To do this I had my starting point, end point, the waypoints (stops in between) and the way of transportation (I selected driving).

After seeing the results, I made a new data frame by combining the four that created this itinerary to show the map with only the four cities selected.

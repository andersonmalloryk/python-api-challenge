# python-api-challenge
This is the fifth homework for the University of Minnesota Data Visualization and Analytics Boot Camp using python.

In this challenge I had to generate a city list using a set of randomly generated latitude and longitudes to complete a weather database to find an ideal location for a vacation. 

# WeatherPy
The first step was the weather analysis. 
After pulling the random list of cities an API call was made to Open Wather Map to pull the temperature, maximum temperature, humidity, cloudiness, wind speed, country, and date of the pull. The units were set to imperial to pull farenheit. 
A try and exception was put into the code as some cities may not come up within Open Weather Map. These were skipped, otherwise the data was pulled and then converted into a dataframe and saved to a csv. 
For the rest of the weather analysis the analysis calls upon the csv to avoid exceeding API call limits and save time.
A summary table of the overall weather metrics downloaded was generated and then the list was checked for any items that had a humidity of over 100. Since there were none the whole list was used.
A series of scatter plots were generated followed by the dataset being split into the northern hemisphere and the southern hemisphere to check the correlation between latitude and weather attributes: wind speed, cloudiness, etc. 

# VacationPy
The second step was selecting cities with the perfect weather conditions and finding hotels. 
First the weather data was cleaned and set to the correct data types. Then the weather data was filtered to remove any cities without the ideal weather conditions. This resulted in a much smaller list of cities. Then hotels were found using an API call with google places nearby search. Paramaters were set for the search, and hotels were pulled for the cities. The final step was to take those hotels and place them on a map to see the options. Markers were put on the map with an overlay of the most humid areas within each country. Now we can pick a vacation spot! 

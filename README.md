# Final-Project-Statistical-Modelling-with-Python

## Project/Goals

> In my opinion, the Project goals are practice and demonstrate Python skills we 
learned so far. Ability to work with APIs and generate visual presentation of results, 
as well as building regression models. 

## Process
### Connecting to CityBikes API

> I started with checking the Citybikes web site. Then I searched in Google "Citybikes API"
 to explore "CityBikes API Documentation" and got link http://api.citybik.es/v2/. In 
 "CityBikes API Documentation" I checked for endpoints and found "networks" endpoint. 
 Then I checked the "http://api.citybik.es/v2/networks" and found all the information 
 including countries and cities where Citybikes operates. The next step was choosing city 
 and I picked Almaty, the city from Kazakhstan. Almaty is the city I was born :). 
 I found city ID, which is "almatybike". Next step was to create function in Python, 
 I did it by using JupiterLab. In "CityBikes API Documentation" I found that the system 
 supports only JSON. To access the JSON data, I used the requests library to make HTTP requests.
 
> Then I created function "get_bike_data_for_city" function to get all information 
about stations in Almaty city

> The next exercise was to create function giving us information about name of the station, 
latitude, longitude and available bikes

> The result shows us information about all stations in Almaty

> The last exercise of the Part_1 was to parse the JSON object into a Pandas dataframe

> The result shows us the table with 179 rows x 4 columns (Station Name','Latitude',
'Longitude' and 'Available Bikes'.


### Connecting to Foursquare and Yelp APIs

> I explored Foursquare website. I have registered and obtained API KEY. I created 
Environment Variable in my System, to avoid using actual KEY in my function. 
I have found that in Foursquare website you can set parameters, choose language and get code. 
There are 2 different options https://location.foursquare.com/developer/reference/place-search 
& https://location.foursquare.com/developer/recipes/place-search-using-latlong. I chose 
2nd option (shown below). I decided to check Bars near one of the Bike stations. 
I set radius as 1000 meters.

> The result shows all the details of bars in that location

> Then created a DataFrame for Foursquare result

> The same approach I used in YELP website. I have registered and obtained API KEY. 
I created Environment Variable in my System, to avoid using actual KEY in my function.

> Unfortunately, the Yelp Api has no information the location I chose and checked 
with Foursquare API. I didn’t feel that I need to change city. 

> Even the Yelp API did not provide me any information for the chosen location, I wrote 
the below function with DataFrame, so it can be used for another location, where Yelp API 
has information.

> Comparing Results: Since Yelp did not provide any results to me, I checked ratings in 
Foursquare and found that Rating information is missing.

### Joining Data

> To join Part 1 and Part 2 dataframes, you can use the merge function in Pandas. 
The common columns between both dataframes are the latitude and longitude values. 
We'll use these columns as the keys to perform the merge.

> Put all your results in an SQLite3 database

### Building a Model

> Build a regression model using Python’s `statsmodels` module that demonstrates 
a relationship between the number of bikes in a particular location and the characteristics 
of the POIs in that location

> Since I didn't have enough time to create databse with all the details and build a proper 
regression model, I believe that results are not accurate. 

## Results

> Based on the provided results, it seems that your regression model has achieved 
a perfect fit to the data, resulting in an R-squared value of 1.0, which indicates that
the model perfectly explains the variance in the target variable. The mean squared error 
(MSE) is extremely close to zero, which further indicates that the model's predictions are 
almost identical to the actual target values. 

>The coefficients of the model are very close to zero, and the intercept is also very 
close to zero. This suggests that the model has found an exact relationship between the 
features and the target variable in the data.

## Challenges 

> In my opinion, the biggest challenges  are time and of course the knowledge of the Python itself.

> Firstly, I spent a lot of time on understanding the of all 3 APIs, how I can use it to retrieve required data. 

> Secondly, to create Python functions, which can be used for different variables, like cities, POIs, etc. 

> Another challenge I faced was the fact that APIs does not necessary have required data, but I decided to 
stick to chosen city. The negative result is also result

> Due to time restriction, I did not explored data using data visualization in proper way. 
Also, I wasn’t able to created a proper sqlite3 databases, hence faced issues with building 
a regression model. 

## Future Goals

> If I have more time, I would study more about data visualization and building a regression model topics. 
I would also test my functions on other cities and POIs. 

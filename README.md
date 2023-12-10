# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
The goal of this project is to see if we can infer any sort of trends between the number of bikes in a chosen location (Montreal) and the points of interest in said location.

## Process
Step 1: Connecting to the CityBikes API in order to retrieve the bike station name, the latitude, the longitude and the number of bikes in Montreal.

Step 2: Connecting to Foursquare API in order to retrieve information about restaurants and bars for each bike station in Montreal.

Step 3: Connecting to Yelp API in order to retrieve similar information about restaurants and bars for each bike station in Montreal.

Step 4: Joining all the data from the previous steps into a new DataFrama in order to compare the data.

Step 5: Providing a visualization used as part of the EDA process.

Step 6: Creating an SQLite database to store the collected data.

Step 7: Building a regression model to explain the relationship between number of bikes and the points of interest in Montreal and interpreting the results and findings.

## Results
Comparing the two APIs, my dataset seems to have better data coverage with Yelp since many ratings under the Foursquare API appeared to be null whereas Yelp did not have any null values.

The final model has an Adj. R-Squared value of 0.7%, which is not a good model fit. I ended up only removing two variables out of the five that I originally included and removed the variables with the highest p-value.
If I kept going, I would have to remove all the variables so I just kept it at three variables.

The linear regression model equation is as follows:
(Number of Bikes) = 4.88 + 18.32*(Average_popularity_F) - 3.11*(Average_rating_Y) + 0.03*(Average_review_count_Y)

## Challenges 
At first, I struggled a bit with the API requests since there was a daily limit, but after doing an AR, I ended up using a small sample to test out if my code works (with the head() giving me the first 5 rows). This saved me a lot of time.

The automatic limit of data/reviews for each location was small (either 10 or 20) so I changed the limit to 50 in order to gather as much data possible to work with.

## Future Goals
If I had more time to work on this project, I definitely would've gone through everything more closely and try to get a better understanding of why I didn't end up with a good model fit and look into other variables for the modelling.

I would also attempt to make a classification model.

If I wanted to make this a long-term goal, I could check if there's a difference in seasons that affect the result. Since, right now, it is winter time so many people aren't using the Bixi bikes and I would probably have a better read with any other season.

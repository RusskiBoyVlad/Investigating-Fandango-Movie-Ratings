# Investigating-Fandango-Movie-Ratings
This project is investigating the claim proposed in this fivethirtyeight blog https://fivethirtyeight.com/features/fandango-movies-ratings/

Scenario:
Fandango the movie review site is inflating their movie rating by round them up to the nearest whole number and thus appears to have the highest average rating out of all the movie rating websites
![image](https://user-images.githubusercontent.com/85899536/219857210-d2395613-77df-43a7-92ba-0ca244340085.png)

As an example, Ted 2 has a 4.1 RatingValue in the html script

![image](https://user-images.githubusercontent.com/85899536/219857232-a9e4aefa-2128-4bb0-a2b5-94556e008e41.png)

but displays 4.5 as it round the 4.1 to 4.5 and not 4.0 as one would expect

![image](https://user-images.githubusercontent.com/85899536/219857238-ff7f332e-5e3a-48c1-8c9c-d2578cc2d098.png)

After being accused of this error, Fandango promised to fix their rating system which they claimed was a bug

My work:
My hypothesis is that after fixing their movie rating now round to the nearest 0.5/.0 rating and thus results would skew to the left (lower mean, median, mode) compared to 2015. We will show this to our non-technical stakeholder/user by making a kernel density plot to visualise the difference between the 2015 and 2016-2016 datasets that we will be comparing.

2015 data: https://github.com/fivethirtyeight/data/tree/master/fandango shape: (146,22)

2016-2017 data: https://github.com/mircealex/Movie_ratings_2016_17 shape: (214,15)


1. Cleaning data (>30, separating by year)
2. Plotting 

![image](https://user-images.githubusercontent.com/85899536/219857647-a94c243f-6ef2-4c58-99ec-6561b3084862.png)

2.1 Visualising the 3Ms

![image](https://user-images.githubusercontent.com/85899536/219857714-cc832e77-a2af-4e80-809e-054150e3bf5a.png)

Conclusion:

Our analysis showed that there is indeed a slight difference between Fandango's ratings for popular movies in 2015 and Fandango's ratings for popular movies in 2016. We also determined that, on average, popular movies released in 2016 were rated lower on Fandango than popular movies released in 2015.

We cannot be completely sure what caused the change, but the chances are very high that it was caused by Fandango fixing the biased rating system following Hickey's analysis.

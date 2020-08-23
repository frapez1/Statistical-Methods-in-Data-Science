# Project

My project concerns the prediction, by means of Bayesian inference methods, of the PM10 levels in the air in the city where there is no such detector, analyzing what happens in nearby cities.

I used a huge [dataset](https://aqicn.org/data-platform/covid19/) with many air quality records from around the world. 

I focused on Italy from the beginning of 2019 up to July 2019.

## Problems with the dataset

Unfortunately the dataset wasn't that good, there were a lot of missing values ​​and a lot of duplicate days. The last problem was easy to tackle, but for the first one I chose to use a Bayesian approach instead of the classic "replace all NAs with the mean".

The approach was simple: estimate, with the Metropolis Hasting algorithm, the missing values ​​on the basis of those given.

## Meaning of the high correlation between cities

As you can see, within the html, the correlation of pm10 between cities is really high, this is due to the fact that even if the cities are very far away, the daily style of people is the same: on Sundays many people stay at home, on Mondays many people take the car... You can see this cyclic behavior in the autocorrelation graph.
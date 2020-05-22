# Analysis of Bay Wheels trip history data
## by Ulrich Schlecht


## Dataset

In this project we will explore trip history data of Bay Wheels for the year 2019. The main goal is to better understand various aspects of frequency and duration of bike rides. Timing of trips (weekday and hour of day) and depndency on user type (subscriber or non-subscriber) will be explored.

The raw data were downloaded from https://www.lyft.com/bikes/bay-wheels/system-data and include information about ~2.5 million individual rides made in a bike-sharing system covering the greater San Francisco Bay area. Features such as trip duration, month, week day, hour of trip, coordinates of start and end station have been collected for every bike ride and will be explored below.


## Summary of Findings

- The data we will explore here consists of slightly more than 2.5 million entries (i.e. records of individual trips) and multiple columns with information about trip duration, month, week day, hour of trip, distance between start and end station among others.

- One of the features of interest in this dataset is trip duration. Other features that will support the investigation of the main feature are month, week day, and hour of day the trips were made, as well as user type, and distance.

- After log-transformation trip duration looks close to normally distributed. The median trip duration is 571 seconds (close to 10 minutes).

- December had the fewest trips, which makes sense since it tends to be the coldest and rainiest month of the year in the bay area. July and March had the highest number of rides.

- Weekdays have similar number of rides per day (with Tuesday being the most popular day), in contrast bikes are much less used on Saturdays and Sundays.

- We observe a bimodal distribution with bikes being used most during peak morning (8 am) and evening (5 pm) rush hours. Very little use is observed during night between midnight and 5 am.

- Trip distance close to normally distributed. The median trip distance is 1486 meters (close to 1.5 km or 1 mile).

- There are 4 times more subscribers (\~80%) than non-subscribers (~20%).

- Interestingly, up to a certain distance (approximately 450 meters, marked with the red dashed line) there is a wide spread in trip durations (between 100 and 10000 seconds). Beyond that the minimum time traveled increases with the distance, which makes sense as there is an upper limit for how fast a person can bike.

- People seem to be taking longer bike rides on the weekend: trip duration is about 200 second (~3.5 min) longer on Saturday and Sunday compared to weekdays.

- Trips that non-subscribers do tend to be longer (on average about 10 min) than trips of subscribers.


## Key Insights for Presentation

- During data exploration we've seen that number of trips fluctuate over the course of a day with peak usage at 8 am and 5 pm. We have also seen that bikes are used more frequently during the week than during weekends. Here we want to have a look at the combination of both variables weekday and hour of day in the context of number bike rides. During the week bike rides peak during morning and evening rush hour. In contrast, on the weekend days number of bike rides slowly increase starting at 9 am in the morning and peak in the early afternoon (1 and 2 pm).

- Non-subscribers are taking longer trips than subscribers throughout the week. Both user types take longer trips on the weekends. The variability in trip duration appears to be higher for non-subscribers (indicated by the larger error bars) than for subscribers. 

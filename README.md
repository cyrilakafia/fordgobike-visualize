# Exploration of the Ford GoBike System Data
## Cyril Selase Akafia


## Dataset

The data consists of information regarding 183,412 individual rides made in a bike-sharing system covering the greater San Francisco Bay area. The dataset can be found [here](https://s3.amazonaws.com/fordgobike-data/index.html), with feature documentation available [here](https://www.lyft.com/bikes/bay-wheels/system-data). The dataset has 16 columns. The columns are as follows: 

- `duration_sec`: The duration of the ride in seconds
- `start_time`: The start time of the ride
- `end_time`: The end time of the ride
- `start_station_id`: The ID of the station where the ride started
- `start_station_name`: The name of the station where the ride started
- `start_station_latitude`: The latitude of the station where the ride started
- `start_station_longitude`: The longitude of the station where the ride started
- `end_station_id`: The ID of the station where the ride ended
- `end_station_name`: The name of the station where the ride ended
- `end_station_latitude`: The latitude of the station where the ride ended
- `end_station_longitude`: The longitude of the station where the ride ended
- `bike_id`: The ID of the bike used for the ride
- `user_type`: The type of user (Subscriber or Customer – “Subscriber” = Member or “Customer” = Casual)
- `member_birth_year`: The birth year of the user
- `bike_share_for_all_trip`: Whether the ride was shared with a non-member
- `memeber gender`: The sex of the users


**Wrangling**
* All rows with null values were dropped
* Datatypes of columns were changed to the appropriate types
* Extra features were extracted from the data. These include:
    * `duration_min`: The duration of the ride in minutes
    * `distance`: The distance travelled in the ride in km
    * `age`: The age of the user
    etc.


## Summary of Findings

* The distribution of duration and distance were similar and skewed to the right. Users with a trip distance of 0 km were due to the fact that the start and end station were the same or they did not travel at all.
* Most of the users were male. Males were about 3x the number of females.
* Most of the users did not share bikes for all trips
* The ages of most users were between 25 and 40
* The average trip duration was 12 minutes with majority of the bike rides being below 100 minutes.
* Majority of bike rides were above 10km.
* Users between ages 20 and 60 usually ride the bicycles for longer distance as compare to users above these ages.
* Females usually took longer rides in terms of duration
* Customers usually took longer rides than subscribers in terms of duration and distance


## Key Insights for Presentation

For the presentation, I focus on just the duration and distance of trips and relationship with other features. I start by introducing the duration variable, followed by its distribution and relationship with other features. Afterwards, I introduce the distance variable and visualize its distribution. 

I then find the relationship between my key variables and other features.

- Which user type has the longest trip duration?
On the average customers have the longest trip duration
- Which user type has the longest trip distance?
Customers have the longest trip duration on average
- Which gender has the longest trip duration?
On the average females have the longest trip duration
- Which gender has the longest trip distance?
Again, as expected, females have the longest trip distance

For some insights, box plots were used inplace of clustered bar charts to show the distribution of the data. This was done to show the distribution of the data and outliers.
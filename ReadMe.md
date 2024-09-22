## Data Description

Download both departues data from source airport, and arrival data to destination airport. Store arrival data in the `data/arrivals` directory where filename pattern is `AirlineName_Airlines.csv`. Also please remove the meta data (first 7 lines of the downloaded csv file) from the data file.

### Data Period
Month(s): March, April, and May
Day(s): 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30 and 31
Year(s): 2006, 2007, 2009, 2010, 2011, 2012, 2013, 2014, 2015, 2016, 2017, 2018, 2019, 2022 and 2023

### Source to Destination
MCO - SYR, 
JFK - SYR, 
ORD - SYR

### Airlines

1. American
2. Delta
3. United 
4. SouthWest 
5. JetBlue
6. Endeavor
7. Envoy
8. Mesa
9. PSA
10. Republic
11. Skywest

## Final Data
We build 3 dataset from the raw data

### Heading of dataset-1, which we use to predict the first flight
DATE,DAY,FLIGHT NUMBER,ORIGIN,DEPARTURE TIME,ARRIVAL TIME, AIRLINE_CARRIER_DELAY, AIRLINE_YEARLY_ON_TIME_ARRIVAL_PERCENTAGE, AIRPORT_RANKING_for_on_time_dep, WEATHER_DELAY, ARRIVAL STATUS

### Heading of dataset-2, which we use to predict the second flight, based on previous flight status
DATE,DAY,FLIGHT NUMBER,ORIGIN,DEPARTURE TIME,ARRIVAL TIME, AIRLINE_CARRIER_DELAY, AIRLINE_YEARLY_ON_TIME_ARRIVAL_PERCENTAGE, AIRPORT_RANKING_for_on_time_dep, WEATHER_DELAY, PREVIOUS_FLIGHT_STATUS, ARRIVAL STATUS

### Weather Model, which predicts weather delay value for a flight on dataset-1 and dataset-2
Get weather data for the dates we have in data, also collect weather prediction for the upcoming dates (April 19 to April 22). From the weather data, predict the weather_delay column of dataset-1 and dataset-2

### AIRLINE CARRIER DELAY 
Carrier delay for airline is already there in the arrival data. For the test samples we use median value of carrier delay for the flights in april 2024.

### AIRLINE_YEARLY_ON_TIME_ARRIVAL_PERCENTAGE 
add the yearly on-time percentage data for every airline from the directory `on-time-arrival-ranking-airlines` to the training data. There are data for 2003 to 2023. 
We need to find on-time percentage data for every airlines for 2024, so that we can add those on our qweries.

### AIRPORT_RANKING_for_on_time_dep
Add the yearly on-time departure percentage for three airports (ORD, MCO and JFK) is available in the directory `on-departure-ranking-airport`



# Advanced-Data-Storage-and-Retrieval-Exercise

## Climate Analysis and Exploration
To begin, used Python and SQLAlchemy to do basic climate analysis and data exploration of climate database. All the following analysis was completed using SQLAlchemy ORM queries, Pandas, and Matplotlib.
* Chose a start date and end date for trip. 
*	Used SQLAlchemy create_engine to connect to sqlite database.
*	Used SQLAlchemy automap_base() to reflect tables into classes and saved a reference to those classes called Station and Measurement.

## Precipitation Analysis
*	Designed a query to retrieve the last 12 months of precipitation data.
*	Selected only the date and prcp values.
*	Loaded the query results into a Pandas DataFrame and set the index to the date column.
*	Sorted the DataFrame values by date.
*	Ploted the results using the DataFrame plot method.
*	Used Pandas to print the summary statistics for the precipitation data.

## Station Analysis
* Designed a query to calculate the total number of stations.
* Designed a query to find the most active stations.
    * Listed the stations and observation counts in descending order.
    * Which station has the highest number of observations?
* Designed a query to retrieve the last 12 months of temperature observation data (TOBS).
* Filtered by the station with the highest number of observations.
* Plotted the results as a histogram with bins=12.

## Climate App
* Designed a Flask API based on the queries that I had developed above.
* Used Flask to create routes.

## Temperature Analysis I
Across all the stations, the mean temperatures in June and December temperature in years 2010-2017 differ by 3.9 degrees Fahrenheit. An unpaired t-test was conducted, and with an extremely low p-value, the difference is deemed statistically significant.

## Temperature Analysis II
* Used the calc_temps function to calculate the min, avg, and max temperatures for your trip using the matching dates from the previous year.
* Plotted the min, avg, and max temperature from query as a bar chart.
    * Used the average temperature as the bar height.
    * Used the peak-to-peak (TMAX-TMIN) value as the y error bar (YERR).
![temperature](Images/temperature.png)

## Daily Rainfall Average
* Calculated the rainfall per weather station using the previous year's matching dates.
* Calculated the daily normals. Normals are the averages for the min, avg, and max temperatures.
* Created a list of dates for your trip in the format %m-%d. Used the daily_normals function to calculate the normals for each date string and append the results to a list.
* Loaded the list of daily normals into a Pandas DataFrame and set the index equal to the date.
* Used Pandas to plot an area plot (stacked=False) for the daily normals.
![daily-normals](Images/daily-normals.png)

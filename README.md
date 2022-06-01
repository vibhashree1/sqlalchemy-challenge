# SQL-Alchemy-for-climate-analysis-and-exploration.
Used Python and SQLAlchemy to do basic climate analysis and data exploration of the climate database. All of the following analysis are done using SQLAlchemy ORM queries, Pandas, and Matplotlib.

The following steps were followed to answer all queries:-

Chose a start date and end date for the trip. The vacation range is approximately 3-15 days total.
Used SQLAlchemy create_engine to connect to the sqlite database.
Used SQLAlchemy automap_base() to reflect the tables into classes and save a reference to those classes called Station and Measurement.



PRECIPITATION ANALYSIS


Designed a query to retrieve the last 12 months of precipitation data.
Selected only the date and prcp values.
Loaded the query results into a Pandas DataFrame and set the index to the date column.
Sorted the DataFrame values by date.
Plotted the results using the DataFrame plot method.


Used Pandas to print the summary statistics for the precipitation data.



STATION ANALYSIS


Designed a query to calculate the total number of stations.

Designed a query to find the most active stations.


Listed the stations and observation counts in descending order.
Which station has the highest number of observations?


Designed a query to retrieve the last 12 months of temperature observation data (tobs).


Filtered by the station with the highest number of observations.
Plotted the results as a histogram .


CREATING CLIMATE APP:

Designed a Flask API based on the queries that I have just developed.


Used FLASK to create the routes.

Converted the query results to a Dictionary using date as the key and prcp as the value.
Returned the JSON representation of the dictionary.


Returned a JSON list of stations from the dataset.

Queried for the dates and temperature observations from a year from the last data point.
Returned a JSON list of Temperature Observations (tobs) for the previous year.


Returned a JSON list of the minimum temperature, the average temperature, and the max temperature for a given start or start-end range.
When given the start only, calculated TMIN, TAVG, and TMAX for all dates greater than and equal to the start date.
When given the start and the end date, calculated the TMIN, TAVG, and TMAX for dates between the start and end date inclusive.





















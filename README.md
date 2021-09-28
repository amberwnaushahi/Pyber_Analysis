# Pyber_Analysis

## Overview

The purpose of this analysis is to identify total weekly fare metrics by type of city and understand how they differ by city type, to aid the decision-makers at PyBer while devising future strategy. 

As part of the exercise, a summary DataFrame of the ride-sharing data by city type was created along with a multiple-line graph that show the total weekly fares for each city type.

Data Source: city_data.csv, PyBer_ride_data.csv, ride_data.csv *Software: Python 3.7.10 *Jupyter Notebook## * Matplotlib

## Results

### Total and Average Numbers

The total drivers, total rides and total fares by city type were obtained from the combined dataframes using the groupby function along with the sum and count functions. Subsequently,  the average fare per ride by city type and average fare per driver by city type were calculated. The results were put into a new PyBer dataframe with the following output:

![image](https://github.com/amberwnaushahi/Pyber_Analysis/blob/main/analysis/pyber_summary_df.png)

As shown in the data frame above, the rural cities had the highest average fare per driver and per ride while the urban cities had the lowest. 
The suburban cities fell somewhere in the middle of the two. The total rides, drivers and fares were much lower in absolute terms for rural while urban was the higest. I believe this can be attributed to the lower population in rural areas and/or their preference of using their own vehicles. People in the city/urban centers prefer convenience and find it much easier and cheaper to use ride-sharing than getting around in their own vehicle. Parking costs are also higher in urban centers.  We can see that:

* Urban cities have more than four times drivers than suburban cities.
* Suburban cities have almost six times drivers than rural but only 4.5 times the revenue.
* Rural cities have the highest average fare per ride and driver.
* We can establish a relationship in which average fare revenue per ride is higher by city type when there is a larger ratio of rides to drivers (1.6 for rural, 1.27 for suburban and 0.53 for urban)

### Weekly Analysis

A new dataframe was also created using loc to fitler the data to show the weekly performance over the period 01 January 2019 to 28 April 2019. The data was resampled into weekly bins after resetting the index to datetime data type and sum() was used to get total weekly fares. The result was then plotted onto a multiple line graph as follows:

![image](https://github.com/amberwnaushahi/Pyber_Analysis/blob/main/analysis/PyBer_fare_summary.png)

It can be seen that the urban cities had the highest total fare within the months of January to April 2019 followed by the rural cities while the urban cities had the lowest fare. 

All 3 city types exhibit a similar overall trend over the period of increase between January and April, within fluctuations in between. This could be due to holidays and weekends. 

## Summary

Based on the analysis, several factors can be considered by PyBer while devising future strategy regarding allocation of rides and drivers by city type to improve revenues and profitability:

* Include additional demographic data such as population and age to understand the customer trends in each city type. Fares can be grouped by age and city type to see who are the main users of the service.
* Include analysis from previous years (such as a three year period) to assess trends over a period of time. This can help understand if similar patterns are observed in similar months of the years across the three different city types. 
* Include average length of trip to understand if more drivers need to be allocated. Data for rural cities could indicate that rural area based riders are taking longer trips which could result in a loss in potential revenue when there are peaks in business and drivers are unavailable.



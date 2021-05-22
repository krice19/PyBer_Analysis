# PyBer_Analysis

## Overview of Analysis
The purpose of the new analysis is to provide ride sharing data for Pyber.  My first deliveable is a dataframe summary that shows the data by city type: Urban, Suburban, and Rural.  My  second deliverable is a multi-line chart of the total fares by city type, which was created using Matplotlib.  With this, we can visualize the fares over the course of time (in weeks) for each city type. The information can be used to easily compare and point out fares between the 3 city types.

## Results

In my first deliverble, I have created a summary table that shows the total rides, total drivers, total fares, average fare per ride, and average fare per driver by each city type.  From this summary, it is clear that urban locations have the most total rides, total drivers, and have the highest sum in total fares.  However, the urban locations have the lowest average fare per ride and average fare per driver.  Meanwhile, the rural locations have the lowest amount of total rides, drivers, and sum of fares, but have the highest average fare per ride and average fare per driver.  The suburban locations stay in the middle spot across all categories.<br /> 
<br /> 
My second deliverable is a multiple line chart that shows fares by city time from Jan 2019 to April 2019.  To make this chart, I first created a dataframe grouped by type and date and showed the sum of fares.  After removing the index, I created a pivot table from the this data frame with date as the index, type as the columns, and fares as each value.  From this pivot table, I created a new data frame only using the dates from Jan 1st 2019 to April 29th 2019.  I then set the date indx to the datatime data type and resamples it to only show the week.  Using matplotlin, I created a multi line chart using the following code:<br /> 
<br /> 
fare_by_type = jan_apr_resample.plot(figsize=(20,6))
fare_by_type.set_ylabel("Fare ($USD)")
fare_by_type.set_title("Total Fare by City Type")
from matplotlib import style
style.use('fivethirtyeight')
<br /> 
The resulting chart is below:
![fare_by_type_chall](Analysis/fare_by_type_chall.png)



## Summary
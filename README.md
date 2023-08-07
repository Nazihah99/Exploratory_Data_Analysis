# Exploratory Data Analysis of USA Flight Dataset 2008

## Overview
This project aims to analyze flight delay data to identify trends and patterns in delay durations and cancellations. By refining the dataset to remove outliers and focusing on specific airlines, the analysis provides valuable insights into the frequency and average duration of delays for selected flights. The findings highlight the significance of certain airlines in contributing to overall delay statistics and emphasize the need for targeted strategies to reduce delays and cancellations, resulting in a smoother travel experience for passengers.

## Motivation
Flight delays and cancellations can significantly disrupt travel arrangements and inconvenience passengers. Understanding the factors contributing to delays and cancellations is crucial for the airline industry to implement preventative measures and specific strategies to improve on-time performance and enhance customer satisfaction.

# Methodology
## Apache Pig Analysis
### Approach 1: Flight with the Highest Frequency of Delays
Filter the data to exclude flights that were cancelled using the FILTER function.
Perform aggregation based on flight number and unique carriers using the GROUP BY function.
Utilize the AVG function to determine the average time delay and the COUNT function to determine the number of non-cancelled flights.
Sort the data in descending order to identify the flight with the highest average time delay.
### Approach 2: Flights with the Highest Frequency of Arrival Delays
Filter the data to include only arrival delays greater than zero, excluding flights arriving early or with negative delays.
Perform aggregation based on flight number and unique carriers using the GROUP BY function.
Determine the number of flight delays using the COUNT function.
Sort the results in descending order to identify the flights with the highest frequency of arrival delays.
### Approach 3: Flights with the Highest Frequency of Cancellations
Aggregate the data based on flight number and unique carriers using the GROUP BY function.
Determine the number of flight cancellations using the SUM function.
Sort the results in descending order to identify the flights with the highest frequency of cancellations.

## Python Analysis
The frequency table is imported to Google Colab, and columns are renamed for clarity.
The data is filtered to exclude airlines with a number of flights less than the mean and time delays lower than a specified threshold. This step removes irrelevant observations and focuses on airlines with significant delay times and a higher number of flights.
The percentage of delayed flights is calculated for each airline based on the total number of flights, and the top 20 airlines with the highest percentages are selected.
Bar plots are generated to visualize the average delay and the number of delayed flights for the top 20 airlines, providing insights into their performance in these areas.
The number of cancellations for the top 20 airlines with the most cancellations is identified and plotted. The percentage of cancellations relative to the overall sum of cancellations is calculated.

## Data Refinement
To ensure the reliability of the results, the dataset was refined by selecting flights that had delays greater than the mean delay time (10.819121 minutes) and had been flown more than the mean total number of flights (101 times). This filtering process aimed to remove any bias caused by outlier flights with significantly long delays or occurrences. By focusing on commonly traveled routes with average delay times, a more accurate understanding of overall delay patterns was obtained.

# Results
## Analysis of Top 20 Flights with Longest Delays
After analyzing the filtered data, it was evident that the top 20 flights have an average delay of almost one hour. These flights, which have been operated more than 100 times, experience an average delay of around 10 minutes per flight. Notably, American Airlines (AA) exhibited a rate of flight delays that surpasses the average, consistent with prior studies suggesting higher delays for American Airlines compared to other carriers.

## Concentrated Analysis of Flight Delays
A concentrated analysis was performed by studying the frequency of flight delays among the 20 instances with the greatest total delay durations. This approach helped pinpoint particular flights or routes that make a substantial contribution to overall delay statistics. Southwest Airlines (WN) emerged as the airline responsible for the most flight delays compared to other carriers, indicating the need for targeted actions to alleviate tardiness associated with Southwest Airlines flights.

## Flight Cancellations
Apart from flight delays, the analysis also shed light on flight cancellations, which can significantly disturb travel arrangements. SkyWest Airlines (OO) exhibited the highest cancellation rate among other airlines, underscoring the impact of SkyWest Airlines' cancellations on overall flight disruptions. Understanding and addressing the root causes behind SkyWest Airlines' elevated cancellation rate are crucial in reducing travel disruptions for customers.

# Conclusion
The findings from the flight delay analysis highlight the significance of American Airlines and Southwest Airlines in contributing to delay statistics. The results suggest the need for specific strategies to address delay frequency and duration for these airlines. Additionally, the high cancellation rate of SkyWest Airlines calls for comprehensive measures to mitigate travel disruptions.

By implementing preventative measures and targeted strategies, airlines can work towards reducing delays and cancellations, resulting in a more seamless travel experience for passengers. Understanding the patterns and factors contributing to flight delays and cancellations is essential in improving on-time performance and enhancing overall customer satisfaction in the airline industry.

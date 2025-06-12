# US-Flight-Pattern-Analysis
This project analyzes a large dataset of US commercial flights from 1999 to 2008 . Dataset found: https://dataverse.harvard.edu/citation?persistentId=doi:10.7910/DVN/HG7NV7

The main goals were to:
- Identify the best times and days of the week to minimise flight delays each year.
- Assess whether older planes experience more delays on a year-to-year basis.
- Build logistic regression models predicting the probability of flight diversions using flight attributes such as departure times, airport coordinates, distances, and carriers, and visualize coefficient changes across years.

The project involves extensive data wrangling, cleaning, and statistical modeling using both Python and R. The analysis includes reproducible codes and clear visualizations supporting the findings.

##Finding the best times and days of the week to minimise delays each year
Overview: 
We analysed 10 years of U.S. flight data to identify when flights are least likely to be delayed. Initial analysis highlighted arrival delays as the main contributing factor. After data wrangling, we visualized yearly patterns to see which specific times of day showed the lowest delays. To give a broader view across the entire 10-year period, scheduled arrival times were grouped into four parts of the day (Night, Morning, Afternoon, Evening), and the percentage of delayed flights was calculated for each period. To identify the best days of the week, we summed arrival and departure delays, then aggregated the data to find average delays per day. Days of the week were mapped, and a final visualisation was created for indiviual years. Finally we repeat the steps but across the whole 10 year period using a heatmap comparing with the individual delay variables and the combined delay vairable across the days of the week. Detailed methodology and calculations are documented in the code. 
Key Insights:
Best Time of Day: While Night flights showed the lowest delays in several individual years, when aggregated across all 10 years, Morning flights had the lowest overall delay percentage. This suggests that the best time to fly differs in short-term trends or long-term patterns. 
Best Day of the Week: Both individual year plots and the 10-year summary indicate that Saturday consistently has the lowest average flight delays. 
How to Run: 
All relevant packages are loaded, and the analysis is fully implemented in both Python and R. Each code chunk includes detailed explanations to guide you through the steps — from data cleaning and wrangling to visualisation and insights. To replicate the analysis, simply follow the code chunks in order within your R or Python environment, ensuring the dataset files are correctly loaded.

##Do older planes suffer more delays on a year-to-year basis
Overview: 
We defined a threshold to classify planes as either younger or older. Using this classification, we calculated the average total delay (Arrival + Departure) and plotted the results for individual years. To analyse the full 10-year dataset efficiently, we split the period into two halves (first 5 years and last 5 years), repeating the same steps.
Key Insights: 
There's little to no difference between younger and older in both yearly and aggregated visualisations. On average, younger planes do experience more delays - by 1%, which is likely insignificant
How to run:
All relevant packages are loaded, and the analysis is fully implemented in both Python and R. Each code chunk includes detailed explanations to guide you through the steps — from data cleaning and wrangling to visualization and insights. To replicate the analysis, simply follow the code chunks in order within your R or Python environment, ensuring the dataset files are correctly loaded.


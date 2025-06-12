# US-Flight-Pattern-Analysis
This project analyzes a large dataset of US commercial flights from 1999 to 2008 . Dataset found: https://dataverse.harvard.edu/citation?persistentId=doi:10.7910/DVN/HG7NV7

The main goals were to:
- Identify the best times and days of the week to minimise flight delays each year.
- Assess whether older planes experience more delays on a year-to-year basis.
- Build logistic regression models predicting the probability of flight diversions using flight attributes such as departure times, airport coordinates, distances, and carriers, and visualize coefficient changes across years.
- Demonstrate that all data wrangling and analysis steps can be replicated in both Python and R.

The project involves extensive data wrangling, cleaning, and statistical modeling using both Python and R. The analysis includes reproducible codes and clear visualizations supporting the findings.

THE FOLLOWING OVERVIEW IS JUST A SHORT SUMMARY OF THE DATA ANALYSIS AND WRANGLING PROCESS FOR MORE DETAILED METHODOLOY READ THE PYTHON AND R CODES/ FILES. 

## Finding the best times and days of the week to minimise delays each year
Overview: 
We analysed 10 years of U.S. flight data to identify when flights are least likely to be delayed. Initial analysis highlighted arrival delays as the main contributing factor. After data wrangling, we visualized yearly patterns to see which specific times of day showed the lowest delays. To give a broader view across the entire 10-year period, scheduled arrival times were grouped into four parts of the day (Night, Morning, Afternoon, Evening), and the percentage of delayed flights was calculated for each period. To identify the best days of the week, we summed arrival and departure delays, then aggregated the data to find average delays per day. Days of the week were mapped, and a final visualisation was created for indiviual years. Finally we repeat the steps but across the whole 10 year period using a heatmap comparing with the individual delay variables and the combined delay vairable across the days of the week. 

Key Insights:
Best Time of Day: While Night flights showed the lowest delays in several individual years, when aggregated across all 10 years, Morning flights had the lowest overall delay percentage. This suggests that the best time to fly differs in short-term trends or long-term patterns. 
Best Day of the Week: Both individual year plots and the 10-year summary indicate that Saturday consistently has the lowest average flight delays. 

How to Run: 
All relevant packages are loaded, and the analysis is fully implemented in both Python and R. Each code chunk includes detailed explanations to guide you through the steps — from data cleaning and wrangling to visualisation and insights. To replicate the analysis, simply follow the code chunks in order within your R or Python environment, ensuring the dataset files are correctly loaded.

## Do older planes suffer more delays on a year-to-year basis
Overview: 
We defined a threshold to classify planes as either younger or older. Using this classification, we calculated the average total delay (Arrival + Departure) and plotted the results for individual years. To analyse the full 10-year dataset efficiently, we split the period into two halves (first 5 years and last 5 years), repeating the same steps.

Key Insights: 
There's little to no difference between younger and older in both yearly and aggregated visualisations. On average, younger planes do experience more delays - by 1%, which is likely insignificant

How to run:
All relevant packages are loaded, and the analysis is fully implemented in both Python and R. Each code chunk includes detailed explanations to guide you through the steps — from data cleaning and wrangling to visualization and insights. To replicate the analysis, simply follow the code chunks in order within your R or Python environment, ensuring the dataset files are correctly loaded.


## Fitting a logistic regression model for the probability of diverted US flights using as many features as possible
Overview: 
We loaded 2 extra dataset named carriers,csv and airports.csv and merge them into every individual year. After extra data wrangling, we create a new column containing coordinates. 
Next, we separate the variables into 2 groups - numerical and categorical and plot the regression model with AUC score and its respective coefficients for each group. Repeat this step for each year 
Then to show across 10-year we first split into first 5 year and last 5 year. the 2 extra dataset loaded will then be merged into this 2 big time periods but the data wrangling and plotting will remain the same. 

Key insights: 
Logistic models using numerical variables consistently achieved higher AUC scores than those using categorical variables, indicating better classification performance.
Numeric coefficients were generally positive in both R and Python, showing a similar directional influence on flight diversion likelihood.
However, categorical coefficients differed more significantly: Python showed mostly positive relationships, while R showed mostly inverse relationships. However, some similarities in key variables were still observed across both platforms. 

How to Run: 
All relevant packages are loaded, and the analysis is fully implemented in both Python and R. Each code chunk includes detailed explanations to guide you through the steps — from data cleaning and wrangling to visualisation and insights. To replicate the analysis, simply follow the code chunks in order within your R or Python environment, ensuring the dataset files are correctly loaded.


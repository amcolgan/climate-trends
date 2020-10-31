# climate-trends
This repository includes all code needed to carry out analysis of climate trends at Pinkham Notch and Mount Washington and to create figures for publication. 

**R CODE**

**monthly_temp_trends.Rmd** 
The purpose of this code is to calculate the mean monthly average, minimum, and maximum temperatures for Pinkham Notch and the Summit of Mount Washington and to analyze the trends in each of those metrics for each month from 1935 through 2018.

**season_temp.Rmd**
The purpose of this code is to calculate the mean annual and seasonal average temperatures for Pinkham Notch and the Summit of Mount Washington and to analyze the trends for each season from 1935 through 2018. 

**indicators_trends.Rmd**
The purpose of this code is to calculate climate indicators and analyze trends in those indicators for Pinkham Notch and the Summit of Mount Washington. 


**snow_trends.Rmd**
This script was written to calculate and analyze the trends in the following metrics: first snowfall, last snowfall, snow season start and end date, total snow, and maximum snow depth for the Pinkham Notch and Summit snow records. 

**above_zero_threshold.Rmd**
The Purpose of this script is to calculate the first day when smoothed air temperature crosses from below 0°C to above 0°C. The threshold and the code to calculate it were both adapted from Contosta et al. (2017) and Alix Contosta's Github repository.


**DATA FILES**

**“pinkham_temp.csv”** – file containing homogenized daily min, max, and average temperature data for Pinkham Notch from 1935 – 2018. Columns: year, month, day, MaxT_PN, MinT_PN, temp_c. Temperatures are given in °C, “temp_c” is the average daily temp. 

**“summit_temp.csv”** – file containing daily min, max, and average temperature data for Mt. Washington Summit from 1935 – 2018. Columns: year, mo, day, maxC, minC, average, jday. 
Temperaturs are given in °C, “mo” is month. 

**“PN_snow.csv”** – file containing daily snow depth and snow fall data for Pinkham Notch from 1930 – 2018. Columns: STATION, DATE, SNOW (MM), SNAW (MM), SNOW (in), SNAW (in), First SNOW, first SNAW. SNOW (MM) is snowfall in millimeters, SNAW (MM) is snow depth in mm. First SNOW is the date of the first snowfall for each year. First SNAW is the date of the first snow depth measurement for each year. 

**“summit_snow.csv”** – file containing daily precipitation, snow depth, and snow fall data for Mt. Washington Summit from 1948 – 7/29/2020. Columns: Date, Precipitation, Snowfall, SnowDepth. Measurements are in inches, M, indicates missing data and T indicates trace amount (less than 0.1" snowfall; less than 1" snow depth). 




**References**

Contosta, A. R., Adolph, A., Burchsted, D., Burakowski, E., Green, M., Guerra, D., ... & Routhier, M. (2017). A longer vernal window: the role of winter coldness and snowpack in driving spring transitions and lags. Global change biology, 23(4), 1610-1625.


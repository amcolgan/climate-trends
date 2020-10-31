# climate-trends
This repository includes all code needed to carry out analysis of climate trends at Pinkham Notch and Mount Washington and to create figures for publication. 

**R CODE**

**monthly_temp_trends.Rmd** 
The purpose of this code is to calculate the mean monthly average, minimum, and maximum temperatures for Pinkham Notch and the Summit of Mount Washington and to analyze the trends in each of those metrics for each month from 1935 through 2018. Running this code produces the following:

1. 'monthly_results.csv', a csv file containing information on the mean average, minimum, and maximum temperature for each month and each site and the results of Mann Kendall and Sens Slope analysis of the trends over time. 

2. A set of three multi-panel graphs showing the trend over time in the mean average, minimum, and maximum, monthly temperature for each month. These graphs are saved as png files named 'avg_plot.png', 'max_plot.png', and 'min_plot.png', respectively.

Required Input files: “pinkham_temp.csv”, “summit_temp.csv”

**season_temp.Rmd**
The purpose of this code is to calculate the mean annual and seasonal average temperatures for Pinkham Notch and the Summit of Mount Washington and to analyze the trends for each season from 1935 through 2018. Running this code produces the following:

1. 'seasonal_trends.csv', a csv file containing the results of Mann Kendall and Sens Slope analysis of the trends over time for each year (annual) and each season. 

2. Figures showing trends in annual temperature averages ("annual.temp.trend.png") and a panel figure showing the trends in each season ("season.png")

Required input files: "pinkham_temp.csv", "summit_temp.csv"

**indicators_trends.Rmd**
The purpose of this code is to calculate climate indicators and analyze trends in those indicators for Pinkham Notch and the Summit of Mount Washington. 

1. "climate_indices_trend_results.csv" - a csv file containing results of the analysis

2. "growing.season.end.png" - a graph showing data on the end of the growing season at the summit of mount washington over time. 

required input files: "pinkham_temp.csv", 'summit_temp.csv', 'PN_snow.csv', 'summit_snow.csv'


**snow_trends.Rmd**
This script was written to calculate and analyze the trends in the following metrics: first snowfall, last snowfall, snow season start and end date, total snow, and maximum snow depth for the Pinkham Notch and Summit snow records. Running this code produces the following:

1. "snow_results.csv" - a csv file containing results of trend analysis for each metric x each site including slopes and p values. 

2. The following three figures: 
(1) "snow.season.png" - a graph showing trends in the start and end dates of the continuous snow season at Pinkham Notch from 1931 - 2018. 
(2) "snow.png" - a two panel graph showing in one panel the trend in total snowfall and in the other the trend in maximum snowpack depth. Both are for Pinkham Notch. 
(3) "tot_snow.png" - a graph showing the trends in total snowfall at Pinkham Notch between 1931 - 2018. 

Required input files: "PN_snow.csv", "summit_snow.csv"


**above_zero_threshold.Rmd**
The Purpose of this script is to calculate the first day when smoothed air temperature crosses from below 0°C to above 0°C. The threshold and the code to calculate it were both adapted from Contosta et al. (2017) and Alix Contosta's Github repository. Running this code produces the following:

1. "above_zero_results.csv" - a csv file containing the results of trend analysis in the date of spring above zero threshold from 1935 - 2018 for both Pinkham and Mt. Washington Summit.

2. "temp.above.zero.png" - a figure showing the trend in the date of the above zero threshold for both pinkham and the summit. 

PLEASE NOTE: THIS CODE INVOLVES RUNNING 1000 ITERATIONS FOR EACH YEAR FOR EACH SITE AND CAN TAKE A WHILE TO RUN. YOU CAN CHANGE THE NUMBER OF ITERATIONS BY ADJUSTING THE "g" VARIABLE IN THE ABOVE ZERO THRESHOLD FUNCTION (line 88).

required input files: "pinkham_temp.csv", "summit_temp.csv"


**DATA FILES**

**“pinkham_temp.csv”** – file containing homogenized daily min, max, and average temperature data for Pinkham Notch from 1935 – 2018. Columns: year, month, day, MaxT_PN, MinT_PN, temp_c. Temperatures are given in °C, “temp_c” is the average daily temp. 

**“summit_temp.csv”** – file containing daily min, max, and average temperature data for Mt. Washington Summit from 1935 – 2018. Columns: year, mo, day, maxC, minC, average, jday. 
Temperaturs are given in °C, “mo” is month. 

**“PN_snow.csv”** – file containing daily snow depth and snow fall data for Pinkham Notch from 1930 – 2018. Columns: STATION, DATE, SNOW (MM), SNAW (MM), SNOW (in), SNAW (in), First SNOW, first SNAW. SNOW (MM) is snowfall in millimeters, SNAW (MM) is snow depth in mm. First SNOW is the date of the first snowfall for each year. First SNAW is the date of the first snow depth measurement for each year. 

**“summit_snow.csv”** – file containing daily precipitation, snow depth, and snow fall data for Mt. Washington Summit from 1948 – 7/29/2020. Columns: Date, Precipitation, Snowfall, SnowDepth. Measurements are in inches, M, indicates missing data and T indicates trace amount (less than 0.1" snowfall; less than 1" snow depth). 




**References**

Contosta, A. R., Adolph, A., Burchsted, D., Burakowski, E., Green, M., Guerra, D., ... & Routhier, M. (2017). A longer vernal window: the role of winter coldness and snowpack in driving spring transitions and lags. Global change biology, 23(4), 1610-1625.


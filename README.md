# Capstone : Forecasting Water Levels in Chennai India
​
​
*By: Asher Lewis* [Github](https://github.com/abrahamlewis4867)
<img src="./assets/chennai-gif_0_SM.gif" width="1400px">>

## Problem Statement

For this project, we are going to try to forecast the average monthly water level for Chennai India's four main reservoirs using time-series data. The threshold of success of our model doing well enough that if it scores higher than the baseline model. The reason for doing so is that in 2019 Chennai experienced a water crisis which had millions of people left without water and required many trains and truck to get the city water. If we can forecast the monthly demand for a given reservoir we can get an idea of how and when the cities reservoirs run out of water. This information can potentially be used later down the line to predict future water demand. The water level is measured in millions of cubic feet. We are going to score our predictions using the Mean Squared Error (MSE). Water demand forecasting is hard in general so we have a rather modest goal for our model to score lower than the baseline's model MSE. This would translate to our model having an MSE closer to zero than the Baseline.regression models.



## Executive Summary

On 19 June 2019, Chennai city officials declared that "Day Zero", or the day when almost no water is left, had been reached, as all the four main reservoirs supplying water to the city had run dry. First in this project we first combined our two given data sets and saved them into a new csv for analysis and forecasting.

The workflow was than broken up in four separate notebooks with this fifth one serving as the place where the notebooks could all come together.

In each notebook, we analyzed trends and the nature of both the water level and rain. 
We then explained some elements of time-series data, such as the potential problem of data not being stationary. 

After this, we split our data and modeled. We ran a baseline model on each one of the reservoirs. After that, we ran an ARIMA model on each reservoir. 
For the ARIMA model, we looked at the residuals and plotted the predictions.



## Table of Contents
The workflow for this project has been divided up into five notebooks:  
    
Four notebooks for each individual reservoir, and a fifth notebook that summarizes our problems and findings.

1. [Main notebook](https://github.com/abrahamlewis4867/GA-Capstone-Project/blob/master/code/main_notebook.ipynb)
1. [Notebook for Chembarambakkam](https://github.com/abrahamlewis4867/GA-Capstone-Project/blob/master/code/notebook_for_chembarambakkam_reservoir.ipynb)
1. [Notebook for Poondi](https://github.com/abrahamlewis4867/GA-Capstone-Project/blob/master/code/notebook_for_poondi_reservoir.ipynb)
1. [Notebook for Redhills](https://github.com/abrahamlewis4867/GA-Capstone-Project/blob/master/code/notebook_for_redhills_reservoir.ipynb)
1. [Notebook for Cholavaram](https://github.com/abrahamlewis4867/GA-Capstone-Project/blob/master/code/notebook_for_cholavaram_reservoir.ipynb)


## Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|Date|datetime64|chennai_reservoir_levels.csv| The date in year, month and day|
|Poondi_water_level|Float64|chennai_reservoir_levels.csv|Water level of Poondi lake in Millions of Cubic Feet|
|Cholavaram_level|Float64|chennai_reservoir_levels.csv|Water level of Cholavaram lake in Millions of Cubic Feet|
|Redhills_water_level|Float64|chennai_reservoir_levels.csv|Water level of Redhills lake in Millions of Cubic Feet|
|Chembarambakkam_water_level|Float64|chennai_reservoir_levels.csv|Water level of Chembarambakkam lake in Millions of Cubic Feet|
|Cholavaram_rain|Float64|chennai_reservoir_rainfall.csv|Rainfall for Cholavaram lake in millimeters|
|Poondi_rain|Float64|chennai_reservoir_rainfall.csv|Rainfall for Poondi lake in millimeters|
|Redhills_rain|Float64|chennai_reservoir_rainfall.csv|Rainfall for Redhills lake in millimeters|
|Chembarambakkam_rain|Float64|chennai_reservoir_rainfall.csv|Rainfall for Chembarambakkam lake in millimeters|

Our data comes from [Chennai Metro and Sewer](https://chennaimetrowater.tn.gov.in/) and was gathered together on Kaggle. It contains data daily data from 2004 to the end of 2019.




## Conclusions and Recommendations

All of our models managed to get above our problem statement's goal of higher MSE score than the baseline model.

Time-series data is a very difficult task and I wish I had more time, more time to go in-depth to see things that are very elusive and have to be pulled out. The seasons define us and the trends need to be explored

There are many things we can do in the future such as implementing more complex Models such as SARIMA and var models. Another thing we could do is run the are existing models with differencing the data. Another thing we could have done is regularize the data.

It goes without being said but always getting more data is better. It would be nice to have such features such as temperature and exact water usage.


In terms of the data, it was fascinating to see how in the data how much everything is man-made from the reservoirs themselves to the water scarcity problem with the data. I would suggest better collection methods of water during the monsoon season. Another thing I would suggest is to get a better record of how people use the water. This is truly a crisis that unfortunately awaits most cites unless we take the proper action.



## References

1. [Duke University](http://people.duke.edu/~rnau/timereg.html)  
1. [Penn State](https://online.stat.psu.edu/stat462/node/188/) 
1. [dataquest](https://www.dataquest.io/blog/tutorial-time-series-analysis-with-pandas/)
1. [lin_reg_SOLUTION](https://git.generalassemb.ly/DSI-US-12/)
1. [Regression Metrics](https://git.generalassemb.ly/DSI-US-12/)
1. [linear_time_series_SOLUTION](https://git.generalassemb.ly/DSI-US-12)
1. [Indian Express](https://www.newindianexpress.com/cities/chennai/2019/jun/15/water-becomes-a-priced-possession-in-north-chennai-1990378.html)
1. [Our water in stress](https://ourworldindata.org/water-use-stress) 
1. [Water Project](https://www.wri.org/aqueduct/data)  
1. [UN](https://www.un-ihe.org/water-peace-and-security-partnership)
1. [Digital India](https://analyticsindiamag.com/solving-global-water-crisis-with-artificial-intelligence/)    
        
1. [Kaggle](https://www.kaggle.com/sudalairajkumar/exploration-to-quench-chennai-s-thirst)   
1. [towards data](https://towardsdatascience.com/almost-everything-you-need-to-know-about-time-series-860241bdc578)
1. [npr](https://www.npr.org/sections/goatsandsoda/2019/06/25/734534821/no-drips-no-drops-a-city-of-10-million-is-running-out-of-water)

1. [indian press](https://www.newindianexpress.com/cities/chennai/2019/jun/15/water-becomes-a-priced-possession-in-north-chennai-1990378.html
)
1. [wbr](https://www.wbur.org/onpoint/2019/08/01/india-chennai-water-shortage-crisis-infrastructure)
1. [cenus India](https://censusindia.gov.in/maps/Town_maps/chennai_Mun_cor_div.aspx)
1. [stack exchange](https://stats.stackexchange.com/questions/142248/difference-between-r-square-and-rmse-in-linear-regression)
1. [chenni sewer metro](https://chennaimetrowater.tn.gov.in/)
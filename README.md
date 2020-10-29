<img src = '../Images/BMWBanner.jpg' width = 850/>

# Carbuying Made Easy: <br>Predicting the Price of a Car Based on its Features 
<b>by Clifton Saul</b>

## Project Overview & Background

This project's task is to utilize previously developed skills in data exploration and analysis and build upon them by developing, testing, and evaluating a model. Specifically, this project will use a multiple linear regression model to predict the price of a car given its features. In the notebook, the scenario involved is a friend asking for help in predicting a fair price for a vehicle. By predicting a fair price for a vehicle given particular features, the friend can then evaluate if a listed price is above or below predictions for a similar vehicle.

This topic was chosen from the author's own personal interests in vehicles and out of curiosity after recently assisting a friend in purchasing a vehicle. The data used is freely available, and therefore this experiment is easily replicated. There are similar projects which use regression to predict prices of cars, houses, and other items available on Github currently. While this project was not inspired by those, the author encourages others to visit some of those other individuals' work.


## Repo Content & Navigation

<b>[Data](https://github.com/cmszip/DATA601-Project1-Regression/tree/main/Data)</b> - Folder containing datasets used in this project.
  * <b>[auto_data.csv](https://github.com/cmszip/DATA601-Project1-Regression/blob/main/Data/auto_data.csv)</b> - dataset of 201 automobiles pulled from IBM Cloud. Dataset can also be downloaded from [Kaggle](https://www.kaggle.com/statsakash/used-car-price-prediction).
* <b>[Images](https://github.com/cmszip/DATA601-Project1-Regression/tree/main/Images)</b> - Folder containing images used in this project.
* <b>[Notebooks](https://github.com/cmszip/DATA601-Project1-Regression/tree/main/Notebooks)</b> - Folder containing the Jupyter notebook used in this project.
  * <b>[Notebook 1 - Technical Notebook](https://github.com/cmszip/DATA601-Project1-Regression/blob/main/Notebooks/Notebook%201%20-%20Technical%20Notebook.ipynb)</b> - Jupyter notebook where data was pulled, explored, and cleaned, and models were built and evaluated. 
* <b>[License](https://github.com/cmszip/DATA601-Project1-Regression/blob/main/LICENSE)</b> - MIT license and copyright.

## Motivation

Buying a car can be one of the most stressful experiences in a person's life. There is a ton of information to weigh, salespeople will push and pressure you, and knowing you can easily be taken advantage of can make the experience a painful one.
![Stressed Out Car](https://www.confused.com/-/media/confused/articles/article-content-images/car-insurance/driving-stress-main.jpg?la=en-gb&hash=FD620795484988910AC1E8C32C671B2AF49C880B)

However, we rarely stop and take a moment to wonder if the weather is actually odd or if it's typical for the given time of year. People should be able to discern if the weather truly is uncommon, and the author wants to provide a useful tool for others to do just that.

## Goals

Given the above motivation, the primary goal of this project is to determine if Baltimore's forecasted temperatures are in line with historical data. If so, it will explain how the forecasted data falls within historical norms. If not, it will explain how the forecasted temperatures differ from historical norms.

A secondary goal is a more personal one. This author hopes to build experience using an API to effectively retrieve data. This project will use the 8 day forecast provided by OpenWeather API and compare it to the historical temperatures taken from Baltimore's US Weather Station for the same area over those same days.


## Data Overview

Data was pulled from two different sources: OpenWeather API and from Carnegie Mellon University's repository of US Weather Station data. 

In order to use OpenWeather's API, you must first create an account [at this page](https://openweathermap.org/api) to receive your personal API key. Accounts vary in price and access, but this project uses data that can be gathered from a free account. The specific API the author used was [OpenWeather's One Call API](https://openweathermap.org/api/one-call-api), which pulls forecasted weather data of eight days for a selected latitude and longitude. Because this project is focused on Baltimore's forecast, the values for latitude and longitude were those for Baltimore, MD.

An important note: this project can be replicated, but not for the exact same dates, as this project requested data from the API on October 3, 2020 to receive a forecast from October 3, 2020 to October 10, 2020. Instead, if you wish to replicate this project, you can use [OpenWeather's One Call API](https://openweathermap.org/api/one-call-api) to pull forecasting data for the week following when you run the code seen in the notebook. From there, you will need to alter the code used to clean the dataset from Carnegie Mellon University. That dataset is taken from [this csv](https://github.com/cmszip/DATA601-Assignment2/blob/main/Data/USW00093721.csv). The alterations you should make are in the seventh code block of [Notebook 1](https://github.com/cmszip/DATA601-Assignment2/blob/main/Notebooks/Notebook%201%20-%20Weather%20Data%20Acquisition%20%26%20Cleaning.ipynb), specifically within the "Pull and Clean Historical Data" section and beneath "# Remove dates outside forecast range". Modify the month(s) and days you wish to focus on or exclude. Once you've done this, you will be able to replicate this project for the time you wish to examine.

The dataset from Carnegie Mellon University contains data from the US Weather Station in Baltimore. These include daily weather readings from 1871 to 2018. Because the US Weather Station in Baltimore moved in 1950 from downtown Baltimore to Baltimore Washington Thurgood Marshall International Airport (BWI), the author only used data from 1950 and later.

Below is information on each dataset and the packages used in this project:

#### The OpenWeather API 
The original dataset of the 8 day forecast includes:
  * 8 rows
  * 21 columns:
    * Column datatypes:
      * float64: 11
      * int64: 7
      * object: 3
 
 This dataset was altered to include:
  * 8 rows
  * 7 columns
    * Column datatypes:
      * datetime64: 1
      * float64: 3
      * int64: 3
      
 #### US Weather Station Data
 The original csv file of historical weather data from the Baltimore weather station includes:
  * 54,421 rows
  * 5 columns
    * Column datatypes:
      * float64: 3
      * int64: 1
      * object: 1
      
 This dataset was altered to include:
  * 560 rows
  * 7 columns
    * Column datatypes:
      * datetime64: 1
      * float64: 3
      * int64: 3
 
 #### Merged Dataset
 These two datasets were combined and altered to create the following dataset:
  * 568 rows
  * 8 columns
    * Column datatypes:
      * datetime64: 1
      * float64: 3
      * int64: 3
      * object: 1
      
#### Packages
Packages used to retrieve, clean, alter, and analyze the data included:
 * datetime
 * json
 * matplotlib
 * numpy
 * pandas
 * requests
 * seaborn
 
## Summary

The forecasted temperatures for Baltimore, MD, USA for the week dating from October 3, 2020 to October 10, 2020 are common for the time period historically. The average forecasted high temperature is approximately 1.5 degrees Fahrenheit below the average high from 1950 to 2018. However, the average forecasted low temperature is more than 6 degrees Fahrenheit above the the average low from 1950 to 2018. What is most notable is that the temperature is rather stable, as the difference between the forecasted high and low temperatures is only 63.68% of the average historic difference between high and low temperatures. This means that we can expect less temperature change during the upcoming week than is typical. No heavy coats needed yet. 

## Limitations
One of the main limitations of this project regards the dataset. It is only 568 rows. This is due mainly to the small window of time we are exploring (an eight day period). Additionally, while the original dataset from Carnegie Mellon University contains data beginning in 1871, we decided to remove all data from before 1950. The reasoning behind this is that the original US Weather Station for Baltimore was located in downtown Baltimore until 1950, when it was moved to its current location at the airport that is now known as BWI. For consistency of data, the decision to shrink the dataset was made. Further exploration to compare the forecast to dates beginning in the 1870s could be done, however.

## Contributors

Clifton Saul

## [License & copyright](https://github.com/cmszip/DATA601-Assignment2/blob/main/LICENSE) 

© Clifton M Saul Jr.


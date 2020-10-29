<img src = '../Images/BMWBanner.jpg' width = 850/>

# Automating the Start of an Automobile Startup: <br>Predicting the Price of a Car Based on its Features 
<b>by Clifton Saul</b>

## Project Overview & Background

This project's task is to utilize previously developed skills in data exploration and analysis and build upon them by developing, testing, and evaluating a model. Specifically, this project will use a multiple linear regression model to predict the price of a car given its features. In the notebook, the scenario involved is a friend asking for help in predicting a fair price for a vehicle. By predicting a fair price for a vehicle given particular features, the friend can then evaluate if a listed price is above or below predictions for a similar vehicle.

This topic was chosen from the author's own personal interests in vehicles and out of curiosity after recently assisting a friend in purchasing a vehicle. The data used is freely available, and therefore this experiment is easily replicated. There are similar projects which use regression to predict prices of cars, houses, and other items available on Github currently. While this project was not inspired by those, the author encourages others to visit some of those other individuals' work.


## Repo Content & Navigation

<b>[Data](https://github.com/cmszip/DATA601-Assignment2/tree/main/Data)</b> - Folder containing datasets used in this project.
  * <b>[Baltimore7DayForecast.csv](https://github.com/cmszip/DATA601-Assignment2/tree/main/Data)</b> - dataset of Baltimore's forecasted temperatures initially retrieved from OpenWeather API. See [Notebook 1](https://github.com/cmszip/DATA601-Assignment2/blob/main/Notebooks/Notebook%201%20-%20Weather%20Data%20Acquisition%20%26%20Cleaning.ipynb) for more details on using this API.
  * <b>[USW00093721.csv](https://github.com/cmszip/DATA601-Assignment2/blob/main/Data/USW00093721.csv)</b> - dataset of temperature and precipitation readings from the US Weather Station in Baltimore. Taken from Carnegie Mellon University at [this webpage](https://kilthub.cmu.edu/articles/dataset/Compiled_daily_temperature_and_precipitation_data_for_the_U_S_cities/7890488?file=20881932).
  * <b>[CombinedWeather.csv](https://github.com/cmszip/DATA601-Assignment2/blob/main/Data/CombinedWeather.csv)</b> - cleaned dataset formed from the merging of the two previously mentioned datasets.
* <b>[Images](https://github.com/cmszip/DATA601-Assignment2/tree/main/Images)</b> - Folder containing images used in this project.
* <b>[Notebooks](https://github.com/cmszip/DATA601-Assignment2/tree/main/Notebooks)</b> - Folder containing the Jupyter notebooks used in this project.
  * <b>[Notebook 1 - Weather Data Acquisition & Cleaning](https://github.com/cmszip/DATA601-Assignment2/blob/main/Notebooks/Notebook%201%20-%20Weather%20Data%20Acquisition%20%26%20Cleaning.ipynb)</b> - Jupyter notebook where OpenWeather API was called to retrieve data, and datasets were cleaned in preparation for analysis. Code to use API and save the data retrieved can be found in the second codeblock. 
  * <b>[Notebook 2 - Weather Data Analysis](https://github.com/cmszip/DATA601-Assignment2/blob/main/Notebooks/Notebook%202%20-%20Weather%20Data%20Analysis.ipynb)</b> - Jupyter notebook where data analysis is conducted to answer research question.
  * <b>[Notebook 3 - Summary Presentation](https://github.com/cmszip/DATA601-Assignment2/blob/main/Notebooks/Notebook%203%20-%20Summary%20Presentation.ipynb)</b> - Jupyter notebook that provides the data analysis from Notebook 2 without viewing the code. This is meant to provide a cleaner notebook to read from.
* <b>[License](https://github.com/cmszip/DATA601-Assignment2/blob/main/LICENSE)</b> - MIT license and copyright.

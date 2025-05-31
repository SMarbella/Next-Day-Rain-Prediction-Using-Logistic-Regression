![image](https://github.com/user-attachments/assets/9692c535-9dd3-464a-baad-6d060788ea50)![image](https://github.com/user-attachments/assets/9de4bee7-df0a-4b15-a8be-cee351e87d96)# Next Day Rain Prediction Using Logistic Regression
## Data Information
This project comprises about 10 years of daily weather observations from numerous locations across Australia. I used Python and Jupyter Notebooks to perform logistic regression to predict next-day rain in Australia. It explores features that increase the likelihood of rain in Australia and predicts whether or not it will rain tomorrow.

## Source
**Title:** Rain in Australia

**Date of Study:** 2007 - 2017

**Authors:** Joe Young and Adam Young

**Affiliation:** Kaggle

**Relevant Information:**
The observations were gathered from a multitude of weather stations. You can access daily observations from http://www.bom.gov.au/climate/data.
For example, you can check the latest weather observations in Canberra here: Canberra Weather.

Definitions have been adapted from the Bureau of Meteorology's Climate Data Online.
Data source: Climate Data and Climate Data Online.

Copyright Commonwealth of Australia 2010, Bureau of Meteorology.

**Source:** https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package

## Table Columns
Date - The date of observation.

Location - The common name of the location of the weather station.

MinTemp - The minimum temperature in degrees celsius.

MaxTemp - The maximum temperature in degrees celsius.

Rainfall - The amount of rainfall recorded for the day in mm.

Evaporation - The so-called Class A pan evaporation (mm) in the 24 hours to 9am.

Sunshine - The number of hours of bright sunshine in the day.

WindGustDir - The direction of the strongest wind gust in the 24 hours to midnight.

WindGustSpeed - The speed (km/h) of the strongest wind gust in the 24 hours to midnight.

WindDir9am - Direction of the wind at 9am.

WindDir3pm - Direction of the wind at 3pm.

WindSpeed9am - Wind speed at 9am.

WindSpeed3pm - Wind speed at 3pm.

Humidity9am - Humidity level at 9am.

Humidity3pm - Humidity level at 3pm.

Pressure9am - Barometric pressure at 9am.

Pressure3pm - Barometric pressure at 3pm.

Cloud9am - Cloudiness level at 9am.

Cloud3pm - Cloudiness level at 3pm.

Temp9am - Temperature at 9am.

Temp3pm - Temperature at 3pm.

RainToday - Did it rain today?

RainTomorrow - Will it rain tomorrow?

## Retrieved table from
- https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package/data

# Charts and Calculations Generated For This Project

## Jupyter Notebooks Libraries
I imported the common libraries used for Jupyter Notebook. The pandas library is an open-source tool for data analysis and manipulation in Python. It reads files and creates Dataframes and Series. The NumPy library works with arrays and performs mathematical calculations. The Seaborn library provides statistical data visualization. The Sklearn library includes tools I need for machine learning and making predictions based on data.

# Data Cleaning
I created a DataFrame in Python using Pandas and read the data into it. I displayed the number of rows and columns. The raw data table has 143460 rows and 23 columns. I chose to include 9 columns into the analysis since I do not need all the columns.
![Image](https://github.com/SMarbella/Next-Day-Rain-Prediction-Using-Logistic-Regression/blob/main/Data%20Cleaning/Number%20of%20Null%20Values.png)

I checked each column for Null values and dropped them. I included a comparison that shows the table with its NULL values and after I removed its NULL values. This time, the cleaned table has fewer columns. It shows no NULL values.
![Image](https://github.com/SMarbella/Next-Day-Rain-Prediction-Using-Logistic-Regression/blob/main/Data%20Cleaning/Before%20and%20After%20Removing%20Nulls.png)

# Data Exploration
I split the dataset into feature_set and target_set. The feature_set includes WindSpeed9am, WindSpeed3pm, Humidity9am, Humidity3pm, Temp9am, and Temp3pm. The target_set includes the RainRomorrow column. I converted the RainTomorrow values into their mapped numeric variables. Using the Seaborn library, I cerated a pairplot. The plots visually compare all the columns included in feature_set. RainTomorrow color codes the likelihood of rain.
![Image](https://github.com/SMarbella/Next-Day-Rain-Prediction-Using-Logistic-Regression/blob/main/Data%20Exploration/Pairplot.png)

I imported the train_test_split function from the Sklearn library and split the data into training and testing sets. I imported LogisticRegression and accuracy_score from the Sklearn library to measure the accuracy of my logistic regression. I instantiated a logistic regression machine learning model. When I assessed my model's performance, its accuracy score is 0.8305474452554744, meaning that it is quite accurate in predicting raining conditions. The model correctly predicts 83% of the rainy forecasts based on the weather’s possible combinations of features. I created a confusion matrix to map its accuracy.

# UdacityDSND-Capstone Project: Sparkify
This code was written under the Udacity Data Scientist Nanodegree Project.
Capstone Project - Sparkify

## Table of Contents

1. [Installation](#Installation)
2. [Introduction/Motivation](#Introduction)
3. [Data](#Data)
4. [Results](#Results)
5. [Licensing, Authors, and Acknowledgements](#Licensing)

## Installation <a name="Installation"></a>
* The code was developed and tested on anaconda with python 3.73. Nevertheless, it should run with no issues using Python 3.* in any other environment.
* The dataset (tiny subset) is included in this rep.
* Libraries needed:
  * PySpark;
  * Pandas;
  * Seaborn 0.9+;
  * Matplotlib.

## Introduction / Motivation <a name="Introduction"></a>
This is an Udacity Data Science Nanodegree project.

#### Intro
Sparkify is a music streaming service (similar to Apple Music and Spotify), and can be used for free, or if the customer wants there are also paid plans which eliminate advertising.

The data provided is the log of the users interactions with the service/application. Every event/interaction is recorded with the following information:

`root
 |-- artist: string (nullable = true)
 |-- auth: string (nullable = true)
 |-- firstName: string (nullable = true)
 |-- gender: string (nullable = true)
 |-- itemInSession: long (nullable = true)
 |-- lastName: string (nullable = true)
 |-- length: double (nullable = true)
 |-- level: string (nullable = true)
 |-- location: string (nullable = true)
 |-- method: string (nullable = true)
 |-- page: string (nullable = true)
 |-- registration: long (nullable = true)
 |-- sessionId: long (nullable = true)
 |-- song: string (nullable = true)
 |-- status: long (nullable = true)
 |-- ts: long (nullable = true)
 |-- userAgent: string (nullable = true)
 |-- userId: string (nullable = true)`
 
This project has 4 main stages:
1. Loading and cleaning data
    1. Load dataset
    2. Cleaning missing or invalid data
2. Exploratory Data Analysis
    1. Define Churn & Downgrades from the original features
    2. Explore data (analysing interactions from both type of users: those who churned and those who didn't)
3. Feature Engineering
    1. Build meaningfull features from the original dataset for each user, that represent the overall experience in Sparkify
    2. Save final dataset with engineered features
4. Model training and Prediction
    1. Split data into training and testing data sets
    2. Train several classification models & Hyperparameter tunning with Grid Search
    3. Select best machine learning model based on f1score

In this project I'll be using Spark (PySpark) for all the data manipulation, loading, cleaning, feature engineering and Machine Learning.
This workspace contains a tiny subset (128MB) of the full dataset available (12GB). This workspace is used to build the project, or to explore a smaller subset with Spark. The code can then be deployed on the cloud.


#### Problem Definition

The aim of this project is to predict customer churn based on its usage history/log. For that purpose it will be needed to generate new meaningfull features that characterize user experience in Sparkify, so that we can use a machine learning model to predict which customers are likely to churn.

For the prediction part I'll be using use F1 score to select the best machine learning model since the churned users are a fairly small subset (highly imbalanced dataset).
   
## Data <a name="Data"></a>
```text
DataScience-LisbonAirbnb/
├── DataScience-LisbonAirbnb.ipynb
├── utility.py
└── data/
    ├── listings_complete.csv
    ├── calendar.csv
    ├── listings.csv
```
* __DataScience-LisbonAirbnb.ipynb__: Notebook with all the scripts used to analyse data and to answer the questions mentioned above
* __Data/listings.csv__: Listings data for Lisbon ([Airbnb](https://airbnb.com/))
* __Data/listings_complete.csv__: Detailed Listings data for Lisbon ([Airbnb](https://airbnb.com/))
* __Data/calendar.csv__: Detailed Calendar Data for listings in Lisbon ([Airbnb](https://airbnb.com/))

## Results <a name="Results"></a>
The detailed analysis and main conclusions/results are availabe in [here](https://medium.com/@luisf.almeida90/lisbon-an-amazing-destination-b36edff06967)).

* Price fluctuation over time

![price_vs_time](price_vs_time.png)
For 2019, the prices decrease after Summer time until December.
Then, close to New Year's Eve, there is sudden increase in average price as it would be expected.
For 2020, the prices are considerably higher than in 2019, and seem to steadily increase from the begining of the year.


* Listings - price tag and property types

![pricetag](pricetag.png)

![proptype](proptype.png)

As seen in the bar chart above, most of the listings have a price tag between 20\\$ and 140\\$
Also, the most frequent property type is apartment, followed up by (entire) house.


* Main factors influencing price

![pricepred](pricepred.png)

The features which characterize the house/listing topology (bathrooms, bedrooms, accomodates) are on the top 5 of the top 10 important features, meaning these features have a high impact on the price.


## Licensing, Authors, and Acknowledgements <a name="Licensing"></a>
* Thanks to Udacity for all the useful insights and interesting challenges!
* Thanks to Airbnb for making these data sets available to everyone!

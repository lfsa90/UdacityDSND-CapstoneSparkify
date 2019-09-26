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

For this project I chose Airbnb-Lisbon (my hometown) 2019 dataset ([here](http://insideairbnb.com/get-the-data.html)), and was mainly interested in finding the answers to the following questions:
1) How does price fluctuate over time?;
2) What is the availability trend over time?;
3) What type of listings do we have in Lisbon? - price range, house types and listings by neighbourood;
4) How is availability related wity price, host type, number of reviews and scores, and room type?;
5) Price preditction - main factors influencing price.
   
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

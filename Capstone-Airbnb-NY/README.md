# Capstone---Airbnb-NY

## Problem Statement

This project uses an Airbnb dataset to improve revenue management of Airbnb in NYC. The project utilizes the listings and reviews datasets to make inferences, practice NLP, and make predictions on the demand for accommodation in the hotels and the best price-value ratio for guests.

## Contents:

- Background
- Data Collection
- Data Cleaning
- Exploratory Data Analysis
- Modeling
- Conclusions and Recommendations

---

## Background

### Datasets

* [`listings.csv`](./data/listings.csv): Listing attributes for New York Airbnbs
* [`reviews.csv`](./data/reviews.csv): Reviews left by clients who stayed at the New York listings


### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|listing_id|float|reviews|The unique ID for each listing|
|id|object|float|The ID number|
|date|object|reviews|The data each review was written|
|reviewer_id|float|reviews|The unique ID for each reviewer|
|reviewer_name|object|reviews|The name of each reviewer|
|comments|object|reviews|The reviews left by customers who stayed in each listing|
|reviews_per_month|float|listings|The number of reviews per each month|
|number_of_reviews|float|listings|The total number of reviews|
|number_of_reviews_ltm|float|listings|The total number of reviews in the last twelve months|
|number_of_reviews_l30d|float|listings|The total number of reviews in the last 30 days|
|bedrooms|float|listings|The total number of bedrooms in each listing|
|accommodates|float|listings|The total number of people each listing can accommodate|

---

### Findings on Trends in the Data

One of the most unique findings was right in the beginning during the data cleaning stage: 82% of the selftext from our 'cats' Subreddit were missing values. And considering I only selected 1000 data entries for each Subreddit, this meant I was missing almost all of the selftext for 'cats'.¶
Because selftext is considered the body of the post, a missing value when initially analyzing our data does not mean that Reddit user were posting blank messages. Instead, we can assume that if no text was present in the body, that users were instead posting images, videos, or gifs.
Lastly, our best model was a stacked model of Logistic Regression, Naive Bayes, and Random Forests, which gave us a training score of 99.23%, testing score of 96.4%, and a sensitivity of 95.6%.


### Conclusions and Recommendations

##### My models did not perform very well, indicating that predicting price of Airbnb listings in NY based off of other numeric features is not that helpful.

##### The highest score I got was with Linear Regression and hit only about 22% on my test set.

##### In terms of revenue management and predicting the demand for accommodations, it's important to consider New York's size. This means that in order to be within walking distance of popular attractions or at a reasonable price, the listing will ideally accomodate 2-4 people with 1-2 bedrooms.

##### Still working with the Listings dataset, but focusing on number of reviews, we can see that the total number of reviews and the number of reviews in the last twelve months is relatively similar, both gravitating towards 100-125. This is pretty on track with the number of reviews in the last 30 days with the average being around 10 reviews.

##### These ask the questions:
* which months are most likely to generate reviews? 
* Is there correlation for volume of bookings per month and number of reviews left per month?

##### But on the NLP side and switching to the Reviews dataset, I found the bigrams most commonly listed in the comments on the listings:
* new york
* great location
* highly recommend
* place stay
* great host
* great place
* definitely stay
* walking distance
* central park

##### These bigrams would beneficial to consider when promoting the listings, i.e. How far away is your listing from Central Park? Is it within walking distance of popular New York attractions? And lastly, it's important to consider how to display for your most positive, and popular reviews to potential or returner customers to show them you have superhost qualities.

---
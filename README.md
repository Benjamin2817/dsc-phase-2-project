# Overview
The Prospective homebuyer looking to live in area for a few years and sell for profit.

## Business Problem
* What is the correlation between the sizes of properties and their selling prices?
* Where is renovation money best spent?
***

## Data
The kc_house_data.csv from Kaggle.com is the source of data for this project and contains 21,597 entries of homes sold in King County, Washington in the years 2014 and 2015.  Features from this dataset include a house's square footage of living space, it's number of bedrooms, and a grade based on it's construction quality. It's 'price' column becomes the target variable.

## Methods
Initial data cleaning involved removing duplicates and extreme outliers, assigning values to missing data, and changing columns to appropriate data types.  The baseline model trained here does not meet any of linear regression's assumptions.  And so, all categorical variables are turned into indicator columns, some (months, bedrooms, etc.) are first binned to reduce feature numbers.  New predictors are formed applying user created functions to split data based on renovation recency and coordinates.  Another model trained at this point shows an increased r-squared but still fails to meet the assumptions.  Data preparation for the third model was the removal of outliers in the dataset's  'price' and 'sqft_lot' determined with use of the interquartile range.  This model proves to meet the assumptions of both normality and homoscedasticity and yields a r-squared of %69.1.  Finally, for model four both continuous variables were log transformed and scaled to produce more normally distributed features.  This model ***produces a much more reliable r-squared

## Results
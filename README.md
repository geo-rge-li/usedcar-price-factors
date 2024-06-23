# Introduction
This is an analysis of about 30K car sales in the US. With information on the make, model, mechanical differences and specifications, color, and the region it is in, we want to determine what particular features of the car are stronger predictors for the price. 
## The Business Problem
Our goal is to determine what particular features of the car are stronger predictors for the price. In addition to that, the geographical location of the car may also factor into its sale price depending on the economic conditions of the area. The data received contains information about the make, model, mechanical differences and specifications, color, and the region it is in. The data also contains the price of the car. Our goal is to fit a model that will select the best features to predict the price of the car.
## Preparing the Data
In general, some of the data steps are not necessarily needed such as unique identifiers since those are not features that customers will use to determine price of the car. We removed those columns. Also rows with missing data or nonsensical data like a 0 dollar price on the car were discarded to avoid impacting the data analysis.

# Data Analysis

## Features Used
The following features were used to predict the price of the car:
- region
- year
- manufacturer
- model
- condition
- cylinders
- fuel
- odometer
- title_status
- transmission
- drive
- size
- type
- paint_color
- state

For the categorical features, we used label encoding to convert them to numerical values.

## Model Selection
We performed a grid search on the following models:
- Sequential Feature Selection (both forward and backward) with a Linear Regression model (with simple, 5, and 10-fold cross validation)
- Sequential Feature Selection (both forward and backward) with a Ridge Regression model with multiple alpha values (with simple, 5, and 10-fold cross validation)
- Lasso Regression with multiple alpha values (with simple, 5, and 10-fold cross validation)


---
title       : Shiny Forecast Tool
subtitle    : Interactive time-series and forecasting tool
author      : Zane Lim
job         : Analytics Consultant
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Shiny App for Forecasting

Four features:

1. Data: Selecting dataset from fpp R package/Uploading own dataset in csv
2. Exploratory Data Analysis: Exploratory data analysis and visualization
3. Decomposition: Time-series decomposition and smoothing
4. Forecasting

Credits to fpp R package
`install.packages('fpp')`

For more information, please refer to [Forecasting: principles and practice](https://www.otexts.org/fpp)

--- .class #id 

## Feature 1: Data

Allows user to either select one of the four dataset:

1. Monthly anti-diabetic drug sales in Australia from 1992 to 2008
2. Quarterly expenditure on eating out in Australia
3. Quarterly retail trade: Euro area
4. USA Electricity monthly total net generation

Or upload a csv file which contains a column/vector of time-series values, then specify the start year and frequency per year.

--- .class #id

## Feature 2: Exploratory Data Analysis

Allows user to explore the time-series data via the following plot:

1. Time plot: A line chart
2. Seasonal plot: A line chart broken down by year
3. Seasonal sub-series: A line chart broken down by season
4. Autocorrelation lag plot: Scatter plots with different lagged values (up to 9)
5. Autocorrelation function: A diagram which shows the autocorrelation coefficients (of different lagged values)

--- .class #id

## Feature 3 & 4: Decomposition and Forecasting

Decomposition allows user to pick the following decomposition or smoothing:

1. Seasonal adjustment: Adjust for seasonal effect using STL
2. Moving average: Smooth by moving average
3. STL decomposition: Decompose time-series to trend, seasonal and remainder components

Forecasting allows user to pick one of the two forecasting technique:

1. ARIMA
2. Exponential (Holt-Winters)

For simplicity, the parameters for the method are automatically chosen.

# Module 4 Final Project


## Introduction

For this project, I will be working with a financial dataset downloadeded from Yahoo Finance's API and apply a time-series model to it. My goal is to ultimately see if I can come up with any predictive qualities in the trends of the price. 

## Objectives

1. Understand the time-series algorithms and what exactly it is doing
2. See whether the applied algorithim offers any predictive qualities


## The Datasets

** Will be using SPY dataset from 2001 to present 2020 

1. Very complete, no missing data
2. Columns for a lot of things we will not be looking at but may be useful for future projects (volume) 
3. Dropping all columns except for adjusted close, this will be our target to model the changes in daily price of SPY

## Dataset EDA

Was not very complicated. Debated working with multiple stocks which would use some pandas merges and joins but did not end up going that route. Dataset was very complete with no missing values within the data itself. I made a custom dataset by splicing out all the columns except the adjusted close, and used this dataset for my ARIMA modeling and testing. 


## ARIMA Model

Will be running an ARIMA model with neccesary parameter adjustments for seasonality, trend, etc. ARIMA model is trained on a large majority of the data. Forecasting will be used to predict next-day prices. Will also view the autocorrelation and the partial autocorrelation. 

## Results

Decent model. Forecasting has definite flaws such as context of moves. Algorithm tends to go with the average moves, which makes sense looking at how its programmed. Does not really account for any fundamental changes. 

## Conclusion

Model did a decent job at choosing the average moves. However, this does not work often in the real world and the algorithm could not account for any significant events of strong fundamental changes in the market. Therefore when forecasting, the algorithm would return a weighted average line that would only work in certain situations of the market. More work must be done in both training and when to implement the algorithm in the first place. No real way to model for fundamental events in the traditional manner without including some sort of analysis on the data of fundamentals. This is a whole different phenomenon however. 

## Further Work

1. Look into more nuanced detail (Hourly or minute) to discern any unusual buying activity that may signify further moves
2. Train dataset purely on non-fundamental moves and apply the algorithm in real-life situations when fundamentals are not actively moving the markets. 
3. Apply algorithm to individual stocks/commodities and observe the success rate. 


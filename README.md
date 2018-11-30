# Guilford_Financial

## Introduction
Guilford County Financial Modeling is the idea for our project. We have data for Guilford County approved budgets from 2013-2018 and transactions from 2007-2018.
The dataset available is financial data mainly including adopted/amended budget data and historical transaction
data for the Guilford County. The idea is to help the Financial and Budget Department
of Guilford County in maintaining their expected spending and transactions.

Gregory Purvine (gnpurvin) https://github.com/gnpurvin

Evan Crabtree (Crabtr) https://github.com/Crabtr

Rohit Gulia (rohit-gulia) https://github.com/rohit-gulia

Cody Cothern (Mask487) https://github.com/Mask487

Vincent Xiao(MrVinegar) https://github.com/MrVinegar

## Goals
To be able to discover anomalies in the given financial data and be able to discover new
anomalies as new data is added. Eventually, we would also like to be able to
make financial forecasts and predictions based on the given data. We would like to be able to make predictions about
upcoming transactions. If time allows, we would also like to be able to implement a method for predicting what transactions are likely to
happen in the future. In the interest of keeping our project to a reasonable scope, we are focusing on anomaly detection. Our goal
at this point is to develop a method for discovering anomalies in the past financial data and for catching new anomalies as new data comes in.

## Objectives
In order to achieve these goals efficiently, we have divided the tasks among our team
members like maintaining the data dictionary and documentation, finding the relationships
in the data, finding the patterns in data in different departments, how the spending
trends change with time, detecting anomalies or abnormalities in transactions
and/or total actual spending as we move through the year.

## Stage 2 Tasks
Greg -> Analyze Revenue Data

Evan -> Analyze Expense Data

Rohit -> Data Cleaning

Vincent -> Analyze Transaction Data

Cody -> Anomaly Detection Research

## Data Cleaning
All missing amount values in the budget data have been filled with zeroes. The ExpSort column was dropped,
 as that column is not useful for our purposes at this time. All entries where the fund number was greater than
 or equal to 400 were dropped, at the advice of our mentor. After making these changes to the data (while keeping 
a separate copy of the original data), we split the data into two sets: Revenue and Expense Data. 
 
## Data Analysis
We have begun looking at high level trends in the budget data for both the expense and revenue data sets. 
We have also charted the top 6 revenue and expense sources. We've observed that while the sums of all 
expenses and revenues have both generally increased, the number of expense and revenue sources have both 
decreased over the observed period. 


## Anomaly Detection Research
We have found three methods of finding anomalies in our data: Recurrent Neural Networks, Autoregressive Models, and Sigma 3. While we will mostly likely use Sigma 3 for it's simplicity, we plan on experimenting with the other two methods if we have time to try and find more accurate ways to detect anomalies. 


## Stage 3 Tasks
Greg -> Transaction Regression Modelling

Evan -> Spending & Probability Distribution By Entity

Rohit -> Probability Distribution

Cody -> Budget Anomaly Detection

Vincent -> Transaction Anomaly Detection

## Transaction Regression Modelling
Goal was to see if we could come up with a model for predicting future transaction, as well as using the model
to assist with anomaly detection. Transaction data was plotted with various combinations of variables. Regression was attempted 
with single variable and multivariable models. Neither yielded any usable results. Either regression will not be a useful 
technique for our data set or regression needs to be done on a finer scale, perhaps performing it for each individual entity, 
as opposed to performing on the entire data set. 

## Budget Anomaly Detection
Goal was to find a way to detect anomalies in the budget data set. Anomaly detection was performed using 
Sig3 algorithm. Any value 3 standard deviations or more above or below the mean is considered an anomaly. 
We were able to calculate the number of anomalies within each department over the 5 year period and plot them 
to make it easier to visualize.

## Transaction Anomaly Detection
Similar to with the budget data, we want to be able to identify anomalous transactions. We will use the same methods 
and algorithm to try to find any transactions that seem out of the norm. This task is currently in progress, as we 
are still working on a way to make the data more presentable. 

## Probability Distribution
//description here

## Spending & Probability Distribution Per Entity
//description here

## Budget Forecasting using Time series for average spending in a month 
Time Series (TS) is a collection of data points collected at constant time intervals. These are analyzed to determine the long term trend so as to forecast the future or perform some other form of analysis.
But what makes a TS different from say a regular regression problem? There are 2 things: 
It is time dependent.
So the basic assumption of a linear regression model that the observations are independent doesn’t hold in this case. 
Along with an increasing or decreasing trend, most TS have some form of seasonality trends, i.e. variations specific to a particular time frame.
For example, if you see the sales of a woolen jacket over time, you will invariably find higher sales in winter seasons.

For this:
First step is to Check Stationarity of a Time Series
Second step is to make it Stationarity if it is not.
Third use a machine learning model to predict time series.


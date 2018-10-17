# Guildford_Financial

## Introduction
Guilford County Financial Modeling is the idea for our project. We have data for Guilford County approved budgets from 2013-2018 and transactions from 2007-2018.
The dataset available is financial data mainly including adopted/amended budget data and historical transaction
data for the Guilford County. The idea is to help the Financial and Budget Department
of Guilford County in maintaining their expected spending and transactions.

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


## Anomaly Detection
We have found three methods of finding anomalies in our data: Recurrent Neural Networks, Autoregressive Models, and Sigma 3. While we will mostly likely use Sigma 3 for it's simplicity, we plan on experimenting with the other two methods if we have time to try and find more accurate ways to detect anomalies. 

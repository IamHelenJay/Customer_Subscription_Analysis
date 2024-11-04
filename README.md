# Project Title; Subscription Analysis
---

## Project Overview
---
This data analysis project aims to provide insights into customer subscription trends and behavior to support strategic decision-making, The analysis focuses on understanding subscription patterns, cancellation trends, and  top-performing subscription types, regional breakdowns of customer activity. The goal is to enable the company to make data-driven decisions that improve customer satisfaction, reduce churn, and drive revenue growth.


## Data Sources
---
The primary source of data used in this analysis is the CustomerData set https://1drv.ms/u/s!Ap5Z5GRl9j5YhcdWfrVMRJ4XGP4dQQ?e=icEhNj


## Tools Used
---
1. Microsoft Excel
- For data cleaning and analysis, including creating pivot tables to find subscription patterns, calculate the average subscription duration and identify the most popular 
subscription types.

2.  SQL (Structure Query Language)
- For Data retrivals

3. Power BI
For Building a dashboard that visualizes key customer segments such as;
- cancellations, and subscription trends.

## Data Cleaning and Preparation
---
In the initial stage of data cleaning and preparation, we performed the following steps to ensure the dataset was accurate and ready for analysis:
- Data Loading and Inspection
- Handling Missing Data
- Data Cleaning and Formatting

## Exploratory Data Analysis 
---
The EDA involves the following key questions;
- retrieve the total number of customers from each region.
- find the most popular subscription type by the number of customers.
- find customers who canceled their subscription within 6 months.
- calculate the average subscription duration for all customers.
- find customers with subscriptions longer than 12 months.
- calculate total revenue by subscription type.
- find the top 3 regions by subscription cancellations.
- find the total number of active and canceled subscriptions.

## Data Analysis
---
Below are examples of some SQL queries and DAX expressions used during the analysis to extract and analyze key insights from the customer dataset:
```
SQL CODES

1. Retrieve All Data for Initial Inspection
SELECT * FROM CustomerData
```



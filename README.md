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

SQL CODES

1. Retrieve All Data for Initial Inspection
```
SELECT * FROM CustomerData
```
---
2. Retrieve the Total Number of Customers from Each Region
```
SELECT Region, COUNT(CustomerID) AS TotalCustomers
FROM CustomerData
GROUP BY Region;
```
Region | TotalCustomers
-------|------------------
North	 | 8433
East	 | 8488
South	 | 8446
West	 | 8420

---
3. find the most popular subscription type by the number of customers
```
SELECT SubscriptionType, COUNT(CustomerID) AS MostPopularSubscriptionType
FROM CustomerData
GROUP BY SubscriptionType
ORDER BY MostPopularSubscriptionType DESC;
```
SubscriptionType | MostSubscriptionType
-----------------|---------------------
Basic            | 16921
Premium	         | 8446     
Standard         | 8420   

---
4. find the total number of active and canceled subscriptions
```
SELECT 
    SUM(CASE WHEN Canceled = 'TRUE' THEN 1 ELSE 0 END) AS TotalCanceled,
    SUM(CASE WHEN Canceled = 'FALSE' THEN 1 ELSE 0 END) AS TotalActive
FROM CustomerData;
```
TotalCanceled | TotalActive
--------------|-------------
15175         | 18612

 ---
## Results and Findings
 ---
 #### The analysis yielded the following quantitative insights from the customer subscription data:

- Total Number of Customers by Region:
North: 8,433 customers
East: 8,488 customers
South: 8,446 customers
West: 8,420 customers

#### The distribution of customers is relatively balanced across regions, with the East leading by a small margin.  

- Most Popular Subscription Type

Basic: 16,921 customers
#### The Basic subscription type is overwhelmingly the most popular, showing a strong preference for the entry-level option.


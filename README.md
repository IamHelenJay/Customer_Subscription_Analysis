# Project Title; Subscription Analysis
---
## Table of Contents
- [Project Overview].(#project-overview)
- [Data Sources].(#data-sources)
- [Data Cleaning and Preparation].(#data-leaning-and-preparation)
- [Exploratory Data Analysis].(exploratory-data-analysis)
- [Data Analysis].(data-analysis)
- [Recommendations](recommendations)
- 
- 
- 

## Project Overview
---
This data analysis project aims to provide insights into customer subscription trends and behavior to support strategic decision-making, The analysis focuses on understanding subscription patterns, cancellation trends, and  top-performing subscription types, regional breakdowns of customer activity. The goal is to enable the company to make data-driven decisions that improve customer satisfaction, reduce churn, and drive revenue growth.


## Data Sources
---
The primary source of data used in this analysis is the CustomerData set https://1drv.ms/u/s!Ap5Z5GRl9j5YhcdWfrVMRJ4XGP4dQQ?e=icEhNj


## Tools Used
---
1. Microsoft Excel [Download here](https://www.microsoft.com)
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

- #### Total Number of Customers by Region:
North: 8,433 customers
East: 8,488 customers
South: 8,446 customers
West: 8,420 customers
The distribution of customers is relatively balanced across regions, with the East leading by a small margin.  

- #### Most Popular Subscription Type
The Basic subscription type with a total of 16,921 customers is overwhelmingly the most popular, showing a strong preference for the entry-level option.

- #### Cancellations Within 6 Months
Total of 15,175 customers canceled their subscriptions within 6 months. This high early churn rate points to potential challenges in customer onboarding or product fit that need addressing to improve retention.

- #### Average Subscription Duration
Average: 365 days

- #### Customers with Subscriptions Longer Than 12 Months
A total 11,820 customers show long-term loyalty, suggesting that there is a segment of committed users.

- #### Total Revenue by Subscription Type:
Basic: $33,776,735
Premium: $16,899,064
Standard: $16,864,376
The Basic subscription generates the most revenue due to its large customer base.

- #### Top 3 Regions by Subscription Cancellations:
North: 5,067 cancellations
South: 5,064 cancellations
West: 5,044 cancellations

- #### Total Active vs. Canceled Subscriptions:
Canceled: 15,175 subscriptions
Active: 18,612 subscriptions
Insight: The number of active subscriptions (18,612) compared to canceled ones (15,175) shows that the company maintains more active subscribers but with a notable proportion of churn.

## Recommendations
---
Based on the results and findings from the customer data analysis, the following recommendations are suggested to improve customer retention, maximize revenue, and enhance customer satisfaction:
- Enhance Onboarding and Early Engagement:
High early cancellation rates suggest potential issues with the initial customer experience.
Implement a structured onboarding program with tutorials, welcome emails, and interactive support during the first three months to engage new customers and reduce churn.

- Develop Loyalty Programs for Long-Term Subscribers:
 While a significant number of customers have subscriptions lasting over 12 months, further enhancing loyalty can maximize retention.
Recommendation: Introduce loyalty rewards that offer exclusive perks, discounts, or added benefits for long-term customers to foster sustained engagement and satisfaction.

- Promote Upgrades to Higher-Tier Subscriptions:
The Basic plan has the most subscribers, but higher-tier plans generate more revenue per customer.
Recommendation: Design targeted marketing efforts that showcase the unique features of Premium and Standard plans, offering personalized promotions to motivate Basic subscribers to upgrade, thus boosting overall revenue.
 

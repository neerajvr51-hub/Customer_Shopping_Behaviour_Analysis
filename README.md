Customer Shopping Behavior & Growth Opportunity Analysis

Project Overview

A retail company wants to better understand customer shopping behavior to improve sales, customer engagement, subscriptions, and product decisions.

This project analyzes 3,900 customer records to understand:

What customers buy

Which categories generate more sales

How customer groups behave

Subscription behavior

Discounts and product performance

Customer ratings

Repeat buying behavior

Note: This is a business-focused Data Analyst project. It does not use machine learning or predictive modeling.

Business Problem

The business wants to use customer shopping data to understand buying patterns and identify simple opportunities to improve sales and customer engagement.

Main business question:

How can the company use customer shopping behavior, product performance, subscription status, and promotional data to identify growth opportunities and make better customer and product decisions?

Business Questions

Which customer groups bring the most sales and records?

Do subscribers spend more than non-subscribers?

Which products and categories are most popular or have better ratings?

How common are discounts across products?

Are repeat buyers more likely to subscribe?

Does shipping type affect average purchase value?

How can purchase frequency and previous purchases help group customers?

Which categories and age groups should get more business attention?

Dataset

The dataset contains 3,900 records and 18 columns before cleaning.

Key information includes:

Age

Gender

Product

Category

Purchase Amount

Location

Size

Color

Season

Review Rating

Subscription Status

Shipping Type

Discount Applied

Payment Method

Previous Purchases

Purchase Frequency

Dataset Limitations

The business problem mentions online and offline sales, but the dataset does not contain a sales channel column, so channel analysis was not performed.

The dataset also does not contain a transaction date, so month-to-month or year-to-year trends cannot be analyzed.

Tools Used

Tool

Purpose

Python / Pandas

Data cleaning, data checks and feature engineering

MySQL

Business analysis using SQL

Power BI

Dashboard and visualization

Project Flow: Python → SQL → Power BI → Business Insights

Python Analysis

The data was checked and prepared in Python.

Main checks included:

Dataset structure

Missing values

Duplicate records

Column names

Numerical values

Categorical values

Data Cleaning

There were 37 missing Review Rating values. The other columns had no missing values.

The missing review ratings were filled using the median rating of the same category.

Other preparation steps:

Standardized column names using lowercase and underscores

Renamed Purchase Amount to purchase_amount

Created an age_group column using age quartiles

Converted purchase frequency into approximate days

Removed promo_code_used because it contained the same information as discount_applied

The aim was to keep the data simple and useful for SQL and Power BI.

SQL Analysis

After cleaning, the data was loaded into MySQL.

SQL was used to answer the main business questions, including:

Revenue by gender

Discounted purchases with above-average spending

Top-rated products

Shipping type comparison

Subscriber vs. non-subscriber behavior

Discount-heavy products

Customer lifecycle grouping

Top products within each category

Repeat buyers and subscription behavior

Revenue by age group

SQL techniques used:

GROUP BY

WHERE

CASE

Subqueries

Aggregate functions

Window functions

Key Findings

1. Category Performance

Clothing is the largest category, with about $104K in sales and 1,737 records.

Accessories is second, with about $74K in sales and 1,240 records.

Together, these two categories account for about $178K of the roughly $233K shown in the category analysis.

2. Customer Age Groups

Young Adults are the top age group, with about $62K in sales and 1,028 records.

Middle-aged customers are next with about $59K and 986 records.

The age groups are relatively balanced, suggesting that different customer groups may need different marketing messages.

3. Subscription

Only 27% of customers are subscribers, while 73% are non-subscribers.

This shows a large group of non-subscribers that could potentially be considered for subscription offers.

Repeat buying behavior should be checked before giving stronger subscription benefits.

4. Customer Spending & Rating

Average purchase amount: $59.76

Average review rating: 3.75 / 5

Power BI Dashboard

The Power BI dashboard brings the main customer and sales results into one page.

Main KPIs

Total Customers

Average Purchase Amount

Average Review Rating

Subscribers %

Filters

Subscription Status

Gender

Category

Shipping Type

The dashboard helps users explore customer behavior and category performance without going through individual SQL queries.

Business Recommendations

1. Focus on the Top Category

Use Clothing as an important category for product planning, bundles and marketing because it has the highest sales and activity.

2. Improve the Subscription Offer

Target non-subscribers based on how often they buy instead of giving the same offer to every customer.

3. Use Different Customer Messages

Use previous purchases and buying frequency to separate customers into:

New

Returning

Loyal

4. Use Discounts Carefully

Review products that depend heavily on discounts. Avoid large discounts on products that already have strong sales.

5. Monitor Customer Ratings

The average rating is 3.75, so customer reviews should be monitored. Low-rated categories or products can be checked for possible product or service issues.

Limitations & Future Analysis

No transaction date, so time trends cannot be analyzed.

No sales channel column, so online vs. offline performance cannot be compared.

The dataset is not detailed enough for full customer lifetime value analysis.

More customer history would be required for deeper cohort analysis.

Useful future data:

Transaction date

Sales channel

Order ID

More customer purchase history

This could support deeper analysis such as customer lifetime value, repeat buying and campaign performance.

Project Structure

Customer-Shopping-Behavior-Analysis/
│
├── data/
│   └── customer_shopping_behavior.csv
│
├── python/
│   └── customer_behavior.ipynb
│
├── sql/
│   └── customer_behavior_sql.sql
│
├── powerbi/
│   └── Customer_Behavior.pbix
│
├── report/
│   └── Customer_Shopping_Behavior_Business_Report.pdf
│
└── README.md

Dashboard Preview

Customer Shopping Behaviour Dashboard

<img width="1471" height="803" alt="image" src="https://github.com/user-attachments/assets/e8833fdd-5bd8-410b-a6c0-06d726745582" />


What I Learned

Through this project, I practiced:

Data cleaning using Python/Pandas

Handling missing values

Basic feature engineering

SQL business analysis

Customer segmentation

Revenue and product analysis

Power BI dashboard design

Turning data findings into business recommendations

Conclusion

This project demonstrates a simple end-to-end Data Analyst workflow:

Python → SQL → Power BI → Business Insights

Python was used to prepare the data, SQL was used to answer business questions, and Power BI was used to present the results.

The main findings show that Clothing and Accessories are the strongest categories, most customers are not subscribers, and customer behavior varies across age groups and previous purchase history.

The goal was to keep

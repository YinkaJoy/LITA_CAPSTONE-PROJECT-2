# LITA_CAPSTONE-PROJECT-2
I will be documenting  my second project on customer behavioural pattern here.

### Project Title: Deyinuad Flexipay Customer Behavioural Analysis

### Project Outline
---

[Project Overview](#project-overview)

[Data Sources](#data-sources)

[Tools Used](#tools-used)

[Data Cleaning and Preparation](#data-cleaning-and-preparation)

[Exploratory Data Analysis](#exploratory-data-analysis)

[Data Analysis](#data-analysis)

[Data Visualization](#data-visualization)

[Recommendations](#recommendations)



### Project Overview
---
The aim of this project is to analyze and understand customer behaviour to gain insights into their purchasing habits, preferences, and pain points. This will enable the organization to:
 1. Enhance customer experience
 2. Improve customer retention
 3. Increase sales and revenue
 4. Optimize marketing strategies


### Data Sources
---
The primary source of Data used is the customer data provided by the organization.

### Tools Used
---
- Microsoft Excel [Download Here](https://1drv.ms/x/c/aad348901d0848c9/EVv2v2mzdsVEgBKDRT5cED4Bf0CpP803ccyhAtIAQ2wbgg)
  1. For Data cleaning
  2. For Analysis.
- SQL - Structured Query Language for querying of Data
- PBI - Microsoft PowerBI for visualization.
- GitHub for portfolio building.

### Data Cleaning and Preparation
---
 In the intial phase when I got the data, I performed the following action;
  1. Data loading and Inspection
  2. Removed duplicates
  3. Data Cleaning and Formatting

### Exploratory Data Analysis
---
For effective analysis, I explored the Data to answer the following questions such as;
 - Retrieve the total number of customers from each region.
 - Find the most popular subscription type by the number of customers.
 - Find customers who canceled their subscription within 6 months.
 - Calculate the average subscription duration for all customers.
 - Find customers with subscriptions longer than 12 months.
 - Calculate total revenue by subscription type.
 - Find the top 3 regions by subscription cancellations.
 - Find the total number of active and canceled subscriptions.
   
### Data Analysis
---
Included are some basic lines of code or queries that were used during my analysis;  

 - To retrieve the total number of customers from each region;

```SQL
SELECT  Region, count(distinct Customerid) as Total_customers 
from [dbo].[CUSTOMERDATA _CAPSTONE]
Group by Region;
```

 - To find the most popular subscription type by the number of customers

```SQL
SELECT top 1 subscriptiontype, count(distinct customerid) as Total_customers
From [dbo].[CUSTOMERDATA _CAPSTONE]
Group by subscriptiontype 
Order by Total_customers desc;
```

 - To calculate the average subscription duration for all customers
```SQL
SELECT avg(datediff(day, subscriptionstart, subscriptionend)) as avg_subscription_duration
From [dbo].[CUSTOMERDATA _CAPSTONE]
```


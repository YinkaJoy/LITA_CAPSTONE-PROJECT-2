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

### Basic statistics about the dataset:
- Total Revenue: $67,540,175
- Total Cancellation Count: 15,175
- Total Renewal Count: 18,612
- Average subscription duration: 365
- Number of distinct Customers: 20
- Number of Region: 4

### Exploratory Data Analysis
---
For effective analysis, I explored the Data to answer the following questions such as;
 - Retrieve the total number of customers from each region.
 - Find the most popular subscription type by the number of customers.
 - Calculate the average subscription duration for all customers.
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


### Data Visualization
---
![CUSTOMER DATA DASH BOARD](https://github.com/user-attachments/assets/1f7bccfd-f910-43d2-ac0c-62620b3998e0)
1. Customer Behaviour: This analysis recorded about 20 distinct customer who subscribe to different subscription type.The analysis identified two distinct customer segments, each with unique characteristics and behaviours.
    
### Insights:
 - Loyal Customer: The are regular subscribers who maintain a particular subscription type and renew regularly.
 - Casual or inactive customers: They do not renew at the end of the subscription duration and there is a high possibility of cancellation.
   
The analysis reveals a challenge in customer retention therefore, there is a need for improvement in the area of customer service.

2. Subscription Trend: There are three subscription types;
      1. Basic
      2. Premiun
      3. Standard
   
![TREND 2](https://github.com/user-attachments/assets/40aae385-1e00-454f-98b0-7cc78470815f)
The chart above shows;
  - Basic have the highest renewal rate and revenue, indicating customer commitment and satisfaction.
  - Premium and Standard maintain close or almost the same position in terms of revenue, renewal and cancellaton rate suggesting flexibility or dissatisfaction
  
### Insights:
  - A pattern in the cancellation count across the susbcription types was indentified, leading to the following assumptions;
       1. that cost is a primary reason for cancellation across all subscription types.
       2. Lack of usage and poor customer support are significant factors for monthly and quarterly cancellations.

  ![RENEWAL AND CANCELLATION TREND 2](https://github.com/user-attachments/assets/b37f8a64-5ae3-4b8d-9c32-a21593330a8d)

   - The Line chart above illustrate the trend of subscription renewal and cancellation across month of the year.
   - There were no renewal in the months of **April**, **September** and **October**. This could be due to a number of factors especially the payment of school fees by parents. Also reducing screen time, 
      internet facilities, poor customer support or technical issues.
   - However, months like **March**, **July**, **November** and **December** recorded no Cancellation. 
          
 ![REGIONAL TREND](https://github.com/user-attachments/assets/7ea7ee51-499e-4db2-980b-ba99c93b3eef)

3. Regional Trend: Amongst the four region, **East** recorded no cancellation indicating a high level of customer satisfaction and commitment
![RENEWAL AND CANCELLATION TREND](https://github.com/user-attachments/assets/1a880dee-b5ae-42d3-849e-92e291395a6c)


### Recommendations
---
The following recommendations are proposed; 
1. Offer flexible subscription plans to reduce cancellations.
2. Improve customer support to address specific monthly cancellation concerns.
3. Provide clear pricing and cost-benefit analysis to alleviate cost concerns.
4. Enhance premium and standard subscription benefits to maintain high renewal rates.
5. Monitor customer usage and engage with inactive customers to prevent cancellations.

### Conclusion
---
Our customer behavioral analysis provides valuable insights into customer preferences, pain points, and behaviors. By implementing targeted strategies, we can enhance customer experience, increase loyalty, and drive business growth.
















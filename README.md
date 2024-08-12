# Toman Bike Shop Sales Analysis (2021-2022)

## Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Recommendations](#recommendations)

### Project Overview

This data analysis project provides comprehensive insights into the sales performance of Toman Bike Shop from 2021 to 2022. This project aims to identify key performance indicators by analyzing various sales metrics and making informed recommendations for improving the company's overall performance. The analysis is designed to help stakeholders gain a deeper understanding of the business's success and areas for growth.

### Data Sources

Sales Data: The primary datasets used for this analysis are "bike_share_yr_0.xlsx" and "bike_share_yr_1.xlsx," containing detailed information about each sale made by Toman Bike Shop.

### Tools

- Excel 
- SQL Server
- Power BI

### Data Cleaning/Preparation

In the initial data preparation phase, I completed the following tasks:

1. Built a database
2. Developed SQL queries
3. Connected Power BI to the database
4. Created a dashboard
5. Made analysis recommendations

### Exploratory Data Analysis

- Hourly Revenue Analysis
- Profit and Revenue Trends
-  Seasonal Revenue
-  Rider Demographics

### Data Analysis
Include some interesting code/features worked with

```sql
with cte as (
select * from bike_share_yr_0
union all
select * from bike_share_yr_1)
select  dteday, season, a.yr, weekday, hr,rider_type, riders, price, COGS, riders*price as revenue,
riders* price -COGS as profit
from cte a
left join cost_table b
on a.yr=b.yr;
```
### Recommendations

- Incremental Price Increase: To test market responsiveness without risking a significant loss of customers, it is recommended to implement a conservative price increase in the range of 10-15%.
- Further Evaluation: Continue to monitor demand closely following the price adjustment. If the market responds positively, consider gradual increases to optimize revenue while maintaining customer satisfaction.

### Results/Findings

- Price Increase Analysis: We analyzed the impact of potential price increases on rider demand. A 10% price increase from the 2022 rate of $4.99 would set the new price at approximately $5.49, while a 15% increase would raise it to around $5.74.
  
- Demand Projection: Our analysis indicates that a 25% price increase would result in an estimated additional revenue of $64 from increased rider demand.









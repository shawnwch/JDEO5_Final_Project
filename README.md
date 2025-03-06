## JDE05_Final_Project

A Data Engineering and Data Analysis project done in a group of 3, based on Historical Data from Olist (a Brazillian E-Commerce website).
- We created a full ETL Pipeline completed to database in Azure Cloud
- Data Analysis on the E-commerce data to find and increase sources of revenue to the company

### In this Data Engineering and Data Analysis project, we had a few Key Objectives:

**1. A Full ETL Pipeline completed to Azure Cloud**
- Using services Azure Databricks, Azure Postgres Flexible Server and Azure Blob Storage
  
**2. Clean the raw data to ensure data accuracy and cleanliness for use**

**3. Answer the following analysis questions:**
- “Which States have the highest Revenue (Sum of Payment Value)?”
- “Which States have the highest Revenue per Customer (Sum of Payment Value / Unique Customer ID)?


### python scripts for Data Cleaning (with subsequent ingestion into Azure using Databricks and a local PostgreSQL backup)
Here would be further explanation of the Data Cleaning steps done using Python scripts:

- Removed duplicates using unidecode library
- strip leading / trailing whitespaces from all string columns using .apply(lambda col: col.str.strip())
- handled null values by using .fillna to replace with the string “N/A”
- converting all columns to the appropriate data types using .astype


### Data Analysis Section with PowerBI
We wanted to answer the following analysis questions:
- “Which States have the highest Revenue (Sum of Payment Value)?”
- “Which States have the highest Revenue per Customer (Sum of Payment Value / Unique Customer ID)?

To find out Revenue, we used the column “Sum of Payment Value” instead of “Price”, because we thought that what matters to the Olist company was the payments entered and made by the customers, and not just the price of the items, which assumes that every customer makes payments.

For the customer counts, we also used “Customer Unique ID” to get the count of non-duplicated customers who may have made multiple orders and payments each.


### Data Analysis Observations
From the above, we discovered that the States with the highest Revenues would be:

1. SP — Sao Paulo at $5,904,640.92 (37.5% of total, and 2.8x that of the 2nd state!)
2. RJ — Rio De Janeiro at $2,104,890.73

However when we looked deeper into Revenues per Customer (Sum of Payment Value / Count of Unique Customer ID), SP — Sao Paulo was actually not the 1st, but the 6th.

1. SC — Santa Catarina at $173.98
2. RJ — Rio De Janeiro at $179.86
6. SP — Sao Paulo at $146.54


### Data Analysis Recommendations
1. The company should definitely continue to focus and build marketing efforts in SP — Sao Paulo.
- SP — 37.5% of total revenue
- Revenue of Brazillian E-commerce market is estimated at $40b in 2024 (www.statista.com)
- SP still has a lot of room to grow for Olist.
  
2. For advertisements, while concentrating on their major markets, Olist could feature slightly lower priced products in SP, while featuring slightly higher priced products in RJ.
- SP — Sao Paulo Revenue per Customer at $146.54
- RJ — Rio De Janeiro Revenue per Customer at $179.86


Thank you for reading! and welcome any questions which you may have. 

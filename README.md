# AdventureWorks Sales Analysis – Business Intelligence Project

This project presents a complete sales performance analysis using the AdventureWorks dataset.
A fully interactive dashboard was built to explore revenue, profitability, customer behavior, sales territories, and time-based performance.

#Project Objective

The objective of this project is to perform an end-to-end Business Intelligence analysis that:

Identifies sales, revenue, and profit trends

Analyzes performance across years, quarters, months, weekdays

Highlights customer purchasing patterns

Compares results across countries and sales territories

Supports decision-making through clean KPIs and visual storytelling

Demonstrates strong skills in data modeling, DAX, and dashboard creation

# Dataset Description

The project uses the AdventureWorksDW sample dataset, containing both fact and dimension tables:

Fact Table

FactInternetSales

SalesAmount

TotalProductCost

OrderQuantity

CustomerKey, ProductKey, SalesTerritoryKey

OrderDate, ShipDate, DueDate

Dimension Tables

DimProduct – product details

DimCustomer – customer attributes

DimGeography – countries & regions

DimSalesTerritory – sales regions

DimDate – complete date hierarchy

This dataset includes thousands of sales records from multiple years.

❓ Business Questions & KPIs
Primary KPIs

🛒 Total Quantity Sold

💰 Total Revenue

🏭 Total Cost of Goods Sold (COGS)

📈 Total Profit

📊 Profit Margin %

🔄 Number of Transactions

Analytical Questions

How do revenue and profit change over years?

Which months and quarters generate the highest profit?

Which weekdays contribute the most to sales?

What is the regional sales performance across countries?

Which time periods make up the majority of the annual profit?

What is the seasonal buying behavior of customers?

🔧 Process / Methodology
1. Data Loading

Imported Excel dataset containing Fact and Dimension tables.

2. Data Cleaning

Converted date keys to proper date format

Checked for missing or inconsistent entries

Validated cost and revenue columns

3. Data Modeling

Built a Star Schema

Connected FactInternetSales with Product, Customer, Date, Geography, Territory

4. DAX Measures (Key Calculations)
Total Revenue = SUM(FactInternetSales[SalesAmount])

Total COGS = SUM(FactInternetSales[TotalProductCost])

Total Profit = [Total Revenue] - [Total COGS]

Profit Margin % = DIVIDE([Total Profit], [Total Revenue])

Total Quantity = SUM(FactInternetSales[OrderQuantity])

Total Transactions = DISTINCTCOUNT(FactInternetSales[SalesOrderNumber])

Profit by Quarter =
CALCULATE([Total Profit], VALUES(DimDate[CalendarQuarter]))

Quarter Profit % =
DIVIDE([Profit by Quarter], CALCULATE([Total Profit], ALL(DimDate)))


(More DAX formulas included inside the project file.)

📈 Dashboard Overview

The final dashboard includes:

KPI cards (Revenue, Profit, Margin, COGS, Qty, Transactions)

Year-over-year trends (2005–2008)

Monthly & seasonal performance

Weekday contribution analysis

Quarterly profit distribution

Country-level performance

Profit contribution summary

(Insert your dashboard image here)

![Dashboard Screenshot](your_image_path_here.png)

🔍 Key Insights
⭐ Overall Performance

Total Revenue: ~$307M

Total Profit: ~$126M

Profit Margin: ~41%
This shows a strong and efficient profitability model.

⭐ Yearly Trends

2007 is the best-performing year in revenue & profit.

Slight decline in 2008, indicating market changes.

⭐ Seasonal Trends

Highest monthly profit occurs in March–June, peaking in May.

Q2 is the strongest quarter with 30.9% of total profit.

Q3 is the weakest, indicating seasonal slowdown.

⭐ Weekday Analysis

Friday, Sunday, Monday show the highest profit.

Weekend buying contributes 44.1% of total profit.

⭐ Country/Territory Insights

Top-performing regions include:

United States

Canada

United Kingdom

Germany

🧾 Conclusion

The AdventureWorks Sales Analysis project provides actionable insights into customer behavior, seasonal patterns, and regional performance.
Key takeaways:

The business is profitable with a high margin (41%).

Q2 and Q4 drive most sales, showing strong seasonal patterns.

Weekend and early-week contribute significantly to profit.

Certain regions dominate profitability, helping focus future marketing and inventory planning.

This project demonstrates strong capability in:

Data modeling

DAX calculations

KPI development

Visualization and storytelling

Business-oriented insights

🛠️ Technologies Used

Power BI

DAX

Excel / AdventureWorksDW

Star Schema Modeling

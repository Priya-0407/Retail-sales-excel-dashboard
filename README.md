## Retail Sales Analysis Dashboard - Style Avenue (Excel)

*Tools used:* Microsoft Excel — Pivot Tables, Pivot Charts, IF & TEXT Formulas, Slicers
----
# Overview:
E-commerce businesses generate large volumes of transaction-level data, but raw data alone doesn't drive decisions, it needs to be cleaned, structured, and turned into a story. This project analyzes a year of retail order data (i.e. 2022) to answer a core business question: who is buying, when, and through which channel, and how should that shape the 2023 sales strategy?

# Dataset:
A retail store - Style Avenue dataset in CSV format containing [31,000+ rows] with the following fields:
Order ID, Customer ID, Gender, Age, Date, Status, Channel, SKU, Category, Size, Qty, Currency, Amount, Ship City, Ship State, Ship Postal Code, Ship Country, B2B

# Step 1: Data Cleaning
The raw data contained inconsistent categorical entries that would have skewed pivot table groupings:
•	Gender column: Mixed entries of M/Men and W/Women were standardized to Men and Women using Find & Replace.
•	Quantity column: Mixed numeric and text entries (1/One, 2/Two) were standardized to numeric values.

# Step 2: Data Processing — Feature Engineering
Two new columns were engineered to support the analysis:
•	Age Group: Built using a nested IF formula on the Age column to bucket customers into age brackets.
•	Month: Extracted from the Date column using a TEXT formula, enabling month-over-month trend analysis.

# Step 3: Analysis
Each business question was answered with a dedicated pivot table and matching visualization:

# Question	Method	Visualization
1. Total sales & orders by month	Pivot table: Month (rows), Amount + Order ID (values)	Combo chart — columns for sales, line for order count
2. Do men or women generate more sales?	Pivot table: Gender (rows), Order ID (values)	Pie chart
3. Top 5 states by sales	Pivot table: State (rows), Amount (values), sorted & filtered to top 5	Bar chart
4. Which age group shops most, by gender?	Pivot table: Age Group (rows), Gender (columns), Order ID (values, % of grand total)	Column chart
5. Which channel drives the most sales?	Pivot table: Channel (rows), Order ID (values, % of grand total)	Pie chart
6. What is the order status?	Pivot table: status (rows), Order ID (values, % of grand total)	Pie chart

# Step 4: Interactive Dashboard
All six visualizations were combined into a single dashboard sheet, with slicers for Month, Channel, and Category linked across every chart, allowing any combination of filters to update the full dashboard view in real time.

# Key Insights
•	March recorded the highest sales and order volume of the year.
•	The majority of orders reached Delivered status.
•	Women generated more total sales than men.
•	Women aged 30–49 are the single highest-spending customer segment.
•	Amazon was the top-performing sales channel, ahead of Flipkart and Myntra.

# Recommendation
To grow sales in 2023, marketing spend should prioritize women aged 30–49 in the top 5 highest-performing states, using targeted ads, offers, and coupons concentrated on the leading channels - Amazon, Flipkart, and Myntra.

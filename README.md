# Online Retail Sales and Customer Analytics

## Project Overview

This project analyzes online retail transactions to understand sales performance, product demand, customer purchasing activity, and geographical sales distribution. Python is used for data cleaning and exploratory data analysis, while Power BI is used to develop an interactive dashboard for business reporting.

The project demonstrates an end-to-end data analytics workflow, from dataset preparation to visualization, business insights, and recommendations.

## Problem Statement

Retail businesses need reliable information about sales trends, product performance, customer activity, and market opportunities. Without structured analysis, it can be difficult to identify seasonal changes, prioritize products, understand geographical concentration, and make informed business decisions.

This project uses transaction data to investigate these areas and present the findings through visualizations and a Power BI dashboard.

## Dataset Description

**Dataset:** Online Retail

**Source:** UCI Machine Learning Repository  
https://archive.ics.uci.edu/dataset/352/online+retail

The dataset contains transaction records from a UK-based online retailer covering December 2010 to December 2011.

The original dataset includes the following columns:

- `InvoiceNo`: Invoice or transaction identifier.
- `StockCode`: Product identifier.
- `Description`: Product description.
- `Quantity`: Number of units in a transaction line.
- `InvoiceDate`: Transaction date and time.
- `UnitPrice`: Price per unit in pounds sterling.
- `CustomerID`: Customer identifier.
- `Country`: Customer's country.

Additional analytical fields, including sales revenue, year, month, and day of the week, are derived during data preparation.

## Tools and Technologies

- Python
- pandas and NumPy
- Matplotlib and Seaborn
- Google Colab
- Power BI
- Git and GitHub

## Data Cleaning and Preparation

The dataset was inspected to identify missing values, duplicate records, incorrect data types, cancellation invoices, and non-positive quantities or prices.

The main sales dataset was prepared by:

1. Removing exact duplicate records.
2. Removing rows missing essential transaction information.
3. Excluding cancellation invoices.
4. Filtering out non-positive quantities and unit prices.
5. Converting transaction dates to a datetime format.
6. Standardizing product descriptions.
7. Removing records with invalid dates or missing product descriptions.
8. Calculating sales revenue by multiplying quantity by unit price.
9. Creating additional date fields for time-based analysis.

Transactions with missing customer identifiers were retained when the other required sales fields were valid. These records can contribute to overall sales analysis but cannot be assigned to identified customers.

The resulting dataset represents positive sales transactions under the cleaning rules described above. Returns and cancellations should be analyzed separately when calculating net sales.

## Exploratory Data Analysis

The analysis investigates:

- Overall sales revenue and units sold.
- Number of distinct invoices and identified customers.
- Monthly sales trends.
- Product-level revenue and quantity sold.
- Sales performance by country.
- Relationships between quantity, unit price, and sales.
- Potential outliers in transaction-line sales values.

Descriptive statistics and visualizations are used to identify important patterns and support business decisions.

## Visualizations

The project includes the following visualizations:

1. Monthly online retail sales trend.
2. Top 10 products by sales revenue.
3. Top 10 countries by sales revenue.
4. Distribution of sales per transaction line.
5. Sales revenue versus unit price.

Each chart includes a meaningful title, axis labels, and an explanation of its business relevance.

## Power BI Dashboard

The **Online Retail Sales Dashboard** summarizes business performance using KPI cards, charts, and an interactive date filter.

The dashboard includes:

- Total Sales.
- Total Units Sold.
- Total Orders.
- Monthly sales trend.
- Top products by sales.
- Top countries by sales.
- Monthly transaction summary.
- Date-range filtering.

The current dashboard displays approximately £10.64 million in sales, 6 million units sold as rounded on the KPI card, and 19,960 orders. The detailed table reports total sales of £10,642,110.80 and total quantity of 5,572,420.

These figures describe the prepared dataset and should be interpreted according to the data-cleaning rules and measure definitions.

## Key Business Insights

### 1. Overall Sales Performance

The dashboard reports total sales of approximately £10.64 million across 19,960 orders. This indicates substantial transaction activity during the reporting period. Sales should also be evaluated alongside profitability and returns.

### 2. Late-Year Sales Increase

Monthly sales rise noticeably from September and reach their highest visible level in November, at approximately £1.5 million. December remains high but shows a slight decline. Further multi-year data would be needed to confirm recurring seasonality.

### 3. Product Revenue Concentration

The product chart shows that DOTCOM POSTAGE has the highest displayed sales value, followed by products including REGENCY CAKESTAND 3 TIER and PAPER CRAFT, LITTLE BIRDIE. Postage-related charges should be distinguished from merchandise when evaluating product demand.

### 4. Geographical Sales Concentration

The United Kingdom contributes approximately £9 million in sales and substantially exceeds the other countries displayed. This indicates strong dependence on the home market and suggests an opportunity to investigate international expansion.

### 5. Variation in Monthly Performance

Monthly sales and order counts vary. December 2010 recorded approximately £821,452 in sales across 1,559 orders, while January 2011 recorded approximately £689,812 across 1,086 orders. Comparing average order value and product mix can help explain these differences.

## Business Recommendations

### 1. Improve Seasonal Planning

Prepare inventory, staffing, and promotional campaigns ahead of the late-year sales increase. Use product-level demand data to reduce stockouts and avoid unnecessary inventory accumulation.

### 2. Investigate International Growth Opportunities

Evaluate lower-sales countries based on delivery costs, demand, purchasing patterns, and potential profitability. Test targeted campaigns in selected markets and assess their results before expanding investment.

### 3. Optimize Product and Inventory Management

Monitor high-demand products while considering profit margins and stock requirements. Analyze postage separately from merchandise to ensure product decisions reflect genuine merchandise demand.

### 4. Strengthen Customer Retention

Use transactions with identified CustomerIDs to study repeat purchases. Consider loyalty initiatives and personalized recommendations, and measure their effectiveness through repeat purchase rate and revenue per identified customer.

### 5. Improve Performance Monitoring

Track sales alongside order volume, average order value, returns, cancellations, and profitability where cost data is available. This provides a more complete view of business performance than revenue alone.

## Limitations

- The dataset covers approximately one year, limiting the ability to confirm recurring seasonal patterns.
- Some transactions have missing customer identifiers, restricting customer-level analysis.
- The main sales dataset excludes cancellation invoices and non-positive quantities and prices, so its revenue should not be described as net sales after returns.
- The dataset does not provide all cost information required to calculate reliable profit margins.

## Conclusion

This project demonstrates how retail transaction data can be transformed into actionable business information using Python and Power BI. The dashboard highlights overall sales activity, monthly fluctuations, product revenue concentration, and the importance of the UK market.

The findings provide a foundation for better inventory planning, international market evaluation, customer retention, and performance monitoring. Further analysis of returns, costs, and customer behavior could strengthen future business decisions.

## Repository Structure

- `data/`: Raw and processed datasets.
- `notebooks/`: Python notebook for data cleaning and EDA.
- `visualizations/`: Charts generated during the analysis.
- `dashboard/`: Power BI dashboard file.
- `reports/`: Final project report.

## Dataset Attribution

Chen, D. (2015). *Online Retail*. UCI Machine Learning Repository.  
https://doi.org/10.24432/C5BW33

Dataset licensed under CC BY 4.0. Refer to the original dataset page for attribution and licensing details.

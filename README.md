# Retail Store Sales Analysis

This project analyzes the sales of products at a retail store to understand customer purchasing patterns, identify top-selling items, and explore opportunities for growth.

## Table of Contents
- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Tools Used](#tools-used)
- [Methodology](#methodology)
- [Key Findings](#key-findings)
- [SQL Queries](#sql-queries)
- [Visualizations](#visualizations)

### Project Overview
The purpose of this analysis is to help a retail store understand its sales data better. By analyzing key metrics like product performance, sales trends, and customer behavior, the store can optimize its inventory and marketing strategies.

### Data Source
The data used for this analysis is sourced from the retail store's sales records, with details on:
- Product categories
- Sales volume
- Revenue generated
- Customer segments

### Tools Used
This project was completed using:
- **Excel** for data cleaning and preliminary analysis.
- **SQL Server** for data processing and querying.
- **Power BI** for data visualization and dashboard creation.

### Methodology
1. **Data Cleaning**: 
   - Removed duplicates and irrelevant columns.
   - Handled missing values to ensure accurate analysis.

2. **Exploratory Data Analysis**:
   - Calculated average sales per product.
   - Identified top-performing product categories.
   - Analyzed seasonal and monthly sales trends.

### Key Findings
- **Total Sales**: Overall sales and monthly trends.
- **Top Products**: List of top-selling products by revenue and volume.
- **Customer Preferences**: Insights into purchasing behavior and high-demand categories.
- **Sales Growth Opportunities**: Areas where sales could potentially be improved.

### SQL Queries
Here are some of the SQL queries used to answer the key questions in the analysis:

#### 1. Total Sales by Product
To calculate the total sales for each product:
```sql
SELECT ProductName, SUM(SalesAmount) AS TotalSales
FROM [LITA Capstone Dataset CSV]
GROUP BY ProductName
ORDER BY TotalSales DESC;
```


#### 2. Top 5 Selling Products
```sql
To find the top 5 products with the highest sales:

SELECT TOP 5 ProductName, SUM(SalesAmount) AS TotalSales
FROM [LITA Capstone Dataset CSV]
GROUP BY ProductName
ORDER BY TotalSales DESC;
```


#### 3. Monthly Sales Trend
```sql
SELECT MONTH(SaleDate) AS SaleMonth, SUM(SalesAmount) AS MonthlySales
FROM [LITA Capstone Dataset CSV]
GROUP BY MONTH(SaleDate)
ORDER BY SaleMonth;
```


#### 4.  Average Sales per Product
```sql
SELECT ProductName, AVG(SalesAmount) AS AverageSales
FROM [LITA Capstone Dataset CSV]
GROUP BY ProductName;
```


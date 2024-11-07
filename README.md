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
- **Excel** [Download Here](https://www.bing.com/ck/a?!&&p=fac614c77962a23d80489414f97b3eb17cbff4bb257b3f23ac21188706a1e54bJmltdHM9MTczMDg1MTIwMA&ptn=3&ver=2&hsh=4&fclid=3a45239c-55f3-6f6c-0fc3-37a154a86ea6&psq=download+excel+2016&u=a1aHR0cHM6Ly9zdXBwb3J0Lm1pY3Jvc29mdC5jb20vZW4tdXMvb2ZmaWNlL2Rvd25sb2FkLWFuZC1pbnN0YWxsLW9yLXJlaW5zdGFsbC1vZmZpY2UtMjAxOS1vZmZpY2UtMjAxNi1vci1vZmZpY2UtMjAxMy03YzY5NWIwNi02ZDFhLTQ5MTctODA5Yy05OGNlNDNmODY0Nzk&ntb=1)  for data cleaning and preliminary analysis.
- **SQL Server** [Download Here](https://www.bing.com/ck/a?!&&p=8a738e8a2f9583b92e6c120f24487c228f8a1049a2e7482c9e2c967782691239JmltdHM9MTczMDg1MTIwMA&ptn=3&ver=2&hsh=4&fclid=3a45239c-55f3-6f6c-0fc3-37a154a86ea6&psq=download+sql+server&u=a1aHR0cHM6Ly93d3cubWljcm9zb2Z0LmNvbS9lbi11cy9zcWwtc2VydmVyL3NxbC1zZXJ2ZXItZG93bmxvYWRzP21zb2NraWQ9M2E0NTIzOWM1NWYzNmY2YzBmYzMzN2ExNTRhODZlYTY&ntb=1) for data processing and querying.
- **Power BI** [Download Here](https://www.bing.com/ck/a?!&&p=a8d7ee4d09253ce1845a2be3c63f78d82b25bccc4ce36e835e904c815893cc00JmltdHM9MTczMDg1MTIwMA&ptn=3&ver=2&hsh=4&fclid=3a45239c-55f3-6f6c-0fc3-37a154a86ea6&psq=download+power+bi&u=a1aHR0cHM6Ly93d3cubWljcm9zb2Z0LmNvbS9lbi11cy9wb3dlci1wbGF0Zm9ybS9wcm9kdWN0cy9wb3dlci1iaS9kb3dubG9hZHM_bXNvY2tpZD0zYTQ1MjM5YzU1ZjM2ZjZjMGZjMzM3YTE1NGE4NmVhNg&ntb=1)  for data visualization and dashboard creation.

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

# Project 1: Sales Analysis of Products for a Retail Store

This project analyzes the sales performance of various products in a retail store using SQL and Power BI.

## Dashboard

Here is a visual representation of the sales analysis dashboard:

![Sales Dashboard](https://github.com/Margnet-data/LITA-CAPSTONE-Project-2/blob/main/sales%20performance%20analysis.png)

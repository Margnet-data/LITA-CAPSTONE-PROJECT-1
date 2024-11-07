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
- [Insights and Recommendations](#insights-and-recommendations)

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

## Visualizations

Here is a visual representation of the sales analysis dashboard:

![Sales Dashboard](https://github.com/Margnet-data/LITA-CAPSTONE-Project-1/blob/main/sales%20performance%20analysis.png)

# Insights and Recommendations

## Data-Driven Story

The sales performance dashboard provides a comprehensive overview of key metrics for a retail store, including total revenue, sales by product and region, monthly sales trends, and customer segmentation. Here's a breakdown of the key insights:

### 1. **Sales Overview**
   - The retail store generated a substantial **Total Revenue of 11M**, which sets a strong foundation for assessing the store's performance across different dimensions.

### 2. **Monthly Sales Trend**
   - The **Monthly Sales Trend** chart shows a decline in sales over the last few months, suggesting a seasonal dip or possible loss of customer interest. This trend signals the need to investigate potential causes, such as market competition or changes in customer preferences, and to implement strategies to boost monthly sales.

### 3. **Product Performance**
   - **Product Sales Analysis** indicates that products like **Shirts** and **Shoes** are top contributors to revenue, whereas **Socks** and **Gloves** show relatively low sales figures. This insight highlights opportunities to optimize stock levels, invest in marketing for low-performing products, or introduce new items to replace consistently underperforming ones.

### 4. **Regional Performance**
   - The **Total Revenue by Region** and **Percentage of Total Sales by Region** visualizations reveal that the **South** region dominates with **46% of total sales**, while other regions (North, East, West) have a smaller share. This dominance suggests the South region as a high-priority market, with potential growth opportunities in other regions.

### 5. **Top 5 Customers by Purchase Amount**
   - The **Top 5 Customers by Purchase Amount** chart shows that specific customers (e.g., Customer1079, Customer1236) account for a large share of purchases. These high-value customers are valuable assets to the business and represent potential for targeted loyalty programs, personalized offers, or premium services to increase retention.

### 6. **Customer Base**
   - With a **Count of 500 Customers**, there is a clear customer base that can be further analyzed for behavior patterns and retention strategies. Understanding customer segments can help in tailoring marketing strategies and improving customer satisfaction.

## Recommendations

Based on the insights gathered, here are some recommendations to improve sales and overall business performance:

1. **Increase Marketing in Low-Performing Regions**:
   - Regions like North, East, and West show lower sales volumes compared to the South. Implement targeted marketing campaigns or promotional offers to boost sales in these regions. Expanding regional marketing efforts can help balance the sales distribution across all regions.

2. **Promote Low-Performing Products**:
   - Products such as **Socks** and **Gloves** have lower sales. Consider bundling these items with popular products like **Shirts** or **Shoes**, or running special discounts to increase their appeal. This strategy can help in optimizing inventory and increasing revenue from underperforming products.

3. **Customer Retention Strategy for Top Buyers**:
   - Engage high-value customers with loyalty programs or exclusive discounts to retain their business. Since a small group of customers contributes significantly to sales, maintaining their loyalty is crucial for sustainable revenue growth.

4. **Address Declining Monthly Sales Trend**:
   - Investigate the reasons behind the decline in monthly sales. Possible factors could include seasonality, market competition, or customer demand shifts. Consider running seasonal promotions, enhancing product visibility, or adapting the product range to revive monthly sales growth.

5. **Product Diversification**:
   - Given the strong performance of **Shirts** and **Shoes**, explore introducing related or complementary products to capitalize on customer demand. Diversifying the product range can attract new customers and provide more options for existing customers.

By implementing these strategies, the retail store can drive more balanced revenue across regions, improve the sales of underperforming products, retain high-value customers, and potentially reverse the declining sales trend. These actions will contribute to a more stable and growing sales performance in the long term.

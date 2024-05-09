# Hot 'n Ready Pies

## Project Overview
This project will provide insights on a year's worth of sales data from a large pizza parlor. We will be analyzing the data to find key performance indicators, as well as trends.
These insights will be conveyed using an excel dashboard.

### Data Source
Sales Data: The primary dataset used for this analysis is the "pizza_sales.csv" file, which contains descriptive information on each transaction made by the company.

### Tools Used
- Excel (Data Processing & Visualization)
- PostgreSQL (Data Analysis)

### MIssion Overview
The goal of this project is to create vizualizations that address the following areas:
  - KPI's
    - Total Revenue
    - Average Order Value
    - Total Pizzas Sold
    - Total Orders
    - Average Pizzas Per Order
  - Trends
    - Daily Trend for Total Orders
    - Hourly Trend for Total Orders
    - Percentage of Sales by Pizza Category
    - Top 5 Best/Worst Sellers

### Exploratory Data Analysis - Code Included
- Total Revenue
 ``` sql
  
SELECT SUM(total_price) Total_revenue
 FROM pizza_db
```
- Average Order Value
 ```sql
  SELECT ROUND(SUM(total_price)/COUNT(DISTINCT order_id),2) AOV
  FROM pizza_db
  ```
 - Total Pizzas Sold
   ``` sql
   SELECT SUM(quantity) pizzas_sold
   FROM pizza_db
   ```
  - Total Orders
    ``` sql
    SELECT COUNT(DISTINCT order_id)
    FROM pizza_db
    ```
- Average Pizzas Per Order
  ``` sql
  ROUND(SUM(quantity)::DECIMAL/COUNT(DISTINCT order_id)::DECIMAL,2) AS PizzaPerOrder
  FROM pizza_db
  ```



    
   

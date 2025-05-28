# 🛒 Sales Analysis Project using MySQL

This project focuses on analyzing sales data using SQL (MySQL). It demonstrates my ability to extract, manipulate, and analyze business data to uncover insights that can assist in strategic decision-making.

## 📌 Objective

To analyze the sales data and derive meaningful business insights using various SQL techniques, including joins, filtering, grouping, window functions, and more.

## 📂 Dataset

- **File Used:** `Sales.csv`
- Contains fields such as:
  - `order_id`
  - `customer_name`
  - `product_name`
  - `category`
  - `ship_mode`
  - `country`, `region`, `city`
  - `order_date`
  - `unit_cost`, `unit_price`, `unit_profit`
  - `total_amount`

## 🧠 Key Insights Derived

- High-value orders shipped via **Economy** mode.
- Country-wise and category-specific sales after a certain date.
- Top 10 most profitable transactions.
- Products and customers with specific name patterns.
- Top 5 cities with highest total sales.
- Total revenue, average unit cost, and number of orders.
- Ranking products by total sales using SQL **RANK()** function.
- Customer order frequency and unique regional data.

## 🛠 SQL Techniques Used

- **Filtering & Sorting**
- **Aggregate Functions**: `SUM()`, `AVG()`, `COUNT()`
- **Grouping**: `GROUP BY`
- **Pattern Matching**: `LIKE`
- **Window Functions**: `RANK() OVER`
- **Pagination**: `LIMIT`, `OFFSET`

## 📁 Files

- `Sales.csv`: Raw sales dataset.
- `Sales_Analysis_Queries.sql`: Contains all SQL queries used for analysis.

## 🧾 Sample Queries

```sql
-- Top 5 cities with highest sales
SELECT city, SUM(total_amount) AS total_sales
FROM sales
GROUP BY city
ORDER BY total_sales DESC
LIMIT 5;

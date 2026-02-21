# 📊 SQL Online Sales Analysis

## 📌 Task Description
This project analyzes online sales data using SQL queries.
The objective is to calculate:

- Total Revenue
- Monthly Revenue
- Best Selling Product
- Average Order Value

---

## 🗂 Database Used
MySQL (db-fiddle.com)

Table: online_sales

Columns:
- order_id
- order_date
- amount
- product_id

---

## 🛠 SQL Queries Used

### 1️⃣ Total Revenue
```sql
##Monthly Revenue
SELECT SUM(amount) AS total_revenue
FROM online_sales;
SELECT 
    YEAR(order_date) AS year,
    MONTH(order_date) AS month,
    SUM(amount) AS monthly_revenue
FROM online_sales
GROUP BY YEAR(order_date), MONTH(order_date)
ORDER BY year, month;
##Best Selling Product
SELECT 
    product_id,
    SUM(amount) AS total_sales
FROM online_sales
GROUP BY product_id
ORDER BY total_sales DESC;
##Average Order Value
SELECT AVG(amount) AS avg_order_value
FROM online_sales;
##Results Summary

Monthly revenue calculated successfully.

Product 104 generated highest revenue.

Sales increased from January to March.

##DB-Fiddle Link
https://www.db-fiddle.com/

Author

Ramisha

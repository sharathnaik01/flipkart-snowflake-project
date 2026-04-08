# 🛒 Flipkart Sales Analysis using Snowflake

## 📌 Project Overview

This project demonstrates how to analyze e-commerce sales data using Snowflake.

## ⚙️ Tech Stack

* Snowflake (Data Warehouse)
* SQL
* CSV Dataset

## 📊 Key Insights

* Total revenue generated
* Top-selling products
* Category-wise performance
* City-wise sales trends

## 🚀 Steps Performed

1. Created table in Snowflake
2. Loaded CSV data using stage
3. Performed SQL analysis

## 📁 Project Structure

* data/ → Dataset
* sql/ → SQL scripts
* README.md → Documentation

## 📷 Sample Queries
![OUTPUT-1](https://github.com/user-attachments/assets/e8c07504-57be-45e1-9c61-8334b761fec5)
![OUTPUT-2](https://github.com/user-attachments/assets/1c381ccd-8abe-40d5-a12d-da522a72ac8f)

```sql
SELECT category, SUM(price * quantity) AS revenue
FROM flipkart_sales
GROUP BY category;
```

## 📌 Outcome

Built a basic data analytics project using Snowflake, useful for data engineering beginners.

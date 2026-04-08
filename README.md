<img width="1536" height="1024" alt="architecture diagram" src="https://github.com/user-attachments/assets/54bd5fa0-7091-4132-a1c9-a9d872c9c246" /># 🛒 Flipkart Sales Analysis using Snowflake

## 📌 Project Overview

This project demonstrates how to analyze e-commerce sales data using Snowflake.

## ⚙️ Tech Stack

* Snowflake (Data Warehouse)
* SQL
* CSV Dataset

## Added architecture diagram for Flipkart Sales Snowflake project

<img width="1536" height="1024" alt="architecture diagram" src="https://github.com/user-attachments/assets/edd0cfad-9328-4884-9c3c-275bfe6a61b8" />


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

## 📷 Sample Output 
![OUTPUT-1](https://github.com/user-attachments/assets/e8c07504-57be-45e1-9c61-8334b761fec5)
![OUTPUT-2](https://github.com/user-attachments/assets/1c381ccd-8abe-40d5-a12d-da522a72ac8f)

```sql
SELECT category, SUM(price * quantity) AS revenue
FROM flipkart_sales
GROUP BY category;

--SELECTING ALL THE DATA ---
SELECT * FROM   flipkart_sales ;


-- Total Revenue--
SELECT SUM(PRICE * QUANTITY) AS TOTAL_REVENUE
FROM FLIPKART_SALES;


--Top 5 Selling Products---
SELECT PRODUCT_NAME,SUM(QUANTITY) AS TOTAL_SALES
FROM FLIPKART_SALES
GROUP BY PRODUCT_NAME
ORDER BY TOTAL_SALES DESC
LIMIT 5;


--Revenue by Category--
SELECT CATEGORY,SUM(PRICE * QUANTITY) AS TOTAL_CATEGORY
FROM FLIPKART_SALES
GROUP BY CATEGORY
ORDER BY TOTAL_CATEGORY DESC;


---City-wise Sales---
SELECT CITY, SUM(PRICE * QUANTITY) AS REVENU
FROM FLIPKART_SALES
GROUP BY CITY
ORDER BY REVENU DESC;

---Payment Method Analysis---
SELECT payment_method, COUNT(*) AS total_orders
FROM flipkart_sales
GROUP BY payment_method;
```

## 📌 Outcome

Built a basic data analytics project using Snowflake, useful for data engineering beginners.

# Online-Sales-Data-Trendora
This Project Involves Data Analysis Based On The Sales Trend
# 🛒 Online Sales Analysis using PostgreSQL

This project demonstrates how I used **PostgreSQL** to analyze an **online sales dataset**. I wrote all SQL queries from scratch based on practical data analysis questions, similar to those faced by data analysts in real-world projects.

---

## 📁 Dataset Overview

The dataset contains transactional records of an online sales business. It includes fields such as:

- Order ID
- Product Name
- Product Category
- Customer ID
- Country
- Order Date
- Ship Date
- Sales
- Quantity
- Discount
- Profit
- Region

---

## 🔧 Tools Used

- **PostgreSQL** for querying and analysis
- **MS Excel** for initial data cleaning and conversion to CSV
- **PgAdmin 4** as the PostgreSQL GUI
- **Snipping Tool** / Screenshot utility for query output capture

---

## 🧹 Data Cleaning Steps

1. Cleaned the dataset in Excel:
   - Removed blank rows and duplicate entries
   - Trimmed extra spaces in headers
   - Saved the final version as `Online_Sales_Trendora.csv`
2. Imported into PostgreSQL using:
   ```sql
   CREATE TABLE online_sales (...);
   COPY online_sales FROM 'path/to/Online_Sales_Trendora.csv' DELIMITER ',' CSV HEADER;

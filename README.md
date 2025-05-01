# 🧾 Sales Data Analysis Using PostgreSQL

This project demonstrates how to analyze a retail company's sales dataset using PostgreSQL. It covers data importing, table creation, and executing various SQL queries to derive actionable business insights.

---

## 📌 Objective

To explore, clean, and analyze a sales dataset using PostgreSQL to uncover key insights such as top-selling products, customer behavior, order trends, and payment method performance.

---

## 🛠️ Tools Used

- **PostgreSQL (PgAdmin 4)** – for writing and executing SQL queries
- **Microsoft Excel** – for initial data cleaning
- **Power BI** *(optional)* – for visualization (can be added later)

---

## 📂 Folder Structure

Sales-Data-Analysis-PostgreSQL/ │ ├── 📁 images/ │ ├── importing_sales_pgadmin.png │ ├── table_creation.png │ ├── top_5_selling_items.png │ ├── overall_total_sales.png │ ├── avg_order_value_payment_method.png │ ├── cancelled_orders_by_city.png │ ├── customers_more_than_two_orders.png │ ├── 📄 README.md ├── 📄 queries.sql └── 📄 sales_dataset.csv


---

## 📥 Step 1: Importing Data

Data was imported into PostgreSQL using the `COPY` command after cleaning it in Excel.

📸 Screenshot:  
![Importing Sales File](images/importing_sales_pgadmin.png)

---

## 🧱 Step 2: Table Creation

Created a structured table with appropriate data types and constraints.

📸 Screenshot:  
![Table Creation](images/table_creation.png)

---

## 🔍 Step 3: Key SQL Queries & Results

### 1️⃣ Top 5 Selling Items
```sql
SELECT item_name, COUNT(*) AS order_count
FROM sales
GROUP BY item_name
ORDER BY order_count DESC
LIMIT 5;
2️⃣ Overall Total Sales
sql
Copy
Edit
SELECT SUM(order_value) AS total_sales FROM sales;
📸

3️⃣ Avg Order Value by Payment Method
sql
Copy
Edit
SELECT payment_method, AVG(order_value)
FROM sales
GROUP BY payment_method;
📸

4️⃣ Cancelled Orders by City
sql
Copy
Edit
SELECT city, COUNT(*)
FROM sales
WHERE order_status = 'Cancelled'
GROUP BY city
ORDER BY COUNT(*) DESC;
📸

5️⃣ Customers with More Than 2 Orders
sql
Copy
Edit
SELECT customer_id, COUNT(*)
FROM sales
GROUP BY customer_id
HAVING COUNT(*) > 2;
📸

📈 Key Insights
Digital payments have a higher average order value.

Certain cities show higher cancellation rates — possible delivery/logistics concerns.

Top 5 items drive significant revenue.

Many loyal customers placed more than 2 orders.

🧠 What I Learned
Practical use of GROUP BY, HAVING, and aggregate functions.

Structuring SQL queries for business needs.

How to derive data-driven insights from raw transactional data.

📬 Contact
Arshdeep Singh
LinkedIn - https://www.linkedin.com/in/arshdeep-singh-900540b0-data-analyst/ |
GitHub
📧 


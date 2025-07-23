# 🛍️ Retail Analytics SQL Project

Welcome to the **Retail Analytics SQL Challenge**, where you'll take on the role of a **Junior Data Analyst** at TechStyle Retail Group. Your job is to extract actionable insights from customer, sales, and product data to help the business drive decisions.

---

## 📌 Project Objective

You’ll use your SQL skills to explore customer behavior, sales performance, and inventory health. The project is designed to test your ability to write analytical queries, join multiple tables, calculate KPIs, and identify inconsistencies in data.

---

## 🗃️ Dataset Overview

The project simulates a simplified retail e-commerce company and contains **four key tables**:

### `CUSTOMERS`
| Column           | Data Type     | Description                  |
|------------------|---------------|------------------------------|
| customer_id      | INT (PK)      | Unique ID for each customer |
| name             | VARCHAR(100)  | Full name of the customer   |
| email            | VARCHAR(100)  | Email address               |
| gender           | VARCHAR(10)   | Gender (Male, Female, Other)|
| registration_date| DATE          | Date of account creation    |
| city             | VARCHAR(100)  | City of residence           |
| country          | VARCHAR(100)  | Country of residence        |

### `PRODUCTS`
| Column          | Data Type     | Description                 |
|-----------------|---------------|-----------------------------|
| product_id      | INT (PK)      | Unique product identifier  |
| name            | VARCHAR(100)  | Product name               |
| category        | VARCHAR(50)   | Product category           |
| price           | DECIMAL(10,2) | Retail price               |
| stock_quantity  | INT           | Available inventory units  |

### `ORDERS`
| Column        | Data Type     | Description                    |
|---------------|---------------|--------------------------------|
| order_id      | INT (PK)      | Unique order identifier        |
| customer_id   | INT (FK)      | Link to customer               |
| order_date    | DATE          | Date the order was placed      |
| total_amount  | DECIMAL(10,2) | Total amount paid by customer  |

### `ORDER_ITEMS`
| Column         | Data Type     | Description                     |
|----------------|---------------|---------------------------------|
| order_item_id  | INT (PK)      | Unique order item ID            |
| order_id       | INT (FK)      | Link to order                   |
| product_id     | INT (FK)      | Link to product                 |
| quantity       | INT           | Number of units purchased       |
| price          | DECIMAL(10,2) | Price at the time of purchase   |

---

## 🧠 Business Questions to Answer

Use SQL to answer the following:

### Sales Analysis
1. What is the monthly revenue trend over the past year?
2. Which product categories generate the most revenue?

### Customer Insights
3. Who are the top 10 customers by lifetime value?
4. What percentage of customers made more than one order?

### Product Performance
5. What are the top 5 best-selling products per category?
6. Which products have high stock but poor sales?

### Operational & Data Quality
7. Are there any orders where `total_amount` doesn’t match the sum of items?
8. Identify duplicate emails in the customer table.

---

## ✅ Deliverables

Each student/team must submit the following:

- A `.sql` file with all your queries
- A `summary.md` or `.pdf` with written explanations for your answers
- A bonus: A SQL View or Stored Procedure for any custom metric (e.g. CLV)

---

## 🔧 Data Generation using Mockaroo

We will use [Mockaroo](https://mockaroo.com) to generate sample data. It’s a powerful tool that allows you to define schemas and generate random data in SQL or CSV format.

### How to Generate Your Dataset

1. Visit [https://mockaroo.com](https://mockaroo.com)
2. Click “Create Schema”
3. For each table (`CUSTOMERS`, `PRODUCTS`, `ORDERS`, `ORDER_ITEMS`), add columns matching the schema above:
   - Use types like **Full Name**, **Email Address**, **Row Number**, **City**, **Country**, **Product**, **Category**, **Decimal**, **Date**, etc.
4. For foreign keys:
   - First generate and export the parent tables (e.g., `CUSTOMERS`)
   - Upload them as **datasets**
   - In child tables, use **Dataset Column** to reference the appropriate keys (e.g., `customer_id`, `product_id`)
5. Choose **SQL** as your export format
6. Set desired row counts:
   | Table        | Rows  |
   |--------------|-------|
   | CUSTOMERS    | 300   |
   | PRODUCTS     | 100   |
   | ORDERS       | 1000  |
   | ORDER_ITEMS  | 2500  |
7. Download the generated `.sql` files and import them into your database

### Video Tutorial
Watch this [Mockaroo Tutorial](https://www.youtube.com/watch?v=_TVTHtm3xXc) for a quick demo on building realistic datasets with mock relationships.

---

## 🧩 Bonus Challenges

- Create a dashboard-friendly KPI view (Revenue, AOV, Repeat Rate, New Customers)
- Use `CASE WHEN`, `CTE`, `JOIN`, and `GROUP BY` effectively
- Document assumptions and limitations in your analysis

---

## 🛠️ Getting Started

1. Import your SQL data into a database (MySQL, PostgreSQL, SQLite, etc.)
2. Explore each table with `SELECT *`
3. Begin answering questions using structured queries

---

## 📩 Questions?

Contact your instructor or raise an issue in the class Slack/Teams channel.

Happy querying!  
— Data Science Bootcamp Team

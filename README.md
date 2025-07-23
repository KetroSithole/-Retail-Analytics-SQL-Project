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

## 🧩 Bonus Challenges

- Create a dashboard-friendly KPI table (Revenue, AOV, Repeat Rate, New Customers)
- Use `CASE WHEN`, `CTE`, `JOIN`, and `GROUP BY` effectively
- Document assumptions and limitations in your analysis

---

## 📁 Getting Started

1. Import the `retail_db.sql` script (provided separately)
2. Use your preferred SQL environment (PostgreSQL, MySQL, SQL Server, SQLite)
3. Begin exploring the data using `SELECT *` statements

---

## 🚀 Tips

- Think like a business analyst, not just a coder
- Explain your logic clearly — use comments in your SQL!
- Prioritize readability and efficiency in your queries

---

## 📩 Questions?

Contact your instructor or raise an issue in the class Slack/Teams channel.

Happy querying!  
— Data Science Bootcamp Team

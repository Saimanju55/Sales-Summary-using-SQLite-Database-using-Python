
📊 Task 7 – Basic Sales Summary using SQLite & Python

 Project Overview

This project demonstrates how to integrate SQL with Python to extract and analyze sales data from a SQLite database.

The objective is to:

Retrieve basic sales summaries

Calculate total quantity and revenue

Visualize results using a bar chart

This task showcases foundational skills required for a Data Analyst role.


🎯 Objective

To use SQL queries inside Python to:

Connect to a SQLite database

Perform data aggregation using GROUP BY

Calculate total revenue

Display results using pandas

Create a bar chart using matplotlib


🛠 Tools & Technologies Used

Python

SQLite (sqlite3)

Pandas

Matplotlib

Jupyter Notebook


🗂 Project Structure

task-7-sqlite-sales-summary/
│
├── task7.ipynb
├── sales_data.db
├── sales_chart.png
└── README.md


🗄 Database Details

Table: sales

Column

Data Type

product

TEXT

quantity

INTEGER

price

REAL


🔎 SQL Queries Used


1️⃣ Product-wise Sales Summary

Copy code

Sql

SELECT

    product,
    SUM(quantity) AS total_quantity,
    SUM(quantity * price) AS revenue
FROM sales
GROUP BY product;

✔ Calculates total quantity sold per product

✔ Calculates total revenue per product


2️⃣ Overall Sales Summary
Sql

SELECT 
    
    SUM(quantity) AS overall_quantity,
    SUM(quantity * price) AS overall_revenue
FROM sales;

✔ Calculates total sales revenue

✔ Calculates overall quantity sold


3️⃣ Top Revenue Product

Sql
SELECT 
    
    product,
    SUM(quantity * price) AS revenue
FROM sales
GROUP BY product
ORDER BY revenue DESC
LIMIT 1;

✔ Identifies the highest revenue-generating product


📊 Data Visualization

A bar chart was created using matplotlib to visualize:

Revenue by Product

The chart was saved using:

Python

plt.savefig("sales_chart.png", dpi=300, bbox_inches='tight')


📈 Key Learnings

How to connect Python to a SQLite database

Writing and executing SQL queries inside Python

Using GROUP BY and aggregate functions

Importing SQL results into pandas DataFrame

Creating basic data visualizations

Saving charts for reporting purposes


🚀 Outcome

By completing this task, I successfully:

✔ Integrated SQL with Python

✔ Performed sales data aggregation

✔ Generated business insights

✔ Created and exported a visualization

✔ Structured the project professionally for GitHub submission


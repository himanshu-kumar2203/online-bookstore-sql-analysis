## Online Bookstore Data Analysis using SQL

## Objective
Analyze an online bookstore dataset to identify sales trends, customer purchasing behavior, and revenue patterns using SQL.

## Dataset
The project uses 3 datasets:
* Books.csv
* Customers.csv
* Orders.csv
These tables are connected using common columns like `Book_ID` and `Customer_ID`.

## SQL Concepts Used
* SELECT, WHERE
* JOIN (Inner, Left Join)
* GROUP BY
* ORDER BY
* Aggregate Functions
* Subqueries

##  Business Questions Solved
* What are the top-selling genres?
* Which customers have placed multiple orders?
* What is the total revenue generated?
* Which book is most frequently ordered?
* Who is the highest spending customer?

##  Key Insights
* Fiction and Fantasy genres contribute the highest share of total sales  
* A small percentage of customers generate a large portion of revenue (high-value customers)  
* High-priced books do not necessarily result in higher sales volume  
* Some books have low stock but high demand, indicating restocking opportunities  

##  Files Included
* Books.csv
* Customers.csv
* Orders.csv
* queries.sql
* project.pdf

##  How to Run
1. Import CSV files into your SQL environment  
2. Create tables for Books, Customers, and Orders  
3. Execute queries from queries.sql

##  Sample Queries
### Total Revenue
```sql
SELECT SUM(total_amount) AS total_revenue
FROM Orders;
```

### Most Frequent Book
```sq2
SELECT Book_ID, COUNT(*) AS order_count
FROM Orders
GROUP BY Book_ID
ORDER BY order_count DESC
LIMIT 1;
```

##  Author
Himanshu Kumar

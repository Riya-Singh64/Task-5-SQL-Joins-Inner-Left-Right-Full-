# Task-5-SQL-Joins-Inner-Left-Right-Full
## Objective:
To retrieve and merge data using SQL joins.

## Tool Used:
- MySQL Workbench

## Tables Used:
- customers
- orders

## SQL Practiced:
- INNER JOIN to fetch matching records from both tables.
- LEFT JOIN to get all records from the left table (`customers`) and matching ones from `orders`.
- RIGHT JOIN to get all records from the right table (`orders`) and matching ones from `customers`.
- FULL OUTER JOIN to combine all records from both tables (handled using `UNION`).

## Queries:
-Inner Join
SELECT customers.name, orders.order_id, orders.amount FROM customers INNER JOIN orders ON customers.customer_id = orders.customer_id;

- Left Join
SELECT customers.name, orders.order_id, orders.amount FROM customers LEFT JOIN orders ON customers.customer_id = orders.customer_id;

- Right Join 
SELECT customers.name, orders.order_id, orders.amount FROM customers RIGHT JOIN orders ON customers.customer_id = orders.customer_id;

- Full Join (using UNION)
SELECT customers.name, orders.order_id, orders.amount FROM customers LEFT JOIN orders ON customers.customer_id = orders.customer_id
UNION
SELECT customers.name, orders.order_id, orders.amount FROM customers RIGHT JOIN orders ON customers.customer_id = orders.customer_id;

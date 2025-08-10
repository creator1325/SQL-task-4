# SQL-task-4



This repo contains example SQL queries for analytics on typical events,products, customers, and sales datasets.

Features

* **Basic Queries:** SELECT, WHERE, ORDER BY
* **Aggregations:** GROUP BY with SUM, COUNT, AVG
* **Joins:** INNER, LEFT, RIGHT
* **Subqueries:** Scalar, Correlated, IN
* **Views:** Example for daily revenue
* **Indexes:** For optimization

Example

sql
-- Daily revenue
SELECT DATE(event_time) AS day,
       SUM(price * quantity) AS revenue
FROM events
WHERE event_type = 'purchase'
GROUP BY day
ORDER BY day DESC;

Optimization

* Use EXPLAIN to check query plans
* Add indexes on event_time, event_type, product_id
* Use range queries instead of DATE() in WHERE

 Usage

1. Adjust table/column names to match your schema
2. Create indexes before running heavy queries
3. Use views/materialized views for frequent aggregations



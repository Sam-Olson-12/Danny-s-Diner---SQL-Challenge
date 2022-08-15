# Danny's Diner
Case study #1 8 Week SQL Challenge

**Question #1** 
What is the total amount each customer spent at the restaurant?

    SELECT customer_id, SUM(price) as sum_price
    FROM dannys_diner.sales 
    JOIN dannys_diner.menu
    ON sales.product_id=menu.product_id
    GROUP BY sales.customer_id;

| customer_id | sum_price |
| ----------- | --------- |
| B           | 74        |
| C           | 36        |
| A           | 76        |

---

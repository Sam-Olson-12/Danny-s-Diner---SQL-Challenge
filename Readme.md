### Summary
This is a personal project that I am doing to improve my SQL skills

---

# Case study #1 8 Week SQL Challenge
### https://8weeksqlchallenge.com/case-study-1/
### Danny's Diner

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

**Question #3**
What was the first item from the menu purchased by each customer?

    SELECT DISTINCT ON (customer_id) customer_id, order_date, product_name
    FROM dannys_diner.sales
    JOIN dannys_diner.menu
    ON sales.product_id = menu.product_id
    ORDER BY customer_id ASC,order_date ASC ;

| customer_id | order_date               | product_name |
| ----------- | ------------------------ | ------------ |
| A           | 2021-01-01T00:00:00.000Z | curry        |
| B           | 2021-01-01T00:00:00.000Z | curry        |
| C           | 2021-01-01T00:00:00.000Z | ramen        |

---

# Case Study #1 - Danny's Diner
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


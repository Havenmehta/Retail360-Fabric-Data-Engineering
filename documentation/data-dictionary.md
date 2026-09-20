# Retail360 Data Dictionary

## Customers

| Column | Description |
|---|---|
| customer_id | Unique customer identifier |
| customer_name | Customer name |
| city | Customer city |
| segment | Customer business segment |
| signup_date | Customer registration date |

## Products

| Column | Description |
|---|---|
| product_id | Unique product identifier |
| product_name | Product name |
| category | Product category |
| unit_price | Product unit price |

## Stores

| Column | Description |
|---|---|
| store_id | Unique store identifier |
| store_name | Store name |
| city | Store location |
| store_type | Store classification |

## Sales

| Column | Description |
|---|---|
| order_id | Unique order identifier |
| order_date | Order transaction date |
| customer_id | Customer reference |
| product_id | Product reference |
| store_id | Store reference |
| quantity | Quantity purchased |
| unit_price | Unit selling price |
| payment_method | Payment method |
| discount_pct | Applied discount percentage |
| gross_amount | Gross transaction amount |
| discount_amount | Discount value |
| net_amount | Final transaction amount |

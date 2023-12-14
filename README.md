# Basic-SQL-Practice-A-Store
Solve 169 exercises grouped into different SQL topics: selecting from one table, JOINs, ORDER BY, GROUP BY, subqueries, and set operations.

The exercises in this online SQL problem set are based on a database for a simple store. We'll work with tables that contain customer, product, purchase, and employee data. 

![image](https://github.com/mythilyram/Basic-SQL-Practice-A-Store/assets/123518126/68c4b290-332c-466f-9117-efbd4b7ba336)

The store database
As you can see, the store database has 6 tables:

The customer table contains the information about the customers. It has the following columns:

customer_id – the ID of the customer (mandatory).
contact_name – the full name of the customer (mandatory).
company_name – the company name (optional).
contact_email – the customer email (mandatory).
address – the address of the customer (optional).
city – the city of the customer (optional).
country – the country of the customer (optional).
The product table contains a list of products available in the store. You can see there the following columns:

product_id – the ID of the product. It can't be NULL.
product_name – the name of the product. It's also mandatory.
category_id – the ID of the product's category. It helps you connect with the category table. It also can't be NULL.
quantity_per_unit – the quantity of product items in one unit. The values in this column aren't mandatory.
unit_price – the price of the product.
units_in_stock – the number of the available units of the product. It can be NULL.
discontinued – the information about whether the product is still available in the store (the FALSE value), or if it has been discontinued (TRUE). The values in this column aren't mandatory.
The category table contains information about the categories of the products:

category_id – the ID of the category. It's mandatory.
name – the category name, also mandatory.
description – the optional description of the category.
parent_category_id – the parent category ID if it's a subcategory, NULL otherwise.
The purchase table contains the information about each order:

purchase_id – the required ID of the purchase.
customer_id – the ID of the customer, also mandatory.
employee_id – the ID of the employee who takes care of the order, mandatory.
total_price – the total price of the order, mandatory.
purchase_date – the timestamp of the purchase. It can be NULL.
shipped_date – the timestamp of the purchase shipment, NULL if unknown.
ship_address – the shipment address, can be NULL.
ship_city – the shipment city, can be NULL.
ship_country – the shipment country, can be NULL.
The purchase_item table connects the purchases with the products. The table contains the following mandatory columns:

purchase_id – the purchase ID.
product_id – the ID of the purchased product.
unit_price – the price of one unit of a product.
quantity – the number of purchased units of a product.
The employee table contains the information about the employees. It has the following columns:

employee_id – the mandatory ID of the employee.
last_name – the last name of the employee, mandatory.
first_name – the first name of the employee, also mandatory.
birth_date – the birth date of the employee, optional.
address – the employee's address, also optional.
city – the employee's city, optional.
country – the employee's country, optional.
reports_to – the ID to an employee to whom the employee reports. It's NULL if the employee doesn't report to anyone.



# E-commerce data analysis using SQL

<img src="/img/order_count.png" width="500" height="">

OBJECTIVE
---

The aim of the project is to improve practical skills related to learning SQL. As an exercise, I conducted an analysis of real e-commerce data provided by the Brazilian online store Olist.
  

JUPYTER NOTEBOOKS  
---

Below are links to Jupyter notebooks with data analytics broken down by area:

  1. [Orders and payments](/notebooks/olist_analysis_1_orders.ipynb)
  2. [Products](/notebooks/olist_analysis_2_products.ipynb)
  3. [Sellers](/notebooks/olist_analysis_3_sellers.ipynb)
  4. Customers
  5. Reviews
  6. Delivery time

BACKGROUND
---

This project uses an open dataset from the Brazilian site Olist. All data and full documentation are available on the Kaggle website. This is anonymized e-commerce data for 100,000 orders covering the period 2016-18. That's a great material for practicing SQL, because we are dealing with a real database that is used in a typical online store.

The Olist platform works as a marketplace. Which means that it connects sellers directly with individual customers. In the database, we will find a lot of information about orders, payments, product prices and shipping, locations of sellers and customers, reviews, and features of individual products.

Thanks to this, we can analyze data from many different perspectives and draw interesting conclusions. In this project, I decided to divide the analysis into several main groups starting with orders, products and sellers.


DATABASE SCHEMA
---

The image above shows the database schema along with the keys that are used to connect individual tables to each other.

The database consists of several tables:
- sellers
- orders
- order_payments
- order_items
- customers
- products
- products_translation
- reviews
- geolocation

All tables have documentation on the Kaggle website that describes the contents of each column in detail. The data is available in csv files (each table in a separate file). For the purposes of this project, I converted them to one SQLite database file called *olist.db*.

Useful information:
- all price-related data in this dataset is expressed in Brazilian real (1 BRL ~ 0.2 USD)
- product names are in Portuguese, they can be translated into English using the table *products_translation*
- the total price of the order (payment_value) is calculated as the sum of the prices (price) of all products and shipping (freight_value) within one order
- within one order (order_id) many products from different categories can be ordered, information on this subject can be found in the *order_items* table


TOOLS
---

The main task in this project was to practice SQL on a real dataset and extract valuable information only with the help of SQL. The entire analysis was performed using Jupyter notebook. In several places there are graphs used to visualize some data.

| Task  |  Tool/package |
|---|---|
| Database type | SQLite|  
| Query language   | SQL |  
| Data Visualization   | matplotlib, seaborn |  
| Environment / Platforms   | Python 3.8+, Jupyter Notebook|  


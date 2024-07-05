# Sales-Insight-on-a-Company-Database
This Repository Contains one of my projects involving analysis of a sales on a company database.

# Data Analysis on the Dataset Using MySQL

--Show all customer records

SELECT * FROM customers;


--Show total number of customers

SELECT count(*) FROM customers;


--Show transactions where currency is US dollars

SELECT * from transactions where currency="USD"


--Show total revenue in year 2020,

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";


--Show transactions for Chennai market (market code for chennai is Mark001

SELECT * FROM transactions where market_code='Mark001';


--Show distrinct product codes that were sold in chennai

SELECT distinct product_code FROM transactions where market_code='Mark001';


--Show transactions in 2020 join by date table

SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;


--Show total revenue in year 2020, January Month,

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");


--Show total revenue in year 2020 in Chennai

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";


# Power BI Dashboard for Analysis

<img width="587" alt="Sales Insight (1)" src="https://github.com/Pravi-Jain/Sales-Insight-on-a-Company-Database/assets/140709107/f02ade51-0a7e-4d90-ad23-779f21ec2302">

<img width="588" alt="Sales Insight (2)" src="https://github.com/Pravi-Jain/Sales-Insight-on-a-Company-Database/assets/140709107/37cb5a9d-4874-49d2-bd64-e59d74c43171">

<img width="588" alt="Sales Insight (3)" src="https://github.com/Pravi-Jain/Sales-Insight-on-a-Company-Database/assets/140709107/aa9a20ae-bc25-4604-8eba-ee5366780a0a">

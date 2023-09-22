## Sales Insights Data Analysis Project

1. SQL database dump is in the db_dump.sql file above. Download the `db_dump.sql` file to your local computer and import it as per the instructions given in the tutorial video

### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

2. Show the total number of customers

    `SELECT count(*) FROM customers;`

3. Show transactions for the Chennai market (the market code for Chennai is Mark001)

    `SELECT * FROM transactions where market_code='Mark001';`

4. Show distinct product codes that were sold in Chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

5. Show transactions where the currency is US dollars

    `SELECT * from transactions where currency="USD"`

6. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

7. Show total revenue in the year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
8. Show total revenue in the year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

9. Show total revenue in the year 2020 in Chennai,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
    and transactions.market_code='Mark001';`






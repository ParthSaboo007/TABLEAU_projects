## Problem Flow Chart

![image](https://user-images.githubusercontent.com/66863370/181909715-e92fb16e-2255-43d4-a65c-2eea3e5026a8.png)


## Data Analysisi using SQL-queries

1. Show total count of sales_amount

      `select count(sales_amount) from sales.transactions;`
   
2. Show average of sale_amount

      `select avg(sales_amount) from sales.transactions;`
      
3. Show all the transactions

      `select * from sales.transactions;`
      
4. Show market code for Chennai market

      `select markets_code from sales.markets where markets_name="Chennai";`
      
5. Show all transactions from R.O. with *Mark001* as market code

      'select  * from sales.transactions where market_code="Mark001";`

6. Show all 5 transactions from R.O. with *Mark001* as market code

      `select  * from sales.transactions where market_code="Mark001" limit 5;`

7. Show count of all transactions in Chennai R.O

      `select count(*) from sales.transactions where market_code="Mark001";`
      
8. Display list of top 10 transactions in terms of sales_amount in chennai R.O.

      `select  * from sales.transactions where market_code="Mark001" order by sales_amount desc limit 10;`
      
9. Show transactions for all years joined by Date Table

      `select sales.transactions.*, sales.date.* from sales.transactions INNER JOIN sales.date ON sales.transactions.order_date = sales.date.cy_date;`
      
10. Display distinct Product_IDs

      `select DISTINCT product_code from sales.transactions;`
      
11. Show full details for *Chennai* store in year = *2020*

      `select sales.transactions.*, sales.date.* from sales.transactions INNER JOIN sales.date ON sales.transactions.order_date = sales.date.date WHERE`                     `market_code="Mark001" AND sales.date.year = 2020;`
      
12. Show transaction details for payment done in *USD*

      `select * from sales.transactions where currency = 'USD';`

## Dashboard-1
![image](https://user-images.githubusercontent.com/66863370/181904334-f287fce4-be58-432d-8a43-994bda3ca354.png)

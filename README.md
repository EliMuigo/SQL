# SQL
It's a programming language used in creation of database and database management.

## CREATING A DATABASE
-First you need to create a database before creating a table .

~~~
CREATE DATABASE customer
USE customer
~~~

### CREATING A TABLE
-Use the CREATE TABLE statement followed by the name of the table.
```

CREATE TABLE Customer_Details
(
    customer_ID VARCHAR(30) PRIMARY KEY,
    name VARCHAR(25),
    Region VARCHAR(20),
    Street_Address VARCHAR(30),
    City VARCHAR(25),
    State VARCHAR(30),
    Zip_code VARCHAR(20)

);


```

~~~


CREATE TABLE product
(
    product_ID VARCHAR(25) PRIMARY KEY,
    Description VARCHAR(30),
    price int,
    manufacture_date DATE,
    year YEAR,

);
~~~

### SELECT STATEMENT
-Used to select data from a database.The select statement retrives and transforms data from table without affecting the table.

~~~
# displays all the details in the table

SELECT *FROM customer_Details;
~~~
~~~
# to display a column in the table
SELECT customer_ID *FROM customer_Details;
~~~
- Expressions used in SELECT statement

~~~
# In calculations
SELECT
product_ID,Description,price,
ROUND(price * 1.07,2) AS Taxed_price
FROM product;
~~~

### Text Concatenation
Use the ( || ) operator
~~~
SELECT name,
city||',' state AS location
FROM customer_Details;
~~~

### WHERE STATEMENT
-Used to filter records.

~~~
SELECT *FROM product
WHERE year=2010;
~~~
~~~
-The NOT operator is (!=)(<>)

SELECT *FROM product
WHERE year!=2010;
~~~
- Including ranges 
~~~
SELECT *FROM product
WHERE year BETWEEN 2005 and 2010;
~~~


### ORDER BY SYNTAX
- Used in sorting data in a table
~~~
SELECT *FROM customer_Details
ORDER BY name;
~~~
We can use descendind(DESC) or ascending(ASC)

### basic 
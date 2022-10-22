# verbose-broccoli
SQL EX
-- SQL Introduction Exercise
  -- Using the bestbuy database:
 -- Copy the following and paste into MySql Workbench

-- find all products 
 SELECT * FROM bestbuy.products;
-- find all products that cost $1400
SELECT * FROM  bestbuy.products
WHERE products.Price = 1400.00;
-- find all products that cost $11.99 or $13.99
 select * from bestbuy.products as p 
 where p.price= 11.99 or p.price= 13.99;
-- find all products that do NOT cost 11.99 - using NOT
 select * from bestbuy.products as x
 where not x.price = 11.99;
-- find  all products and sort them by price from greatest to least
 select * from bestbuy.products as x
 order by x.price desc;
-- find all employees who don't have a middle initial
 select * from bestbuy.employees
 where MiddleInitial is null;

-- find distinct product prices
 select distinct bestbuy.products.price
 from bestbuy.products;
-- find all employees whose first name starts with the letter ‘j’
 select * from bestbuy.employees
 where firstname like 'j%';
-- find all Macbooks 
 select * from bestbuy.products
 where name = 'macbook';
-- find all products that are on sale
 select * from bestbuy.products
 where onsale = 1;
-- find the average price of all products 
 select avg (products.price) from bestbuy.products;
-- find all Geek Squad employees who don't have a middle initial 
 SELECT * FROM bestbuy.employees AS e
WHERE e.MiddleInitial IS NULL AND e.title = 'Geek Squad';

-- find all products from the products table whose stock level is in the range  -- of 500 to 1200. Order by Price from least to greatest. **Use the between keyword** 
SELECT * FROM bestbuy.products
WHERE StockLevel BETWEEN 500 AND 1200
ORDER BY Price;

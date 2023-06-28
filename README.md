# SQL-Query-Log
Log of my general SQL skillsets

# AGGREGATE FUNCTIONS
**AVG(): calculates the average value of the column**

SELECT AVG(column_name) FROM table_name WHERE condition 

**COUNT(): Returns the number of rows that matches the specified conditions**

SELECT COUNT(column_name) FROM table_name WHERE condition

**MIN():  returns minimum value in a column**

SELECT MIN(column_name) FROM table_name WHERE condition

**MAX():  returns maximum value in a column**

SELECT MAX(column_name) FROM table_name WHERE condition

**round(): round a numeric value to a specified number of decimal places**

SELECT ROUND(number, decimal_places)

**SUM(): Calculates sum of values in a column**

SELECT SUM(column_name) FROM table_name WHERE condition

# Alter Table
Allows change to an existing table structure

**Adding columns**

ALTER TABLE table_name

ADD COLUMN new_col TYPE


**Alter constraints**

ALTER TABLE table_name

ALTER COLUMN col_name

SET DEFAULT value

**Example:**

ALTER TABLE companies

MODIFY headquarters_phone_number INT(12) NOT NULL;


# BETWEEN
Used to match value against a range of values

Example:

SELECT * FROM employees WHERE salary BETWEEN 30000 AND 50000;

# Create a table
CREATE TABLE customers

(

	  customer_id INT PRIMARY KEY,
		 
    first_name VARCHAR(255) NOT NULL,
		
    last_name VARCHAR(255) NOT NULL,
		
    email_address VARCHAR(255),
		
    number_of_complaints INT
		
 );    

# CASE
conditional statement to perform different actions based on specified conditions

Example:

 CASE
 
     WHEN rental_duration <=4 THEN 'rental too short'
		 
     WHEN rental_rate>= 3.99 THEN 'too expensive'
		 
     WHEN rating IN('NC-17','R')THEN 'too adult'
		 
     WHEN length NOT BETWEEN 60 and 90 THEN 'too long or too short'
		 
     WHEN description LIKE '%shark%' THEN 'nope it has sharks'
		 
     else 'great reco for my niece'
		 
END AS fit_for_recommendation


# Change Case of String

**LOWER CASE**

SELECT Lower(column_name) 

FROM table_name


**UPPER CASE**

SELECT UPPER(column_name) 

FROM table_name


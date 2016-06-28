# SQL 

* relational database: organizes information into one or more tables 
* table: collection of data organized into rows and columns 
* column: set of data values of a particular type 
* row: single record in a table
* common data types are Integer, Text, Date, Real (decimal value) 

## SQL Statements 
* command, always ends with semi-colon 
* example: 
```sql 
CREATE TABLE table_name(
  column_1 data_type, 
  column_2 data_type,
  column_3 data_type
  );
```

## Commands
* select data from a database (* = select everything) 
  `SELECT * FROM TABLE` 
  `SELECT TOP 50 PERCENT FROM TABLE` 
* return only distinct values
  `SELECT DISTINCT column_name FROM table_name` 
* select data that fulfills criterion 
  `SELECT * FROM table WHERE item = "name"`
* order by sorts data into ascending order by default, specify DESC for descending order
  `SELECT * FROM table ORDER BY column;` 
* insert new values into table 
  ```
  INSERT INTO table_name (column1, column2, column3) 
  VALUES (value1, value2, value3) 
  ```
* delete 
  `DELETE FROM table WHERE column = "value";`

## User Input 
* to get user input, `input = getRequestString("User ID");`

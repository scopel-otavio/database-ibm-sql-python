# Course Overview
The course is structured into 6 weeks, each focusing on a specific topic. 

## Week 1: Getting started with SQL 
This week will let you learn the basics of SQL and databases. You will also learn how to query tables in a database. 

## Week 2: Introduction to Relational Databases and Tables 
This week is all about relational databases, creating tables, and modifying their contents. 

## Week 3: Intermediate SQL 
In this module, you will learn more about different types of SQL queries, functions, string patterns, grouping, and sorting. 

## Week 4: Accessing databases with Python 
This week, you will learn the nuances of accessing databases using Python libraries and SQL magic in Jupyter Notebooks. 

## Week 5: Course Assignment 
This week is designed to give you an understanding of how to deal with real-world datasets and complete an assignment which tests your skills acquired throughout the course.  

## Week 6: Bonus Module: Advanced SQL for Data Engineers
In this additional module, you will learn how to apply advanced queries in SQL, like Views, Stored Procedures, and ACID transactions. 

This course can be applied to multiple Specializations or Professional Certificates programs. Completing this course will count towards your learning in any of the following programs: 

- [Introduction to Data Science Specialization](https://www.coursera.org/specializations/introduction-data-science)
- [IBM Data Engineering Foundations Specialization](https://www.coursera.org/specializations/data-engineering-foundations)
- [IBM Data Analyst Professional Certificate](https://www.coursera.org/professional-certificates/ibm-data-analyst)
- [IBM Data Science Professional Certificate](https://www.coursera.org/professional-certificates/ibm-data-science)
- [IBM Data Engineering Professional Certificate](https://www.coursera.org/professional-certificates/ibm-data-engineer)
- [BI Foundations with SQL, ETL and Data Warehousing Specialization](https://www.coursera.org/specializations/bi-foundations-sql-etl-data-warehouse)
- [IBM Relational Database Administrator Professional Certificate](https://www.coursera.org/professional-certificates/ibm-relational-database-administrator)
- [Data Science Fundamentals with Python and SQL Specialization](https://www.coursera.org/specializations/data-science-fundamentals-python-sql)
  
Upon completion of the course, you will receive a shareable certificate that you can add to your LinkedIn profile. 



# Module 01 - Getting Started with SQL

## BASIC SQL: SELECT statement examples

### Objectives
At the end of this reading, you will learn how to:
- Use various `SELECT` queries to retrieve data from the database.

### SELECT statement usage
`SELECT` is classified as a Database Query command used to retrieve information from a database table. There are various forms in which a SELECT statement is used.

1. The general syntax of a `SELECT` statement retrieves the data under the listed columns from Table_1. The code is:
```sql
SELECT COLUMN1, COLUMN2, ... FROM TABLE_1 ;
```

2. To retrieve all columns from a table, use  `*`  instead of specifying individual column names. The code below retrieves the entire table.
```sql
SELECT * FROM TABLE_1 ;
```

3. Use the `WHERE` clause to filter the required data based on a predicate. The code below filters the response to only the entries that match the predicate.
```sql
SELECT <COLUMNS> FROM TABLE_1 WHERE <predicate>;
```


### SELECT examples
Let's look at these codes in action. Below is a database table called `COUNTRY`, which contains the columns `ID`, `Name`, and `CCode`. Here, `CCode` is a 2 letter country code.

| ID | Name | CCode |
|:---|:---|:---|
| 1 | United States of America | US |
| 2 | China | CH |
| 3 | Japan | JA |
| 4 | Germany | GE |
| 5 | India | IN |
| 6 | United Kingdom | UK |
| 7 | France | FR |
| 8 | Italy | IT |
| 9 | Canada | CA |
| 10 | Brazil | BR |

#### Example #1
When we apply the `SELECT` code ```SELECT * FROM COUNTRY ;```, the query retrieves all rows and columns from the database table named `COUNTRY`.
- `SELECT *` instructs the database to select all columns from the table.
- `FROM COUNTRY` specifies the table from which to retrieve the data. In this case, it's the "COUNTRY" table, so the entire table appears, as shown below.

Response:
| ID | Name | CCode |
|:---|:---|:---|
| 1 | United States of America | US |
| 2 | China | CH |
| 3 | Japan | JA |
| 4 | Germany | GE |
| 5 | India | IN |
| 6 | United Kingdom | UK |
| 7 | France | FR |
| 8 | Italy | IT |
| 9 | Canada | CA |
| 10 | Brazil | BR |



#### Example #2
The SQL query `SELECT ID, Name FROM COUNTRY ;` retrieves specific columns from a database table named `COUNTRY`.
- `SELECT ID, Name` instructs the database to select two specific columns from the table: "ID" and "Name." It will return these two columns for each row that matches the query criteria.
- `FROM COUNTRY` specifies the table from which to retrieve the data, which is the "COUNTRY" table. The table below shows that only the "ID" and "Name" columns were retrieved.

Response:
| ID | Name |
|:---|:---|
| 1 | United States of America |
| 2 | China |
| 3 | Japan |
| 4 | Germany |
| 5 | India |
| 6 | United Kingdom |
| 7 | France |
| 8 | Italy |
| 9 | Canada |
| 10 | Brazil |

#### Example #3
The SQL query `SELECT * FROM COUNTRY WHERE ID <= 5 ;` retrieves all columns from the `COUNTRY` table where the value in the `ID` column is less than or equal to 5.
- `SELECT *` instructs the database to select all columns from the specified table.
- `FROM COUNTRY` specifies the table from which to retrieve the data, which is the `COUNTRY` table.
- `WHERE ID <= 5 ;` is a condition that filters the rows from the table. It will only return rows where the value in the "ID" column is less than or equal to 5. In the table below, you can see that only rows 1-5 were retrieved.

Response:
| ID | Name | CCode |
|:---|:---|:---|
| 1 | United States of America | US |
| 2 | China | CH |
| 3 | Japan | JA |
| 4 | Germany | GE |
| 5 | India | IN |


#### Example #4
The SQL query `SELECT * FROM COUNTRY WHERE CCode = 'CA' ;` retrieves all columns from the `COUNTRY` table where the value in the `CCode` column is equal to `'CA'`.
- `SELECT *` instructs the database to select all columns from the specified table.
- `FROM COUNTRY` specifies the bale from which to retrieve the data, which is the `'COUNTRY'` table.
- `WHERE CCode = 'CA';` is a condition that filters the rows from the table. It will only return rows where the value in the `CCode` column is equal to `'CA'`. In the table below, you will find that only the CA column was retrieved.

Response:
| ID | Name | CCode |
|:---|:---|:---|
| 9 | Canada | CA |

In the lab that follows later in the module, you will apply these concepts and practice more SELECT queries hands-on.

### Summary
In this reading, you learned that:
- `SELECT` is a Database Query command that retrieves information from a database table.
- The `SELECT` statement has various forms depending on what action you require.
- The general syntax will retrieve the data under the listed columns from a named table.
- Use `*` to retrieve all columns from a table without specifying individual column names.
- Use the `WHERE` clause to filter the data based on a predicate.





## BASIC SQL: SQL Cheat Sheet: Basics - SELECT, INSERT, UPDATE, DELETE, COUNT, DISTINCT, LIMIT
Use this cheat sheet for various SQL commands and their syntax, descriptions, and examples.

### SELECT
`SELECT` statement is used to fetch data from a database.
#### Syntax:
```sql
SELECT column1, column2, ... FROM table_name; 
```
#### Example:
```sql
SELECT city FROM placeofinterest;
```

### WHERE
`WHERE` clause is used to extract only those records that fulfill a specified condition.
#### Syntax:
```sql
SELECT column1, column2, ...FROM table_name WHERE condition;
```
#### Example:
```sql
SELECT * FROM placeofinterest WHERE city = 'Rome' ;
```

### COUNT
`COUNT` is a function that takes the name of a column as argument and counts the number of rows when the column is not NULL.
#### Syntax:
```sql
SELECT COUNT * FROM table_name ; 
```
#### Example:
```sql
SELECT COUNT(country) FROM placeofinterest WHERE country='Canada';
```

### DISTINCT
`DISTINCT` function is used to specify that the statement is a query which returns unique values in specified columns.
#### Syntax:
```sql
SELECT DISTINCT columnname FROM table_name;
```
#### Example:
```sql
SELECT DISTINCT country FROM placeofinterest WHERE type='historical';
```

### LIMIT
`LIMIT` is a clause to specify the maximum number of rows the result set must have.
#### Syntax:
```sql
SELECT * FROM table_name LIMIT number;
```
#### Example:
```sql
SELECT * FROM placeofinterest WHERE airport="pearson" LIMIT 5;
```

### INSERT
`INSERT` is used to insert new rows in the table.
#### Syntax:
```sql
INSERT INTO table_name (column1,column2,column3...) VALUES(value1,value2,value3...); 
```
#### Example:
```sql
INSERT INTO placeofinterest (name,type,city,country,airport) VALUES('Niagara Waterfalls','Nature','Toronto','Canada','Pearson');
```

### UPDATE
`UPDATE` used to update the rows in the table.
#### Syntax:
```sql
UPDATE table_name SET[[column1]=[VALUES]] WHERE [condition];
```
#### Example:
```sql
UPDATE placeofinterest SET name = 'Niagara Falls' WHERE name = "Niagara Waterfalls";
```

### DELETE
`DELETE` statement is used to remove rows from the table which are specified in the `WHERE` condition.
#### Syntax:
```sql
DELETE FROM table_name WHERE [condition]; 
```
#### Example:
```sql
DELETE FROM placeofinterest WHERE city IN ('Rome','Vienna');
```
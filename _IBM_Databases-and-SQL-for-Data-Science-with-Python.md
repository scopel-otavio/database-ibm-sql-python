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


















































# MODULE 01 - Getting Started with SQL










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

#### Example 1
When we apply the `SELECT` code ```SELECT * FROM COUNTRY ;```, the query retrieves all rows and columns from the database table named `COUNTRY`.
- `SELECT *` instructs the database to select all columns from the table.
- `FROM COUNTRY` specifies the table from which to retrieve the data. In this case, it's the "COUNTRY" table, so the entire table appears, as shown below.

  Response:

  | IAD | Name | CCode |
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



#### Example 2
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

#### Example 3

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


#### Example 4
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


















































# MODULE 02 - Introduction to Relational Databases and Tables










## Introduction to Relational Databases and Tables: Examples to ALTER and TRUNCATE tables using MySQL
In the previous video, the ALTER and TRUNCATE syntax applies to DB2. There are variations in syntax between different databases. This reading will explore some examples of ALTER and TRUNCATE statements using MySQL.



### Objective(s)
At the end of this reading, you will be able to:
- Use the `ALTER TABLE` statement in the correct syntax.
- Use `TRUNCATE` statements in syntax.
- Execute examples of `ALTER` and `TRUNCATE` statements.



### ALTER TABLE
`ALTER TABLE` statements can be used to **add** or **remove** columns from a table, to modify the data type of columns, to add or remove keys, and to add or remove constraints. The syntax of the `ALTER TABLE` statement is:

#### ADD COLUMN syntax
```sql
ALTER TABLE table_name
ADD column_name data_type;
```
A variation of the syntax for adding column is:
```sql
ALTER TABLE table_name
ADD COLUMN column_name data_type;
```

By default, all the entries are initially assigned the value `NULL`. You can then use `UPDATE` statements to add the necessary column values. For example, to add a **telephone_number** column to the **author** table in the **library** database, the statement will be written as:

```sql
ALTER TABLE author 
ADD telephone_number BIGINT;
```

Here, `BIGINT` is a data type for Big Integer.After adding the entries to the new column, a sample output is shown below.

![img001]

### Modify column data type
```sql
ALTER TABLE table_name
MODIFY column_name data_type;
```
Sometimes, the data presented may be in a different format than required. In such a case, we need to modify the data_type of the column. For example, using a numeric data type for telephone_number means you cannot include parentheses, plus signs, or dashes as part of the number. For such entries, the appropriate choice of data_type is `CHAR`.

To modify the data type, the statement will be written as:
```sql
ALTER TABLE author
MODIFY telephone_number CHAR(20);
```
The entries can then be updated using `UPDATE` statements. An updated version of the "author" table is shown below.

![img002]


### TRUNCATE Table
`TRUNCATE TABLE` statements are used to delete all of the rows in a table. The syntax of the statement is:
```sql
TRUNCATE TABLE table_name;
```
So, to truncate the "author" table, the statement will be written as:
```sql
TRUNCATE TABLE author;
```
The output would be as shown in the image below.
![img003]
Note: The `TRUNCATE` statement will delete the rows and not the table.





## Introduction to Relational Databases and Tables: Examples to CREATE and DROP tables

### Objective(s)
At the end of this lab, you will be able to:
- Create and Drop tables in the database.


### CREATE TABLE statement
In the previous video, we saw the general syntax to create a table:
```sql
CREATE TABLE TableName (
   COLUMN1 datatype,
   COLUMN2 datatype,
   COLUMN3 datatype, 
   ...
);
```

Consider the following examples:
1. Create a TEST table with two columns - ID of type integer and NAME of type varchar. For this, we use the following SQL statement.
```sql
CREATE TABLE TEST (
   ID int,
   NAME varchar(30)
);
```
2. Create a COUNTRY table with an integer ID column, a two-letter country code column, and a variable length country name column. For this, we may use the following SQL statement.
```sql
CREATE TABLE COUNTRY (
   ID int,
   CCODE char(2),
   Name varchar(60)
);
```
3. In the example above, make ID a primary key. Then, the statement will be modified as shown below.
```sql
CREATE TABLE COUNTRY (
   ID int NOT NULL,
   CCODE char(2),
   Name varchar(60),
   PRIMARY KEY (ID)
);
```

In the above example, the `ID` column has the `NOT NULL` constraint added after the datatype, meaning that it cannot contain a `NULL` or an empty value. This is added since the database does not allow Primary Keys to have NULL values.



### DROP TABLE
If the table you are trying to create already exists in the database, you will get an error indicating table XXX.YYY already exists. To circumvent this error, create a table with a different name or first `DROP` the existing table. It is common to issue a `DROP` before doing a `CREATE` in test and development scenarios.

The syntax to drop a table is:
```sql
DROP TABLE TableName;
```

For example, consider that you wish to drop the contents of the table `COUNTRY` if a table exists in the dataset with the same name. In such a case, the code for the last example becomes as follows:
```sql
DROP TABLE COUNTRY;
CREATE TABLE COUNTRY (
   ID int NOT NULL,
   CCODE char(2),
   Name varchar(60),
   PRIMARY KEY (ID)
);
```
**WARNING:** Before dropping a table, ensure it doesn't contain important data that can't be recovered easily.

Note that if the table does not exist and you try to drop it, you will see an error like XXX.YYY is an undefined name. You can ignore this error if the subsequent `CREATE` statement is executed successfully.

In a hands-on lab later in this module, you will practice creating tables and other SQL statements.



## Understanding Relational Model Constraints

### Objectives
After completing this reading, you will be able to:
- Define and identify entity integrity, referential integrity, and domain integrity constraints
- Explain how each constraint maintains data integrity
- Recognize examples of how these constraints are implemented in SQL


### Overview
In any well-designed database, maintaining data integrity is essential to ensure the accuracy, consistency, and reliability of the stored information. This lab focuses on three key relational model constraints:
- Entity Integrity
- Referential Integrity
- Domain Integrity

These constraints enforce rules on how data is stored and related within tables.

Imagine you are building a Database `BookShopDB`. You need to ensure that:
- Each book and author has a unique identifier.
- Every book must be linked to a valid author.
- Attributes like price, title, and date must have values within an acceptable range and format.

This reading will walk you through these constraints with examples to solidify your understanding.

### Sample view of the tables used in this reading
1. BookShop table
This is a sample table structure and data view for the **BookShop** table used in this reading.

![img004]

2. BookShop_AuthorDetails table
This is a sample table structure and data view for the BookShop_AuthorDetails table used in this reading.

![img005]


### Types of relational model constraints

#### Entity integrity constraint
This constraint ensures that every table in a relational database has a **primary key**. A primary key uniquely identifies each row in the table. A primary key column(s):
- must not contain `NULL` values
- must be unique across all rows

This constraint guarantees that each record (or entity) in a table is **distinct and identifiable**, preventing duplication and missing identifiers.

#### Example:
```sql
CREATE TABLE BookShop (
    BOOK_ID INT PRIMARY KEY,
    TITLE VARCHAR(100),
    AUTHOR_ID INT
);
```

#### Explanation
Here, `BOOK_ID` is the **primary key**. It must be:
- Unique (no two books can have the same ID)
- Not NULL (every book must have an ID)

**Note:** Every table in a relational database should have a primary key to satisfy entity integrity.

#### Referential integrity constraint
This constraint ensures that a foreign key in one table always refers to a valid primary key in another table. This maintains consistent and meaningful relationships between tables.

It enforces the logical link between related data in different tables, preventing the existence of invalid or "orphaned" references.

```sql
CREATE TABLE BookShop_AuthorDetails (
    AUTHOR_ID INT PRIMARY KEY,
    AUTHOR_NAME VARCHAR(100)
);

CREATE TABLE BookShop (
    BOOK_ID INT PRIMARY KEY,
    TITLE VARCHAR(100),
    AUTHOR_ID INT,
    FOREIGN KEY (AUTHOR_ID) REFERENCES BookShop_AuthorDetails(AUTHOR_ID)
);
```

#### Explanation
`AUTHOR_ID` in BookShop references `AUTHOR_ID` in **BookShop_AuthorDetails**.

This means every `AUTHOR_ID` in BookShop must exist in BookShop_AuthorDetails.

Trying to insert a book with an AUTHOR_ID that doesn't exist in BookShop_AuthorDetails will fail.

#### Domain integrity constraint
This constraint ensures that all values stored in a column fall within a defined domain. This includes rules about:
- Data type
- Format
- Allowed values
- Nullability

It helps ensure that data in a column is **valid**, **logical**, and **consistent** with its intended use.

**Example:** 
```sql
CREATE TABLE BookShop (
    BOOK_ID INT PRIMARY KEY,
    TITLE VARCHAR(100) NOT NULL,
    PRICE DECIMAL(5, 2) CHECK (PRICE >= 0),
    PUBLISHED_DATE DATE
);
```
#### Explanation
Two standard mechanisms used to enforce domain integrity are the CHECK and NOT NULL constraints:

**1. CHECK Constraint:**

The CHECK constraint enforces rules about the range or pattern of acceptable values within a column. It ensures that the data entered meets specific logical conditions.
- The PRICE column in the example above has a CHECK constraint to ensure it's not negative.

**2. NOT NULL Constraint**

The **NOT NULL** constraint enforces nullability rules, ensuring that a column must contain a value and cannot be left empty (NULL).
- TITLE is NOT NULL. A title must be provided.

### Summary
In this reading, you explored three key types of constraints used in relational databases. By applying these constraints, you can create accurate, consistent, and easy-to-manage databases.





## SQL Scripts - Uses and Applications

### SQL Scripts
SQL scripts are a series of commands or a program that will be executed on an SQL server.

SQL scripts are useful for making complex database changes and can be used to create, modify, or delete database objects such as tables, views, stored procedures, and functions.

### Applications of SQL Scripts
Here are some of the things that you can do with SQL scripts:
- Create tables: You can use SQL scripts to create new tables in your database. This is useful when you need to add new functionality to your application or when you want to store new types of data.
- Drop tables: SQL scripts often have commands to Drop tables from databases. This is especially important before Create table commands to make sure that a table with the same name doesnt exist in the database already.
- Insert data: SQL scripts can also be used to insert data into your tables. This is useful when you need to populate your database with test data or when you want to import data from an external source.
- Update data: You can use SQL scripts to update existing data in your tables. This is useful when you need to correct errors or update records based on changing business requirements.
- Delete data: SQL scripts can also be used to delete data from your tables. This is useful when you need to remove old or obsolete records from your database.
- Create views: Views are virtual tables that allow you to query data from multiple tables as if they were a single table. You can use SQL scripts to create views that simplify complex queries and make it easier to work with your data.
- Create stored procedures: Stored procedures are precompiled SQL statements that can be executed on demand. You can use SQL scripts to create stored procedures that encapsulate complex business logic and make it easier to manage your database.
- Create triggers: Triggers are special types of stored procedures that are automatically executed in response to certain events, such as an insert, update, or delete operation. You can use SQL scripts to create triggers that enforce business rules and maintain data integrity.

### Example: Creating Tables
Let us execute a script containing the CREATE TABLE commands for all the tables in a given dataset, rather than create each table manually by typing the DDL commands in the SQL editor.

Note the following points about these scripts.
1. SQL scripts are basically a set of SQL commands compiled in a single file.
2. Each command must be terminated with a delimiter or terminator. Most often, the default delimiter is a semicolon ;.
3. It is advisable to keep the extension of the file as .sql.
4. Upon importing this file in the phpMyAdmin interface, the commands in the file are run sequentially.

Consider the following script:

```sql
DROP TABLE IF EXISTS PATIENTS;
DROP TABLE IF EXISTS MEDICAL_HISTORY;
DROP TABLE IF EXISTS MEDICAL_PROCEDURES;
DROP TABLE IF EXISTS MEDICAL_DEPARTMENTS;
DROP TABLE IF EXISTS MEDICAL_LOCATIONS;


CREATE TABLE PATIENTS (
  PATIENT_ID CHAR(9) NOT NULL,
  FIRST_NAME VARCHAR(15) NOT NULL,
  LAST_NAME VARCHAR(15) NOT NULL,
  SSN CHAR(9),
  BIRTH_DATE DATE,
  SEX CHAR,
  ADDRESS VARCHAR(30),
  DEPT_ID CHAR(9) NOT NULL,
  PRIMARY KEY (PATIENT_ID)
);

CREATE TABLE MEDICAL_HISTORY (
  MEDICAL_HISTORY_ID CHAR(9) NOT NULL,
  PATIENT_ID CHAR(9) NOT NULL,
  DIAGNOSIS_DATE DATE,
  DIAGNOSIS_CODE VARCHAR(10),
  MEDICAL_CONDITION VARCHAR(100),
  DEPT_ID CHAR(9),
  PRIMARY KEY (MEDICAL_HISTORY_ID)
);

CREATE TABLE MEDICAL_PROCEDURES (
  PROCEDURE_ID CHAR(9) NOT NULL,
  PROCEDURE_NAME VARCHAR(30),
  PROCEDURE_DATE DATE,
  PATIENT_ID CHAR(9) NOT NULL,
  DEPT_ID CHAR(9),
  PRIMARY KEY (PROCEDURE_ID)
);

CREATE TABLE MEDICAL_DEPARTMENTS (
  DEPT_ID CHAR(9) NOT NULL,
  DEPT_NAME VARCHAR(15),
  MANAGER_ID CHAR(9),
  LOCATION_ID CHAR(9),
  PRIMARY KEY (DEPT_ID)
);

CREATE TABLE MEDICAL_LOCATIONS (
  LOCATION_ID CHAR(9) NOT NULL,
  DEPT_ID CHAR(9) NOT NULL,
  LOCATION_NAME VARCHAR(50),
  PRIMARY KEY (LOCATION_ID, DEPT_ID)
);
```

This script incorporates commands to first drop any tables with the mentioned names in the database. After that, the script contains commands to create 5 different tables. All these commands are executed sequentially on the interface.

The contents of this file can be saved in a .sql file format and executed on the phpMyAdmin interface. This can be done by first selecting the database, uploading the SQL script in the provided space, and executing it, as shown in the image below.

![img006]

Upon successful execution of each statement in sequence, an note appears on the interface as shown in the image below. It is also prudent to note that the tables created are now visible in the tree structure on the left under the selected database.

![img007]

You may click any of the tables to see its Table Definition (its list of columns, data types, and so on). The image below displays the structure of the table PATIENTS.

![img008]



### Summary: Relational Database Concepts and Tables

Congratulations! You have completed this lesson. At this point in the course, you know:  
- A database is a repository of data that provides functionality for adding, modifying, and querying the data.  
- SQL is a language used to query or retrieve data from a relational database.  
- The Relational Model is the most used data model for databases because it allows for data independence.  
- The primary key of a relational table uniquely identifies each tuple or row, preventing duplication of data and providing a way of defining relationships between tables.  
- SQL statements fall into two different categories: Data Definition Language (DDL) statements and Data Manipulation Language (DML) statements. 










## SQL Cheat Sheet: CREATE TABLE, ALTER, DROP, TRUNCATE
Use this cheat sheet for various SQL commands and their syntax, descriptions, and examples.



### CREATE TABLE
`CREATE TABLE` statement is to create the table. Each column in the table is specified with its name, data type and an optional keyword which could be `PRIMARY KEY`, `NOT NULL`, etc.,

#### Syntax (MySQL/DB2):
```sql
CREATE TABLE table_name (col1 datatype optional keyword, col2 datatype optional keyword,col3 datatype optional keyword,..., coln datatype optional keyword)
```
#### Example (MySQL/DB2):
```sql
CREATE TABLE employee ( employee_id char(2) PRIMARY KEY, first_name varchar(30) NOT NULL, mobile int);
```



### ALTER TABLE - ADD COLUMN
`ALTER TABLE` statement is used to add the columns to a table.

#### Syntax (MySQL/DB2):

Option 1 -
```sql
ALTER TABLE table_name ADD column_name_1 datatype....ADD COLUMN column_name_n datatype; 
```
Option 2 -
```sql
ALTER TABLE table_name ADD COLUMN column_name_1 datatype....ADD COLUMN column_name_n datatype;
```
#### Example (MySQL/DB2):

Option 1-
```sql
ALTER TABLE employee ADD income bigint;
```
Option 2 -
```sql
ALTER TABLE employee ADD COLUMN income bigint;
```



### ALTER TABLE - ALTER COLUMN
**MySQL:** `ALTER TABLE MODIFY MODIFY` clause is used with the `ALTER TABLE` statement to modify the data type of columns.
**Db2:** `ALTER TABLE ALTER COLUMN` statement is used to modify the data type of columns.

#### Syntax:
MySQL - 
```sql
ALTER TABLE table_name MODIFY column_name_1 new_data_type;
```
DB2 -
```sql
ALTER TABLE table_name ALTER COLUMN column_name_1 SET DATA TYPE datatype;
```

#### Example:
MySQL -
```sql
ALTER TABLE employee MODIFY mobile CHAR(20);
```
DB2 -
```sql
ALTER TABLE employee ALTER COLUMN mobile SET DATA TYPE CHAR(20);
```



### ALTER TABLE - DROP COLUMN
`ALTER TABLE DROP COLUMN`  statement is used to remove columns from a table.

#### Syntax (MySQL/DB2):

ALTER TABLE table_name DROP COLUMN column_name_1 ;
Example (MySQL/DB2):

```sql
ALTER TABLE employee DROP COLUMN mobile ;
```


### ALTER TABLE - RENAME COLUMN
**MySQL:** `ALTER TABLE CHANGE COLUMN` CHANGE COLUMN clause is used to rename the columns in a table.
**DB2:** `ALTER TABLE RENAME COLUMN` statement is used to rename the columns in a table.

#### Syntax:
MySQL -
```sql
ALTER TABLE table_name CHANGE COLUMN current_column_name new_column_name datatype [optional keywords];
```
DB2 - 
```sql
ALTER TABLE table_name RENAME COLUMN current_column_name TO new_column_name;
```

#### Example:
MySQL - 
```sql
ALTER TABLE employee CHANGE COLUMN first_name name VARCHAR(255);
```
DB2 - 
```sql
ALTER TABLE employee RENAME COLUMN first_name TO name;
```



### TRUNCATE TABLE
**MySQL:** `TRUNCATE TABLE` statement is used to delete all of the rows in a table.
**DB2:** The `IMMEDIATE` specifies to process the statement immediately and that it cannot be undone.

#### Syntax:
MySQL -
```sql
TRUNCATE TABLE table_name;
```
DB2 - 
```sql
TRUNCATE TABLE table_name IMMEDIATE;
```

#### Example:
MySQL - 
```sql
TRUNCATE TABLE employee;
```
DB2 -
```sql
TRUNCATE TABLE employee IMMEDIATE ;
```



### DROP TABLE
Use the `DROP TABLE` statement to delete a table from a database. If you delete a table that contains data, by default the data will be deleted alongside the table.

#### Syntax (MySQL/DB2):
```sql
DROP TABLE table_name ;
```
### Example (MySQL/DB2):
```sql
DROP TABLE employee ;
```










## Using IBM Db2 - Hands-on Lab Using IBM DB2

Now that you are familiar with the IBM DB2 database, you can practice the SQL basics concepts learned in this module using DB2. To do so, complete each of the labs below in sequence: 
- [Hands-on Lab: Create Tables using SQL Scripts and Load Data into Tables](https://cf-courses-data.static.labs.skills.network/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/Labs_Coursera_V5/labs/Lab%20-%20Create%20tables%20using%20SQL%20scripts%20and%20Load%20data%20into%20tables/instructional-labs.md.html?t=1770028821)
- [Hands on Lab : CREATE, ALTER, TRUNCATE, DROP Table](https://cf-courses-data.static.labs.skills.network/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/Labs_Coursera_V5/labs/Lab%20-%20CREATE%20-%20ALTER%20-%20TRUNCATE%20-%20DROP/instructional-labs.md.html?t=1770029054)

















































# PUBLIC

[img001]: /_public/img001_Add_column.png
[img002]: /_public/img002_Add_dashes.png
[img003]: /_public/img003_Truncate.png
[img004]: /_public/img004_Screenshot-2025-05-22-163430.png
[img005]: /_public/img005_Screenshot-2025-05-23-170603.png
[img006]: /_public/img006_Screenshot-206.png
[img007]: /_public/img007_Screenshot-207.png
[img008]: /_public/img008_Screenshot-208.png
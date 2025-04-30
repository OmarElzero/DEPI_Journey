# Databases and SQL for Data Science with Python

## Introduction
SQL (Structured Query Language) is a domain-specific language used for managing and manipulating relational databases. This module covers the fundamentals of SQL, from basic queries to advanced data manipulation techniques, specifically with a focus on data science applications.

## Key Concepts

### 1. Database Fundamentals
- **Relational Database**: A collection of data organized in tables with rows and columns
- **Table**: A structured set of data elements organized in rows and columns
- **Primary Key (PK)**: A unique identifier for each record in a table
- **Foreign Key (FK)**: A field that refers to the primary key of another table
- **Schema**: The structure and organization of a database

### 2. SQL Execution Flow
SQL queries follow a logical execution order:
1. FROM clause (identify tables)
2. JOIN clause (combine tables) 
3. WHERE clause (filter rows)
4. GROUP BY clause (aggregate data)
5. HAVING clause (filter groups)
6. SELECT clause (select columns)
7. ORDER BY clause (sort results)
8. LIMIT clause (restrict output)

### 3. Connection to Databases from Python
- Using SQLite for lightweight applications
- Using MySQL for more robust database solutions
- Integration with Python using libraries:
  - `sqlite3` for SQLite
  - `mysql-connector-python` for MySQL
  - `ipython-sql` magic commands for notebooks

## Data Retrieval and Manipulation

### Basic Queries
- **SELECT**: Retrieve data from tables
  ```sql
  SELECT column1, column2 FROM table_name;
  ```
- **WHERE**: Filter rows based on conditions
  ```sql
  SELECT * FROM table_name WHERE condition;
  ```
- **LIMIT**: Restrict the number of rows returned
  ```sql
  SELECT * FROM table_name LIMIT n;
  ```
- **ORDER BY**: Sort the result set
  ```sql
  SELECT * FROM table_name ORDER BY column_name [ASC|DESC];
  ```

### Filtering and Conditions
- **Comparison Operators**: `=`, `<>`, `!=`, `>`, `<`, `>=`, `<=`
- **Logical Operators**: `AND`, `OR`, `NOT`
- **BETWEEN**: Range filtering
  ```sql
  SELECT * FROM table_name WHERE column_name BETWEEN value1 AND value2;
  ```
- **IN**: Multiple value matching
  ```sql
  SELECT * FROM table_name WHERE column_name IN (value1, value2, ...);
  ```
- **LIKE**: Pattern matching with wildcards
  - `%`: Represents zero, one, or multiple characters
  - `_`: Represents exactly one character
  ```sql
  SELECT * FROM table_name WHERE column_name LIKE 'pattern%';
  ```
- **IS NULL/IS NOT NULL**: Handling null values
  ```sql
  SELECT * FROM table_name WHERE column_name IS NULL;
  ```

### Aggregation Functions
- **COUNT()**: Count the number of rows
- **SUM()**: Sum of values in a column
- **AVG()**: Average of values in a column
- **MIN()**: Minimum value in a column
- **MAX()**: Maximum value in a column
- **ROUND()**: Round numeric values
  ```sql
  SELECT COUNT(*), AVG(salary), SUM(salary) FROM employees;
  ```

### Grouping and Having
- **GROUP BY**: Group rows that have the same values
  ```sql
  SELECT column_name, COUNT(*) FROM table_name GROUP BY column_name;
  ```
- **HAVING**: Filter groups based on conditions
  ```sql
  SELECT column_name, COUNT(*) FROM table_name 
  GROUP BY column_name HAVING COUNT(*) > 5;
  ```

## Joining Tables

### Types of Joins
- **INNER JOIN**: Returns records that have matching values in both tables
  ```sql
  SELECT * FROM table1 INNER JOIN table2 ON table1.column = table2.column;
  ```
- **LEFT JOIN**: Returns all records from the left table and matched records from the right table
  ```sql
  SELECT * FROM table1 LEFT JOIN table2 ON table1.column = table2.column;
  ```
- **RIGHT JOIN**: Returns all records from the right table and matched records from the left table
  ```sql
  SELECT * FROM table1 RIGHT JOIN table2 ON table1.column = table2.column;
  ```
- **FULL OUTER JOIN**: Returns all records when there is a match in either left or right table
  ```sql
  SELECT * FROM table1 FULL OUTER JOIN table2 ON table1.column = table2.column;
  ```
- **Self Join**: A join of a table to itself
  ```sql
  SELECT a.column, b.column FROM table_name a, table_name b WHERE condition;
  ```

### Multiple Table Join Strategy
- Join tables appropriately to create meaningful relationships
- Alias tables for readability using `AS` or implicit naming
  ```sql
  SELECT a.name, o.order_date
  FROM accounts a
  JOIN orders o ON a.id = o.account_id;
  ```

## Advanced SQL Techniques

### Subqueries
- A query nested inside another query
  ```sql
  SELECT * FROM orders
  WHERE account_id IN (SELECT id FROM accounts WHERE name = 'Company');
  ```

### Common Table Expressions (CTEs)
- Temporary named result set
  ```sql
  WITH revenue AS (
    SELECT account_id, SUM(total_amt_usd) as total_revenue
    FROM orders
    GROUP BY account_id
  )
  SELECT * FROM revenue WHERE total_revenue > 1000;
  ```

### Date Functions
- Manipulating and formatting date and time values
  ```sql
  SELECT DATE(), DATETIME(), STRFTIME('%Y-%m-%d', date_column) FROM table_name;
  ```

### String Functions
- Manipulating text data
  ```sql
  SELECT LOWER(column), UPPER(column), LENGTH(column) FROM table_name;
  ```

### Case Statements
- Conditional logic in SQL
  ```sql
  SELECT column_name,
    CASE
      WHEN condition1 THEN result1
      WHEN condition2 THEN result2
      ELSE result3
    END AS new_column
  FROM table_name;
  ```

### Views
- Virtual tables based on the result set of a SQL statement
  ```sql
  CREATE VIEW view_name AS
  SELECT column1, column2
  FROM table_name
  WHERE condition;
  ```

## SQL for Data Analysis

### Exploratory Data Analysis with SQL
- Understanding data distributions
  ```sql
  SELECT COUNT(*), MIN(value), MAX(value), AVG(value), STDDEV(value)
  FROM table_name;
  ```
- Finding patterns and relationships
  ```sql
  SELECT category, COUNT(*), AVG(value)
  FROM table_name
  GROUP BY category;
  ```
- Detecting outliers
  ```sql
  SELECT * FROM table_name
  WHERE value > (SELECT AVG(value) + 2*STDDEV(value) FROM table_name);
  ```

### Window Functions
- Perform calculations across rows within a partition
  ```sql
  SELECT column1, column2,
    AVG(column2) OVER (PARTITION BY column1) as avg_by_partition
  FROM table_name;
  ```
- Ranking functions
  ```sql
  SELECT column1,
    RANK() OVER (ORDER BY column2 DESC) as rank
  FROM table_name;
  ```

## Best Practices for SQL in Data Science

1. **Write Readable Code**:
   - Use consistent indentation and capitalization
   - Break complex queries into smaller parts

2. **Optimize Performance**:
   - Use indexes for frequently queried columns
   - Avoid SELECT * when possible
   - Limit the result set size

3. **Handle Missing Data Appropriately**:
   - Understand NULL values and their impact
   - Use appropriate functions for missing data

4. **Document and Comment SQL Code**:
   - Add comments to explain complex logic
   - Document the purpose of views and temporary tables

5. **Test SQL Queries**:
   - Verify results with smaller datasets
   - Use LIMIT to test on a subset of data

6. **Use Transactions for Data Modifications**:
   - Wrap insert, update, and delete operations in transactions
   - Use COMMIT and ROLLBACK appropriately

## Key Definitions

- **SQL (Structured Query Language)**: A standard language for accessing and manipulating databases.
- **RDBMS (Relational Database Management System)**: Software that enables users to interact with a relational database.
- **Query**: A request for data or information from a database.
- **Table**: A collection of related data held in a structured format within a database.
- **Record/Row**: One entry in a table, with values for each column.
- **Column/Field**: A vertical category of data in a table.
- **Primary Key**: A column or group of columns that uniquely identifies each row in a table.
- **Foreign Key**: A column that creates a relationship with another table's primary key.
- **Index**: A data structure that improves the speed of data retrieval operations on a table.
- **Join**: Combines rows from two or more tables based on a related column.
- **Aggregate Function**: A function that performs a calculation on a set of values and returns a single value.
- **Transaction**: A unit of work performed within a database management system.
- **Normalization**: The process of organizing data to reduce redundancy and improve data integrity.
- **Schema**: The structure of a database system, described in a formal language supported by the DBMS.
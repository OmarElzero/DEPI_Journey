# Databases and SQL for Data Science Quiz

## Basic SQL Concepts

1. **Which SQL clause is used to retrieve data from one or more tables?**
   - [ ] FETCH
   - [x] SELECT
   - [ ] EXTRACT
   - [ ] QUERY

2. **Which clause is used to filter rows in a SQL query?**
   - [ ] FILTER
   - [ ] HAVING
   - [x] WHERE
   - [ ] RESTRICT

3. **What does the SQL keyword DISTINCT do?**
   - [ ] Sorts data in distinct order
   - [ ] Separates query results into distinct groups
   - [x] Removes duplicate rows from the result set
   - [ ] Distinguishes between NULL and non-NULL values

4. **Which operator is used to check if a value falls within a range in SQL?**
   - [ ] WITHIN
   - [x] BETWEEN
   - [ ] RANGE
   - [ ] FROM-TO

5. **Which wildcard character represents any series of characters in a SQL LIKE pattern?**
   - [ ] ?
   - [ ] *
   - [x] %
   - [ ] #

## SQL Aggregation and Grouping

6. **Which function is used to find the average of a set of values?**
   - [ ] MEAN()
   - [x] AVG()
   - [ ] AVERAGE()
   - [ ] MIDDLE()

7. **Which clause is used to filter groups in SQL?**
   - [ ] WHERE
   - [ ] FILTER
   - [x] HAVING
   - [ ] GROUP FILTER

8. **What is the correct syntax for grouping results by multiple columns?**
   - [ ] GROUP BY column1 AND column2
   - [x] GROUP BY column1, column2
   - [ ] GROUP BY (column1, column2)
   - [ ] GROUP BY column1 & column2

9. **Which of these is NOT an aggregate function in SQL?**
   - [ ] SUM()
   - [ ] MAX()
   - [x] MEDIAN()
   - [ ] COUNT()

10. **What happens if you include a column in the SELECT clause that is not in the GROUP BY clause and is not wrapped in an aggregate function?**
    - [ ] The query will work correctly
    - [x] The query will produce an error (in most SQL implementations)
    - [ ] The column will be automatically aggregated
    - [ ] All values of that column will be shown

## SQL Joins

11. **Which JOIN type returns only the matching rows between two tables?**
    - [x] INNER JOIN
    - [ ] FULL OUTER JOIN
    - [ ] LEFT JOIN
    - [ ] RIGHT JOIN

12. **In a LEFT JOIN, if there is no match in the right table, what values appear for the right table's columns?**
    - [ ] Default values like 0 or empty strings
    - [x] NULL values
    - [ ] The row is not included in the results
    - [ ] Error message

13. **When joining tables, which condition is typically used in the ON clause?**
    - [ ] Any logical condition is equally good
    - [ ] The WHERE conditions from both tables
    - [x] The relationship between primary and foreign keys
    - [ ] The shared column names

14. **How many tables can be joined in a single SQL query?**
    - [ ] Maximum of two tables
    - [ ] Maximum of three tables
    - [ ] Maximum depends on the SQL dialect
    - [x] There is no specific limit

15. **What type of JOIN would you use to include all records from both tables, regardless of whether there are matching values?**
    - [ ] INNER JOIN
    - [x] FULL OUTER JOIN
    - [ ] CROSS JOIN
    - [ ] NATURAL JOIN

## Advanced SQL

16. **What is a subquery in SQL?**
    - [ ] A query that runs before the main query
    - [x] A query nested inside another query
    - [ ] A query that runs on a subset of a table
    - [ ] A query that divides data into subgroups

17. **What does CTE stand for in SQL?**
    - [x] Common Table Expression
    - [ ] Conditional Table Evaluation
    - [ ] Complex Table Entity
    - [ ] Cross Table Extension

18. **Which SQL keyword introduces a Common Table Expression?**
    - [x] WITH
    - [ ] USING
    - [ ] SET
    - [ ] CREATE

19. **Which SQL feature allows you to apply conditional logic to determine values in a result set?**
    - [ ] IF-THEN
    - [x] CASE
    - [ ] WHEN-ELSE
    - [ ] SWITCH

20. **What is a Window Function in SQL?**
    - [ ] A function that works only on a specific time window
    - [ ] A function that creates views or "windows" of the data
    - [x] A function that performs calculations across rows related to the current row
    - [ ] A function that splits data into separate windows or partitions

## SQL in Data Science

21. **Which Python library provides integration between pandas and SQL?**
    - [ ] sql-python
    - [ ] py-sql
    - [x] sqlite3/sqlalchemy
    - [ ] pandas-sql

22. **When working with large datasets in SQL, which is generally more efficient?**
    - [ ] Retrieving all data and filtering in Python
    - [x] Filtering data in SQL before retrieving it
    - [ ] Using multiple small queries instead of one complex query
    - [ ] Converting SQL data to CSV first

23. **Which feature in SQL is especially useful for time series analysis?**
    - [ ] JOIN operations
    - [ ] LIKE patterns
    - [x] Window functions
    - [ ] GROUP BY clauses

24. **Which database type would typically be most appropriate for handling highly structured, relational data in a data science project?**
    - [x] SQL database (like PostgreSQL, MySQL)
    - [ ] Document store (like MongoDB)
    - [ ] Key-value store (like Redis)
    - [ ] Graph database (like Neo4j)

25. **Which approach is generally better for performing aggregations on large datasets?**
    - [ ] Retrieving all data and using pandas for aggregation
    - [x] Performing aggregations in SQL before retrieving the results
    - [ ] Always using a NoSQL database for aggregations
    - [ ] Splitting the data into smaller chunks first

## Answers

1. SELECT
2. WHERE
3. Removes duplicate rows from the result set
4. BETWEEN
5. %
6. AVG()
7. HAVING
8. GROUP BY column1, column2
9. MEDIAN()
10. The query will produce an error (in most SQL implementations)
11. INNER JOIN
12. NULL values
13. The relationship between primary and foreign keys
14. There is no specific limit
15. FULL OUTER JOIN
16. A query nested inside another query
17. Common Table Expression
18. WITH
19. CASE
20. A function that performs calculations across rows related to the current row
21. sqlite3/sqlalchemy
22. Filtering data in SQL before retrieving it
23. Window functions
24. SQL database (like PostgreSQL, MySQL)
25. Performing aggregations in SQL before retrieving the results
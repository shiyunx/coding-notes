## Basic & Intermediate SQL

### Create Table

    CREATE TABLE table_name (
    column1 datatype constraints,
    column2 datatype constraints
    );

<br>

    CREATE TABLE users (
    id INT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE,
    salary DECIMAL(10,2),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
    );

> Data Types

- `INT`: whole numbers
- `DECIMAL` (p,s) (total digitals, decimal digitals): Money, Precise Values
- `VARCHAR(n)`: Text
- `TEXT`: Long text
- `DATE`: Date
- `TIMESTAMP`: Date + Time
- `BOOLEAN`: True, False

> Constraints

- `PRIMARY KEY`: Unique ID
- `NOT NULL`: Required field
- `UNIQUE`: No duplicates
- `FOREIGN KEY`: Link tables
- `DEFAULT`: Preset value
- `REFERENCES`: Link between tables

### Comments

    -- Add sql comment

### Drop Table

    DROP TABLE table_name;

### Insert

> Insert data into one row

    INSERT INTO table_name (column1, column2)
    VALUES ('value1', 'value2');

> Insert data into multiple rows

    INSERT INTO table_name (column1, column2)
    VALUES 
    ('value1', 'value2'),
    ('value3', 'value4');

### Update

    UPDATE table_name
    SET column1 = 'new_value'
    WHERE condition;

### Delete

> Delete all

    DELETE FROM table_name;

> Filter and delete

    DELETE FROM table_name
    WHERE condition;

### Alias

> Rename column & table

    SELECT column1 AS new_name
    FROM table_name AS t;

### Alter Table

> Modify an existing table and add a new column1

      ALTER TABLE table_name
      ADD column1 TEXT;

### Select

> Select all columns
    
    SELECT *
    FROM table_name;

> Select more than one columns
    
    SELECT column1, column2
    FROM table_name;

### Where

- `WHERE`: Filters rows before grouping.

> Filter one condition

    SELECT column1, column2
    FROM table_name
    WHERE condition;

> Filter multiple conditions (AND)

    SELECT column1
    FROM table_name
    WHERE condition1 AND condition2;

> Filter multiple conditions (OR)

    SELECT column1
    FROM table_name
    WHERE condition1 OR condition2;

> Filter multiple conditions (NOT)

    SELECT column1
    FROM table_name
    WHERE NOT condition;

### Order By

> Sort by ASC

    SELECT column1, column2
    FROM table_name
    ORDER BY column1 ASC;

> Sort by DESC

    SELECT column1, column2
    FROM table_name
    ORDER BY column1 DESC;

> Sort by multiple columns

    SELECT column1, column2
    FROM table_name
    ORDER BY column1 ASC, column2 DESC;

### Select, Where, Order by
    SELECT column1, column2
    FROM table_name
    WHERE condition
    ORDER BY column1;

### Limit

- `LIMIT`: How many rows to return

      SELECT column1
      FROM table_name
      LIMIT 5;

### Offset

- `OFFSET`: How many rows to skip

      SELECT column1
      FROM table_name
      LIMIT 5 OFFSET 10;

### Distinct

- `DISTINCT`: Shows only unique values (remove duplicates)

> Select one column

    SELECT DISTINCT column1
    FROM table_name;

> Select multiple columns

    SELECT DISTINCT column1, column2
    FROM table_name;

### Aggregation

- `COUNT(*)`: Counts the number of rows in each group.

> Counts all rows

    SELECT COUNT(*) 
    FROM table_name;

> Counts only rows where column1 is not NULL

    SELECT COUNT(column1)
    FROM table_name;

> Sum

    SELECT SUM(column1)
    FROM table_name;

> Average

    SELECT AVG(column1)
    FROM table_name;

> Minimun & Maximun

    SELECT MIN(column1), MAX(column1)
    FROM table_name;

### Group By

- `GROUP BY`: Group similar rows and summarise each group.

      SELECT column1, COUNT(column2)
      FROM table_name
      GROUP BY column1;

### Having

- `HAVING`: Filters groups after grouping.

      SELECT column1, COUNT(*) AS alias_name
      FROM table_name
      GROUP BY column1
      HAVING COUNT(*) > N;

<br>

      SELECT column1, COUNT(column2)
      FROM table_name
      GROUP BY column1
      HAVING COUNT(column2) > 5;

### Null

- `IS NULL`: Checks if a column has no value.
- `IS NOT NULL`: Checks if a column has a value.

> IS NULL

      SELECT column1
      FROM table_name
      WHERE column2 IS NULL;

> IS NOT NULL

      SELECT column1
      FROM table_name
      WHERE column2 IS NOT NULL;

> Check NULL

    SELECT *
    FROM table_name
    WHERE column1 IS NULL;

> Replace NULL

     SELECT COALESCE(column2, 0)
     FROM table_name;

### Join

- `JOIN`: Matches rows with the same value in common column.

> Join one column

    SELECT a.column1, a.column2, b.column3
    FROM table1 a
    JOIN table2 b
    ON a.common_column = b.common_column;

> Join multiple columns

    SELECT a.column1, b.column2
    FROM table1 a
    JOIN table2 b
    ON a.column1 = b.column1 AND a.column2 = b.column2;

> Join different operators

    SELECT a.column1, b.column2
    FROM table1 a
    JOIN table2 b
    ON a.date_column < b.date_column;

> Join with aliases

    SELECT t1.name, t2.salary
    FROM employees t1
    JOIN payroll t2
    ON t1.emp_id = t2.emp_id;

> Join with functions

    SELECT a.column1, b.column2
    FROM table1 a
    JOIN table2 b
    ON YEAR(a.date) = YEAR(b.date);

> Join multiple tables

    SELECT a.col1, b.col2, c.col3
    FROM table1 a
    JOIN table2 b
    ON a.id = b.id
    JOIN table3 c
    ON b.id = c.id;

> Join with WHERE

    SELECT a.col1, b.col2
    FROM table1 a
    JOIN table2 b
    ON a.id = b.id
    WHERE b.status = 'Active';

- `INNER JOIN`: Only matching rows from both tables.
- `LEFT JOIN`: All rows from left table; matching rows from right table; NULL if no match.
- `RIGHT JOIN`: All rows from right table; matching rows from left table; NULL if no match.
- `FULL OUTER JOIN`: All rows from both tables; NULL where there’s no match.
- `CROSS JOIN`: Cartesian product of both tables (all combinations).
- `SELF JOIN`: Join a table to itself using aliases.

> Inner Join

    SELECT column1, column2
    FROM table1
    INNER JOIN table2
    ON table1.column1 = table2.column1;

> Left Join

    SELECT column1, column2
    FROM table1
    LEFT JOIN table2
    ON table1.column1 = table2.column1;

> Right Join

    SELECT column1, column2
    FROM table1
    RIGHT JOIN table2
    ON table1.column1 = table2.column1;

> Full Outer Join

    SELECT table1.column1, table2.column2
    FROM table1
    FULL OUTER JOIN table2
    ON table1.common_column = table2.common_column;

> Cross Join

    SELECT table1.column1, table2.column2
    FROM table1
    CROSS JOIN table2;

> Self Join

    SELECT a.column1, b.column2
    FROM table1 a
    INNER JOIN table1 b
    ON a.common_column = b.common_column;

### Case When

- `CASE`: IF...ELSE

      SELECT column1,
      CASE 
          WHEN condition THEN 'result1'
          WHEN condition THEN 'result2'
          ELSE 'other'
      END AS new_column
      FROM table_name;

### Subquery (Where)

    SELECT column1
    FROM table_name
    WHERE column2 IN (
       SELECT column2
       FROM table_name2
       WHERE condition
    );

### Correlated Subquery
    
    SELECT column1
    FROM table_name t1
    WHERE column2 > (
        SELECT AVG(column2)
        FROM table_name t2
        WHERE t1.column1 = t2.column1
    );

### Exists

    SELECT column1
    FROM table_name t1
    WHERE EXISTS (
        SELECT 1
        FROM table_name2 t2
        WHERE t1.column1 = t2.column1
    );

### Window Functions (Over)

> ROW_NUMBER

    SELECT column1,
           ROW_NUMBER() OVER (PARTITION BY column1 ORDER BY column2 DESC) AS rn
    FROM table_name;

> RANK

    SELECT column1,
       RANK() OVER (ORDER BY column2 DESC) AS rank_value
    FROM table_name;

### Partition + Aggregation

    SELECT column1,
           SUM(column2) OVER (PARTITION BY column1) AS total_value
    FROM table_name;

### Common Table Expressions

    WITH temp_table AS (
         SELECT column1, column2
         FROM table_name
         WHERE condition
    )
    SELECT *
    FROM temp_table
    WHERE column2 > 100;

<br>

    SELECT column1 FROM table_name
    UNION ALL
    SELECT column1 FROM table_name2;

### Date Functions

    SELECT DATE(column1) 
    FROM table_name;

<br>

    SELECT strftime('%Y-%m', column1) 
    FROM table_name;

### String Functions

    SELECT UPPER(column1), LOWER(column1)
    FROM table_name;

<br>

    SELECT LENGTH(column1)
    FROM table_name;

<br>

    SELECT SUBSTR(column1, 1, 5)
    FROM table_name;

<br>
<br>

## Advanced SQL

### Window Functions (Analytics)

> Row number (unique ranking)

    SELECT column1,
           ROW_NUMBER() OVER (PARTITION BY column2 ORDER BY column1 DESC) AS rn
    FROM table_name;

> Rank (with gaps)

    SELECT column1,
           RANK() OVER (ORDER BY column1 DESC) AS rnk
    FROM table_name;

> Dense rank (no gaps)

    SELECT column1,
           DENSE_RANK() OVER (ORDER BY column1 DESC) AS drnk
    FROM table_name;

> Running total

    SELECT column1,
           SUM(column2) OVER (ORDER BY column1) AS running_total
    FROM table_name;

> Moving average (last 3 rows)

    SELECT column1,
           AVG(column2) OVER (
               ORDER BY column1
               ROWS BETWEEN 2 PRECEDING AND CURRENT ROW
           ) AS moving_avg
    FROM table_name;

### Common Table Expressions

> Basic CTE

    WITH cte_name AS (
        SELECT column1, column2
        FROM table_name
        WHERE condition
    )
    SELECT *
    FROM cte_name;

> Multiple CTEs

    WITH cte1 AS (
        SELECT column1 FROM table_name
    ),
    cte2 AS (
        SELECT column2 FROM table_name
    )
    SELECT *
    FROM cte1
    JOIN cte2 ON cte1.column1 = cte2.column2;

### Recursive Cte

    WITH RECURSIVE cte_name AS (
        SELECT column1, column2
        FROM table_name
        WHERE condition   -- base case

        UNION ALL

        SELECT t.column1, t.column2
        FROM table_name t
        JOIN cte_name c ON t.column1 = c.column2
    )
    SELECT *
    FROM cte_name;

### Subqueries (Advanced)

> Scalar subquery

    SELECT column1,
           (SELECT MAX(column2) FROM table_name) AS max_val
    FROM table_name;

> Correlated subquery

    SELECT column1
    FROM table_name t1
    WHERE column2 > (
        SELECT AVG(column2)
        FROM table_name t2
        WHERE t1.column1 = t2.column1
    );

> EXISTS

    SELECT column1
    FROM table_name t1
    WHERE EXISTS (
        SELECT 1
        FROM table_name t2
        WHERE t1.column1 = t2.column1
    );

### Advanced Joins

> Inner Join

    SELECT t1.column1, t2.column2
    FROM table_name t1
    JOIN table_name t2
    ON t1.column1 = t2.column2;

> Left Join

    SELECT *
    FROM table_name t1
    LEFT JOIN table_name t2
    ON t1.column1 = t2.column2;

> Self Join

    SELECT a.column1, b.column2
    FROM table_name a
    JOIN table_name b
    ON a.column1 = b.column2;

> Cross Join

    SELECT *
    FROM table_name t1
    CROSS JOIN table_name t2;

### Conditional Aggregations

    SELECT column1,
           SUM(CASE WHEN condition THEN column2 ELSE 0 END) AS conditional_sum,
           COUNT(CASE WHEN condition THEN 1 END) AS conditional_count
    FROM table_name
    GROUP BY column1;

### Pivoting (Manual)

    SELECT column1,
           SUM(CASE WHEN column2 = 'A' THEN column3 ELSE 0 END) AS A_total,
           SUM(CASE WHEN column2 = 'B' THEN column3 ELSE 0 END) AS B_total
    FROM table_name
    GROUP BY column1;

### De-Duplication

> Keep latest row per group

    WITH ranked AS (
        SELECT *,
               ROW_NUMBER() OVER (
                   PARTITION BY column1
                   ORDER BY column2 DESC
               ) AS rn
        FROM table_name
    )
    SELECT *
    FROM ranked
    WHERE rn = 1;

### Advanced Filtering

> BETWEEN

    SELECT *
    FROM table_name
    WHERE column1 BETWEEN value1 AND value2;

> IN

    SELECT *
    FROM table_name
    WHERE column1 IN (value1, value2);

> LIKE

    SELECT *
    FROM table_name
    WHERE column1 LIKE '%pattern%';

### Set Operations

> UNION (remove duplicates)

    SELECT column1 FROM table_name
    UNION
    SELECT column1 FROM table_name;

> UNION ALL (keep duplicates)

    SELECT column1 FROM table_name
    UNION ALL
    SELECT column1 FROM table_name;

> INTERSECT

    SELECT column1 FROM table_name
    INTERSECT
    SELECT column1 FROM table_name;

> EXCEPT

    SELECT column1 FROM table_name
    EXCEPT
    SELECT column1 FROM table_name;

### Performance Optimization

> Index

    CREATE INDEX idx_name
    ON table_name (column1);

> Explain query plan

    EXPLAIN QUERY PLAN
    SELECT *
    FROM table_name
    WHERE column1 = value;

### Advanced Date Handling

> Extract year

    SELECT strftime('%Y', column1) AS year
    FROM table_name;

> Date difference

    SELECT julianday('now') - julianday(column1) AS days_diff
    FROM table_name;

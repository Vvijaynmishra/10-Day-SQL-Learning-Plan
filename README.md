# 10-Day SQL Learning Plan **Mishra Tech Hub**

Welcome to the 10-Day SQL Learning Plan at **Mishra Tech Hub**! This guide is designed to take you from a beginner to an advanced SQL user in just ten days. Each day includes topics to learn, practice exercises with example code, and interview questions to help reinforce your understanding.

## Day 1: Introduction to SQL
- **Topics to Learn:**
  - What is SQL? Overview of databases.
  - Basic SQL syntax and structure.
  - Data types in SQL.
- **Practice:**
  - Install a SQL database (e.g., SQLite, MySQL).
  - Create a simple database and a table.
  - Example Code:
    ```sql
    CREATE TABLE students (
        id INT PRIMARY KEY,
        name VARCHAR(50),
        age INT
    );
    ```
- **Interview Questions:**
  - What is SQL and why is it important?
  - What are the common data types used in SQL?

---

## Day 2: Basic Queries
- **Topics to Learn:**
  - SELECT statement.
  - Using WHERE clause for filtering.
  - ORDER BY for sorting results.
- **Practice:**
  - Write queries to select data from your table.
  - Example Code:
    ```sql
    SELECT * FROM students WHERE age > 20 ORDER BY name;
    ```
- **Interview Questions:**
  - How do you retrieve all records from a table?
  - Explain the purpose of the ORDER BY clause.

---

## Day 3: Aggregate Functions
- **Topics to Learn:**
  - COUNT, SUM, AVG, MIN, MAX functions.
  - GROUP BY clause for grouping data.
  - HAVING clause for filtering groups.
- **Practice:**
  - Write aggregate queries on your data.
  - Example Code:
    ```sql
    SELECT age, COUNT(*) FROM students GROUP BY age HAVING COUNT(*) > 1;
    ```
- **Interview Questions:**
  - What is the difference between COUNT(*) and COUNT(column_name)?
  - When would you use the HAVING clause?

---

## Day 4: Joins
- **Topics to Learn:**
  - INNER JOIN, LEFT JOIN, RIGHT JOIN, FULL OUTER JOIN.
  - Understanding primary and foreign keys.
- **Practice:**
  - Create multiple tables and practice different joins.
  - Example Code:
    ```sql
    CREATE TABLE courses (
        course_id INT PRIMARY KEY,
        course_name VARCHAR(50)
    );

    SELECT students.name, courses.course_name
    FROM students
    INNER JOIN enrollments ON students.id = enrollments.student_id
    INNER JOIN courses ON enrollments.course_id = courses.course_id;
    ```
- **Interview Questions:**
  - What is the difference between INNER JOIN and LEFT JOIN?
  - Can you explain how to use a JOIN to combine data from two tables?

---

## Day 5: Subqueries and Nested Queries
- **Topics to Learn:**
  - Writing subqueries in SELECT, INSERT, UPDATE, DELETE.
  - Using EXISTS and IN.
- **Practice:**
  - Create subqueries for filtering data.
  - Example Code:
    ```sql
    SELECT name FROM students
    WHERE id IN (SELECT student_id FROM enrollments WHERE course_id = 1);
    ```
- **Interview Questions:**
  - What is a subquery, and when would you use it?
  - How do EXISTS and IN differ in SQL?

---

## Day 6: Data Manipulation
- **Topics to Learn:**
  - Inserting data with INSERT INTO.
  - Updating records with UPDATE.
  - Deleting records with DELETE.
- **Practice:**
  - Perform CRUD operations on your tables.
  - Example Code:
    ```sql
    INSERT INTO students (id, name, age) VALUES (1, 'Alice', 22);
    UPDATE students SET age = 23 WHERE id = 1;
    DELETE FROM students WHERE id = 1;
    ```
- **Interview Questions:**
  - How do you insert a new row into a table?
  - What happens if you run a DELETE statement without a WHERE clause?

---

## Day 7: Indexes and Performance
- **Topics to Learn:**
  - Understanding indexes and their purpose.
  - How to create and drop indexes.
- **Practice:**
  - Create indexes on your tables and test performance.
  - Example Code:
    ```sql
    CREATE INDEX idx_age ON students(age);
    ```
- **Interview Questions:**
  - What are indexes and why are they important?
  - How do indexes affect query performance?

---

## Day 8: Transactions and ACID Properties
- **Topics to Learn:**
  - Understanding transactions and their properties (ACID).
  - COMMIT and ROLLBACK statements.
- **Practice:**
  - Create a transaction that includes multiple operations.
  - Example Code:
    ```sql
    START TRANSACTION;
    UPDATE students SET age = 24 WHERE id = 1;
    COMMIT;
    ```
- **Interview Questions:**
  - What does ACID stand for?
  - Can you explain the importance of transactions in SQL?

---

## Day 9: Views and Stored Procedures
- **Topics to Learn:**
  - Creating and using views.
  - Introduction to stored procedures.
- **Practice:**
  - Create a view and a simple stored procedure.
  - Example Code:
    ```sql
    CREATE VIEW student_view AS SELECT name, age FROM students WHERE age >= 18;

    CREATE PROCEDURE GetStudents()
    BEGIN
      SELECT * FROM students;
    END;
    ```
- **Interview Questions:**
  - What is a view in SQL?
  - How do stored procedures differ from regular SQL queries?

---

## Day 10: Advanced SQL Concepts
- **Topics to Learn:**
  - Normalization and denormalization.
  - Advanced functions (e.g., window functions).
- **Practice:**
  - Review your previous work and practice complex queries.
  - Example Code:
    ```sql
    SELECT name, RANK() OVER (ORDER BY age) AS age_rank FROM students;
    ```
- **Interview Questions:**
  - What is normalization and why is it important?
  - Can you explain what window functions are in SQL?

---

## Final Tips
- Consistently practice writing SQL queries to reinforce your learning.
- Use online platforms (e.g., LeetCode, HackerRank, SQLZoo) for additional exercises.
- Review all concepts regularly and try to solve real-world problems.

Happy learning at **Mishra Tech Hub**!

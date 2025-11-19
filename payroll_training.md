# PayrollDB SQL Training Documentation

## Session 1 -- Introduction to Relational Databases

-   Explain data persistence and why flat files fail at scale.
-   Define: table, record, column, primary key, foreign key.
-   Show spreadsheet → SQL migration.
-   Install MySQL and connect using Workbench.
-   Create database using `CREATE DATABASE`.

### Lab

-   Create **PayrollDB**
-   Create **Employees(id, name, department, salary)**
-   Insert 3 rows and run `SELECT *`.

------------------------------------------------------------------------

## Session 2 -- Data Definition Language (DDL)

-   Commands: `CREATE`, `ALTER`, `DROP`
-   Data types: INT, VARCHAR, DATE, DECIMAL, BOOLEAN
-   Constraints: PRIMARY KEY, UNIQUE, NOT NULL, DEFAULT

### Lab

-   Add `joining_date`, `email UNIQUE` to Employees.
-   Create **Departments(id, name)**.
-   Add foreign key Employees.department → Departments.id.
-   Demonstrate referential integrity.

------------------------------------------------------------------------

## Session 3 -- Data Manipulation Language (DML)

-   INSERT, UPDATE, DELETE
-   WHERE filtering
-   Atomicity and rollback

### Lab

-   Insert 10 employees
-   Update salary
-   Delete a test row
-   Department transfer by updating FK
-   Demonstrate commit/rollback

------------------------------------------------------------------------

## Session 4 -- Data Query Language (DQL)

-   SELECT syntax
-   WHERE, ORDER BY, LIMIT
-   AND, OR, BETWEEN, IN
-   Aggregations: COUNT, SUM, AVG, MIN, MAX
-   GROUP BY, HAVING

### Lab

-   List employees by department
-   Salary totals per department
-   Departments with avg salary \> 60,000

------------------------------------------------------------------------

## Session 5 -- Joins and Relationships

-   Relationship types: 1--1, 1--many, many--many
-   INNER, LEFT, RIGHT, CROSS joins
-   Natural vs explicit joins

### Lab

-   Join Employees & Departments
-   Create **Projects** and **EmployeeProjects**
-   Query multi‑project employees

------------------------------------------------------------------------

## Session 6 -- Subqueries, Views, Indexing

-   Subqueries in WHERE & FROM
-   CREATE VIEW basics
-   Indexing for performance
-   Use EXPLAIN for query plans

### Lab

-   View: **HighEarners**
-   Add index on salary
-   Compare execution plans

------------------------------------------------------------------------

## Session 7 -- Transactions & ACID

-   START TRANSACTION, COMMIT, ROLLBACK
-   Isolation levels
-   Demonstrate concurrent updates

### Lab

-   Simulate fund transfer with transaction block

------------------------------------------------------------------------

## Session 8 -- JDBC Integration Overview

-   JDBC driver, connection string
-   Steps: load → connect → prepare → execute → close
-   SQL exceptions in Java

### Lab

-   Java program reads employees from PayrollDB

------------------------------------------------------------------------

## Session 9 -- Query Optimisation

-   Full table scans vs indexed searches
-   SELECT \* is discouraged
-   Denormalisation trade‑offs

### Lab

-   Optimise a slow query using indexes / rewrites

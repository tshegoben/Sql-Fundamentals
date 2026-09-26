# Sql-Fundamentals
Demontration of SQl Fundamentals
# SQL Fundamentals – Exercise 1

## Overview

This repository contains my first hands-on SQL exercise from the **BrightLearn Data Analytics** course.

The exercise focuses on the fundamentals of retrieving and filtering data from a database table using SQL. It uses a small `employees` table and requires writing queries to retrieve specific information and predict the expected output.

## Exercise Focus

The main SQL concepts covered in this exercise are:

* `SELECT`
* `SELECT *`
* `DISTINCT`
* `WHERE`
* `ORDER BY`
* `LIMIT`
* `AND`
* `OR`
* `NOT`
* `IN`

## Dataset

The exercise uses an `employees` table containing the following information:

* Employee ID
* First name
* Last name
* Department
* Salary
* Hire date
* City

The dataset contains five employees across the IT, HR, Finance and Marketing departments.

## Questions Covered

The exercise contains 10 SQL queries:

1. Retrieve all columns from the `employees` table.
2. Find all unique departments.
3. Retrieve employee first and last names ordered by salary from highest to lowest.
4. Retrieve the three highest-paid employees.
5. Find employees in the IT department.
6. Find employees in Finance with a salary greater than 60,000.
7. Find employees in HR or Marketing.
8. Find employees who are not in IT.
9. Find employees in IT, HR or Finance using `IN`.
10. Find employees in IT with a salary greater than 65,000 and who are based in Johannesburg.

## What I Practised

### Selecting Data

Using `SELECT` to retrieve either all columns or only the columns required for a question.

```sql
SELECT *
FROM employees;
```

### Removing Duplicates

Using `DISTINCT` to return unique values from a column.

```sql
SELECT DISTINCT department
FROM employees;
```

### Sorting Data

Using `ORDER BY` to arrange results, including descending order with `DESC`.

```sql
SELECT first_name, last_name
FROM employees
ORDER BY salary DESC;
```

### Limiting Results

Using `LIMIT` to restrict the number of rows returned.

```sql
SELECT id, first_name, last_name, salary
FROM employees
ORDER BY salary DESC
LIMIT 3;
```

### Filtering Data

Using `WHERE` to return only rows that meet a specific condition.

```sql
SELECT *
FROM employees
WHERE department = 'IT';
```

### Combining Conditions

Using `AND` when multiple conditions must be true, and `OR` when either condition can be true.

```sql
WHERE department = 'IT'
AND salary > 65000;
```

```sql
WHERE department = 'HR'
OR department = 'Marketing';
```

### Excluding Data

Using `NOT` to exclude records that match a condition.

```sql
WHERE NOT department = 'IT';
```

### Using IN

Using `IN` when checking whether a value belongs to a list of possible values.

```sql
WHERE department IN ('IT', 'HR', 'Finance');
```

## Learning Outcome

This exercise helped me practise the basic structure of SQL queries and understand how different clauses work together to retrieve specific information from a table.

One of the main things I am learning is that SQL is not just about writing a query. I also need to understand what the query is asking for and be able to predict the expected result before running it.

## Exercise Format

The original exercise is designed as a handwritten, pen-and-paper activity. Each question requires:

1. Writing the SQL query.
2. Drawing the expected output table.
3. Checking that the output contains the exact columns requested.

## Course

**BrightLearn – Data Analytics**
**Exercise 01 – SQL Fundamentals**
**Topic:** SELECT & Filtering

## Status

**Completed – SQL Fundamentals Exercise 1**

## Repository Purpose

This repository documents my progress while learning SQL as part of my Data Analytics journey. It represents an early practical exercise focused on the fundamentals before moving into more complex SQL queries and data analysis.

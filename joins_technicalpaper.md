# SQL Joins

## Introduction

SQL joins are used to combine data from two or more tables.

Joins help retrieve related information from databases.

They are commonly used in:

- Banking systems
- Shopping websites
- Hospital systems
- School management systems

---

# What is a Join?

A join is an SQL operation that combines rows from multiple tables.

Tables are connected using common columns.

Usually joins use:

- Primary keys
- Foreign keys

---

# Types of SQL Joins

Main types of joins are:

1. Inner Join
2. Left Join
3. Right Join
4. Full Join
5. Cross Join
6. Self Join

---

# Inner Join

An inner join returns only matching rows from both tables.

## SQL Syntax

```sql
SELECT employees.name, departments.department_name
FROM employees
INNER JOIN departments
ON employees.department_id = departments.department_id;
```

---

# Left Join

A left join returns all records from the left table.

Matching records from the right table are also returned.

If no match exists, NULL values are shown.

## SQL Syntax

```sql
SELECT employees.name, departments.department_name
FROM employees
LEFT JOIN departments
ON employees.department_id = departments.department_id;
```

---

# Right Join

A right join returns all records from the right table.

Matching records from the left table are displayed.

## SQL Syntax

```sql
SELECT employees.name, departments.department_name
FROM employees
RIGHT JOIN departments
ON employees.department_id = departments.department_id;
```

---

# Full Join

A full join returns all matching and non-matching records from both tables.

## SQL Syntax

```sql
SELECT employees.name, departments.department_name
FROM employees
FULL OUTER JOIN departments
ON employees.department_id = departments.department_id;
```

---

# Cross Join

A cross join combines every row from one table with every row from another table.

## SQL Syntax

```sql
SELECT employees.name, departments.department_name
FROM employees
CROSS JOIN departments;
```

---

# Self Join

A self join joins a table with itself.

It is useful when related data exists in the same table.

## SQL Syntax

```sql
SELECT A.name AS Employee,
B.name AS Manager
FROM employees A, employees B
WHERE A.manager_id = B.employee_id;
```

---

# Primary Key and Foreign Key

## Primary Key

A primary key uniquely identifies each row in a table.

Example:

- Employee_ID

## Foreign Key

A foreign key connects one table with another table.

Example:

- Department_ID

---

# Importance of Joins

Joins help:

- Retrieve related data
- Reduce duplicate data
- Improve database design
- Save storage space

---

# Real-World Applications

Joins are used in:

- Banking systems
- Online shopping websites
- Hospital databases
- Airline reservation systems

---

# Advantages of SQL Joins

- Easy data retrieval
- Better database management
- Improves data organization

---

# Conclusion

SQL joins are important in relational databases.

They help combine related data from multiple tables.

Types of joins such as inner join, left join, right join, full join, cross join, and self join are widely used in modern applications.

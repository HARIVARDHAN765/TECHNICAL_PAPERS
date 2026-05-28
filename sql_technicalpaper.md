# Technical Paper on SQL Concepts

# 1. ACID Properties

ACID properties help maintain reliable and accurate database transactions.

ACID stands for:

- Atomicity
- Consistency
- Isolation
- Durability

## Atomicity

Atomicity means a transaction is completed fully or not completed at all.

## Consistency

Consistency ensures the database remains valid before and after a transaction.

## Isolation

Isolation ensures multiple transactions do not interfere with each other.

## Durability

Durability ensures saved data remains permanent even after system crashes.

# 2. CAP Theorem

CAP theorem explains the limitations of distributed databases.

CAP stands for:

- Consistency
- Availability
- Partition Tolerance

## Consistency

Every user sees the same updated data.

---

## Availability

The system always responds to requests.

---

## Partition Tolerance

The system continues working even if network communication fails.


# 3. Joins

Joins are used to combine data from multiple tables.

Suppose we have:

### Students Table

| id | name |
|---|---|
| 1 | Hari |
| 2 | Ram |

### Marks Table

| student_id | marks |
|---|---|
| 1 | 90 |
| 2 | 80 |

---

## INNER JOIN

Returns matching rows from both tables.

```sql
SELECT students.name, marks.marks
FROM students
INNER JOIN marks
ON students.id = marks.student_id;
```

---

## LEFT JOIN

Returns all rows from the left table and matching rows from the right table.

---

## RIGHT JOIN

Returns all rows from the right table and matching rows from the left table.

---

## FULL JOIN

Returns all rows from both tables.

---

# 4. Aggregations and Filters

Aggregation functions perform calculations on data.

Common aggregation functions:

- COUNT()
- SUM()
- AVG()
- MAX()
- MIN()

## Filters

Filters are used with the `WHERE` clause.

## GROUP BY

Groups rows with similar values.

# 5. Normalization

Normalization organizes data to reduce redundancy and improve efficiency.

---

## First Normal Form (1NF)

- Removes repeating groups
- Each column contains single values

---

## Second Normal Form (2NF)

- Must already be in 1NF
- Removes partial dependency

---

## Third Normal Form (3NF)

- Must already be in 2NF
- Removes transitive dependency

---

# 6. Indexes

Indexes improve query performance.

Without indexes:
- Database scans the full table.

With indexes:
- Database finds data faster.

## Advantages

- Faster searching
- Faster sorting
- Better query performance

# 7. Transactions

A transaction is a group of SQL operations executed together.

Example:

```sql
BEGIN;

UPDATE accounts
SET balance = balance - 1000
WHERE id = 1;

UPDATE accounts
SET balance = balance + 1000
WHERE id = 2;

COMMIT;
```

---

## Transaction Commands

- BEGIN
- COMMIT
- ROLLBACK

---

# 8. Locking Mechanism

Locking prevents conflicts when multiple users access the same data.

---

## Shared Lock

- Multiple users can read data
- Cannot modify data

---

## Exclusive Lock

- Only one user can modify data
- Other users must wait

---

# 9. Database Isolation Levels

Isolation levels control how transactions interact with each other.

---

## Read Uncommitted

- Lowest isolation
- Allows dirty reads

---

## Read Committed

- Only committed data can be read

---

## Repeatable Read

- Prevents changes during a transaction

---

## Serializable

- Highest isolation level
- Prevents all conflicts
- Slower performance

---

# 10. Triggers

Triggers are automatic actions executed when database events occur.

Events:
- INSERT
- UPDATE
- DELETE

Example:

```sql
CREATE TRIGGER log_update
AFTER UPDATE
ON employees
FOR EACH ROW
INSERT INTO logs(message)
VALUES('Employee data updated');
```

---

## Uses of Triggers

- Logging changes
- Data validation
- Automatic updates

---

# 11. Views

Views are virtual tables created from SQL queries.

Example:

```sql
CREATE VIEW employee_view AS
SELECT name, salary
FROM employees;
```

# 12. Primary Key and Foreign Key

## Primary Key

A primary key uniquely identifies each row.

## Foreign Key

A foreign key connects two tables.

# References

1. MySQL Documentation  
2. PostgreSQL Documentation  
3. Oracle SQL Documentation  
4. W3Schools SQL Tutorial  
5. GeeksforGeeks Database Articles  
6. MDN Web Docs  
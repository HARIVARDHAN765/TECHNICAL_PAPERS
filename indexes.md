# Database Indexes

# Introduction

Database indexes are used to improve the speed of data retrieval.

Indexes help databases find data quickly without scanning the entire table.

Indexes are important in large database systems.

They are commonly used in:

- Banking systems
- Shopping websites
- Hospital systems
- Airline reservation systems
- Social media applications

Without indexes, searching data becomes slow.

---

# What is an Index?

An index is a special database structure that helps locate data quickly.

It works like an index in a book.

Instead of checking every page, the index helps directly find information.

In databases, indexes help quickly locate rows in a table.

---

# Why Indexes are Important

Suppose a table contains millions of employee records.

If a user searches for one employee:

Without an index:

- Database scans every row
- Search becomes slow

With an index:

- Database finds the row quickly
- Performance improves

Indexes reduce search time significantly.

---

# How Indexes Work

Indexes store:

- Indexed column values
- Pointers to table rows

When a query runs:

1. Database checks the index
2. Finds matching value
3. Retrieves required row

This reduces unnecessary scanning.

---

# Features of Indexes

Indexes provide:

- Faster searching
- Faster sorting
- Better query performance
- Efficient data retrieval

---

# Types of Indexes

Main types of indexes are:

1. Primary Index
2. Secondary Index
3. Clustered Index
4. Non-Clustered Index
5. Unique Index
6. Composite Index

---

# Primary Index

A primary index is automatically created on the primary key.

It uniquely identifies rows in a table.

## Example

Employee table:

| Employee_ID | Name |
|-------------|------|
| 1 | Ravi |
| 2 | Sita |

Employee_ID can have a primary index.

---

# Advantages of Primary Index

- Fast searching
- Prevents duplicate values
- Improves data access

---

# Secondary Index

A secondary index is created on non-primary key columns.

It helps search data using other columns.

## Example

An index on employee name.

---

# Advantages of Secondary Index

- Faster searching on non-primary columns
- Improves query performance

---

# Clustered Index

A clustered index stores table data in sorted order.

A table can have only one clustered index.

## Example

Rows stored based on Employee_ID order.

---

# Advantages of Clustered Index

- Faster range searches
- Better sorting performance

---

# Non-Clustered Index

A non-clustered index stores indexes separately from table data.

It contains pointers to actual rows.

A table can have multiple non-clustered indexes.

---

# Advantages of Non-Clustered Index

- Multiple indexes allowed
- Faster searching

---

# Unique Index

A unique index prevents duplicate values in a column.

## Example

Email column in a user table.

Two users cannot have the same email.

---

# Composite Index

A composite index uses multiple columns together.

## Example

Index on:

- First_Name
- Last_Name

---

# Importance of Indexes

Indexes help:

- Improve database performance
- Reduce query execution time
- Speed up data retrieval
- Improve sorting and filtering

---

# SQL Syntax for Creating Index

```sql
CREATE INDEX index_name
ON employees(name);
```

---

# SQL Syntax for Unique Index

```sql
CREATE UNIQUE INDEX index_name
ON employees(email);
```

---

# SQL Syntax for Dropping Index

```sql
DROP INDEX index_name;
```

---

# Real-World Applications

Indexes are used in:

- Banking systems
- ATM applications
- E-commerce websites
- Hospital databases
- Railway reservation systems

---

# Banking Example

Suppose a bank stores millions of customer records.

Indexes help quickly find:

- Account numbers
- Customer names
- Transaction details

This improves system performance.

---

# Online Shopping Example

E-commerce websites use indexes for:

- Product searches
- Customer information
- Order tracking

Indexes help websites respond quickly.

---

# Advantages of Indexes

- Faster searching
- Better query performance
- Faster sorting
- Efficient data access
- Improved database efficiency

---

# Limitations of Indexes

- Uses extra storage space
- Insert and update operations may become slower
- Too many indexes may reduce performance

---

# Best Practices for Using Indexes

- Create indexes on frequently searched columns
- Avoid unnecessary indexes
- Use unique indexes when needed
- Monitor query performance regularly

---

# Difference Between Clustered and Non-Clustered Index

## Clustered Index

- Stores data in sorted order
- Only one clustered index allowed

## Non-Clustered Index

- Stores indexes separately
- Multiple indexes allowed

---

# Common Problems with Indexes

Some common problems are:

- Too many indexes
- Unused indexes
- Increased storage usage
- Slow updates

---

# How to Improve Index Performance

Performance can be improved by:

- Using proper indexes
- Removing unused indexes
- Using composite indexes carefully
- Monitoring database queries

---

# Future of Database Indexes

Modern databases use advanced indexing techniques.

Examples include:

- In-memory indexes
- Bitmap indexes
- Hash indexes

These methods improve database performance further.

---

# Conclusion

Database indexes are important for improving database performance.

Indexes help retrieve data quickly and efficiently.

Types of indexes such as primary index, secondary index, clustered index, non-clustered index, unique index, and composite index are widely used in modern applications.

Indexes improve searching, sorting, and query execution in database systems.

---

# References

1. MySQL Documentation
2. PostgreSQL Documentation
3. Oracle Database Documentation
4. SQL Server Documentation
5. W3Schools SQL Tutorial
6. GeeksforGeeks Database Articles
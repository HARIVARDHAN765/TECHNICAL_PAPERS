# Locking Mechanism in Databases

## Introduction

A locking mechanism is used in databases to control access to data.

It helps prevent problems when many users access the same data at the same time.

Locking is important in multi-user applications.

Examples:

- Banking systems
- Shopping websites
- Hospital systems
- Railway reservation systems

Without locking, data may become incorrect.

---

# What is a Lock?

A lock is a restriction placed on data.

Locks help:

- Protect data
- Prevent conflicts
- Maintain consistency

When data is locked:

- Some users can read data
- Some users must wait
- Some users cannot modify data

---

# Importance of Locking

Suppose two users access the same bank account.

User A withdraws money.

User B also withdraws money.

Without locking:

- Balance may become incorrect

With locking:

- One transaction completes first
- Second transaction waits
- Correct balance is maintained

---

# Goals of Locking

Locking helps to:

- Maintain consistency
- Prevent data corruption
- Protect transactions
- Improve reliability

---

# Types of Locks

Main types of locks:

1. Shared Lock
2. Exclusive Lock

---

# Shared Lock

A shared lock allows users to read data.

Many users can read the same data together.

But users cannot modify the data.

## Features

- Multiple users allowed
- Only reading allowed
- Writing blocked

## Advantages

- Good reading performance
- Useful for reports

## Disadvantages

- Writing operations must wait

---

# Exclusive Lock

An exclusive lock allows only one transaction to modify data.

Other users must wait.

## Features

- Only one user allowed
- Writing allowed
- Prevents conflicts

## Advantages

- Maintains data integrity
- Prevents incorrect updates

## Disadvantages

- Other users must wait

---

# Lock Granularity

Lock granularity means the amount of data locked.

Types:

- Row-level locking
- Table-level locking
- Database-level locking

---

# Row-Level Locking

Only one row is locked.

Other rows remain available.

## Advantages

- Better concurrency
- Better performance

## Disadvantages

- More memory usage

---

# Table-Level Locking

The whole table becomes locked.

Other users cannot modify the table.

## Advantages

- Easy management

## Disadvantages

- Lower concurrency
- More waiting time

---

# Concurrency Control

Concurrency control means managing multiple transactions safely.

Locking is part of concurrency control.

---

# What is a Transaction?

A transaction is a group of database operations.

Example:

- Deduct money from one account
- Add money to another account

Both operations form one transaction.

---

# Deadlock

A deadlock happens when two transactions wait for each other.

Neither transaction can continue.

## Causes

- Incorrect lock order
- Long transactions

## Prevention Methods

- Timeout
- Rollback
- Deadlock detection

---

# Two-Phase Locking

Two-phase locking has two phases.

## Growing Phase

- Transaction acquires locks

## Shrinking Phase

- Locks are released

---

# Lock Manager

A lock manager controls all locks in the database.

Responsibilities:

- Granting locks
- Releasing locks
- Detecting deadlocks

---

# Advantages of Locking

- Maintains consistency
- Prevents conflicts
- Improves reliability
- Protects transactions

---

# Disadvantages of Locking

- May reduce speed
- Users may wait
- Deadlocks may occur

---

# Conclusion

Locking mechanisms are very important in databases.

They help maintain:

- Data consistency
- Transaction safety
- Reliable operations

Modern applications depend heavily on locking mechanisms.
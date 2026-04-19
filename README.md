# SQL-COH
SQL-COH is a comprehensive collection of SQL queries, commands, and best practices used to perform various database operations efficiently.

## TABLE OF CONTENTS

- [Database Schema](#1-database-schema)
- [Normalization](#2-normalization)
- [Denormalization](#3-denormalization)
- [ACID Properties](#4-acid-properties)
- [Indexing](#5-indexing)
- [Transactions](#6-transactions)
- [Views](#7-views)
- [Stored Procedures](#8-stored-procedures)
- [Triggers](#9-triggers)
- [Functions](#10-functions)
- [Joins](#11-joins)
- [Subqueries](#12-subqueries)
- [Aggregate Functions](#13-aggregate-functions)
- [String Functions](#14-string-functions)
- [Date Functions](#15-date-functions)
- [Mathematical Functions](#16-mathematical-functions)
- [Logical Functions](#17-logical-functions)
- [User Management](#18-user-management)
- [Backup and Restore](#19-backup-and-restore)
- [Performance Tuning](#20-performance-tuning)
- [Security](#21-security)
- [Best Practices](#22-best-practices)
- [Resources](#23-resources)

---
# Database Systems Overview

A **database** is an organized collection of structured information, or data, typically stored electronically. To manage this data effectively, we use a **Database Management System (DBMS)**.

---

## 1. Relational Databases (RDBMS)
The most common type, RDBMS uses a rigid, predefined schema. Data is organized into **tables** with rows (records) and columns (attributes).

* **Key Feature:** Uses **SQL** (Structured Query Language) and maintains **ACID** compliance (Atomicity, Consistency, Isolation, Durability).
* **Examples:** MySQL, PostgreSQL, Oracle Database, Microsoft SQL Server.

## 2. Non-Relational (NoSQL) Databases
NoSQL databases are designed for distributed data stores with high scalability needs. They are flexible, allowing for unstructured or semi-structured data.

* **Document Stores:** Store data in JSON-like documents (e.g., **MongoDB**).
* **Key-Value Stores:** Store data as a collection of key-value pairs (e.g., **Redis**).
* **Wide-Column Stores:** Optimized for large datasets and high availability (e.g., **Cassandra**).

## 3. Specialized Architecture Types

### **Graph Databases**
Uses **nodes** (entities) and **edges** (relationships). Perfect for social networks or recommendation engines where the connection between data points is the priority.
* **Examples:** Neo4j, Amazon Neptune, ArangoDB.

### **Time-Series Databases**
Optimized for time-stamped data, providing efficient storage and retrieval for sequences of events.
* **Examples:** InfluxDB, TimescaleDB, OpenTSDB.

### **Object-Oriented Databases**
Data is represented in the form of **objects**, as used in object-oriented programming. This bridges the gap between application code and data storage.
* **Examples:** ObjectDB, db4o, Versant.

### **Columnar Databases**
Unlike traditional row-based storage, these store data in columns. This significantly improves performance for analytical workloads and data warehousing.
* **Examples:** Amazon Redshift, Google BigQuery, Apache Druid.

---

## 4. Performance & Deployment Models

### **In-Memory Databases**
Stores data in the main memory (RAM) rather than on disk to allow for near-instant data access.
* **Use Case:** Real-time applications, caching, and financial trading.
* **Examples:** Redis, Memcached, SAP HANA.

### **NewSQL Databases**
A modern class of RDBMS that seeks to provide the scalability of NoSQL systems while maintaining the ACID guarantees of traditional SQL.
* **Examples:** CockroachDB, VoltDB, NuoDB.

### **Distributed & Cloud Databases**
* **Distributed:** Spread across multiple physical locations or servers to ensure high availability and fault tolerance (e.g., **Amazon DynamoDB**).
* **Cloud:** Hosted and managed on cloud platforms, offering "Database as a Service" (DBaaS) (e.g., **Amazon RDS**, **Google Cloud SQL**).

---

## Summary Comparison

| Category | Primary Usage | Data Structure |
| :--- | :--- | :--- |
| **RDBMS** | Business Logic / Transactions | Structured (Tables) |
| **NoSQL** | Big Data / Real-time Web | Unstructured (JSON/Key-Value) |
| **Graph** | Social Networks / Fraud Detection | Nodes & Edges |
| **Columnar** | Analytics / BI Reporting | Columns |
| **In-Memory** | Caching / High-speed Apps | RAM-based |

---
## Database Management Systems (DBMS) :
A **Database Management System (DBMS)** is software that interacts with end-users, applications, and the database itself to capture and analyze data. It provides an interface for users to create, read, update, and delete data in a database.
### Key Functions of a DBMS:
1. **Data Storage Management**: Efficiently stores and retrieves data.
2. **Data Manipulation**: Allows users to manipulate data using SQL or other query languages.
3. **Data Security**: Implements access controls to protect data from unauthorized access.  
4. **Data Integrity**: Ensures data accuracy and consistency through constraints and rules.
5. **Backup and Recovery**: Provides mechanisms for data backup and recovery in case of failures
6. **Concurrency Control**: Manages simultaneous data access by multiple users to prevent conflicts.
7. **Performance Optimization**: Uses indexing and query optimization techniques to enhance performance.
### Popular DBMS Examples:
| DBMS | Type | Use Case |
| :--- | :--- | :--- |
| MySQL | RDBMS | Web applications, small to medium-sized databases |
| PostgreSQL | RDBMS | Complex queries, large databases, and data integrity |
| MongoDB | NoSQL (Document Store) | Flexible schema, big data, real-time applications |
| Redis | NoSQL (Key-Value Store) | Caching, real-time analytics, session management |
| Neo4j | Graph Database | Social networks, recommendation engines |
| Amazon DynamoDB | NoSQL (Distributed) | High scalability, serverless applications |
| Amazon RDS | Cloud DBMS | Managed relational database service |
| Google Cloud SQL | Cloud DBMS | Managed relational database service |

---

## Database Concepts
### 1. Database Schema
A **database schema** is the structure that defines the organization of data in a database. It includes definitions of tables, columns, data types, relationships, and constraints. A well-designed schema ensures data integrity and efficient querying.
### 2. Normalization
**Normalization** is the process of organizing data in a database to reduce redundancy and improve data integrity. It involves dividing large tables into smaller, related tables and defining relationships between them. The normal forms (1NF, 2NF, 3NF, etc.) provide guidelines for achieving different levels of normalization.
### 3. Denormalization
**Denormalization** is the process of intentionally introducing redundancy into a database schema to improve read performance. It is often used in data warehousing and analytical databases where read operations are more frequent than write operations.
### 4. ACID Properties
The **ACID** properties ensure reliable transactions in a database:
- **Atomicity**: Ensures that all operations within a transaction are completed successfully or none are.
- **Consistency**: Ensures that a transaction brings the database from one valid state to another.
- **Isolation**: Ensures that concurrent transactions do not interfere with each other.
- **Durability**: Ensures that once a transaction is committed, it will remain so, even in the event of a system failure.
### 5. Indexing
**Indexing** is a technique used to improve the speed of data retrieval operations on a database table. An index is a data structure that allows for fast access to rows in a table based on the values of one or more columns. Common types of indexes include B-tree, hash, and bitmap indexes.
### 6. Transactions
A **transaction** is a sequence of one or more SQL operations that are executed as a single unit of work. Transactions ensure data integrity and consistency by adhering to the ACID properties. They can be committed (saved) or rolled back (undone) based on the success or failure of the operations within the transaction.
### 7. Views
A **view** is a virtual table that is based on the result set of a SQL query. It does not store data itself but provides a way to simplify complex queries, enhance security by restricting access to specific data, and present data in a specific format. Views can be used to encapsulate business logic and provide a consistent interface for querying data.
### 8. Stored Procedures
A **stored procedure** is a precompiled collection of SQL statements and optional control-of-flow statements that are stored under a name and processed as a unit. Stored procedures can accept parameters, perform complex operations, and return results. They are used to encapsulate business logic, improve performance, and enhance security by controlling access to data.
### 9. Triggers
A **trigger** is a special type of stored procedure that automatically executes in response to certain events on a particular table or view. Triggers can be set to execute before or after an insert, update, or delete operation. They are commonly used for enforcing business rules, maintaining audit trails, and synchronizing data across tables.
### 10. Functions
A **function** is a reusable block of code that performs a specific task and returns a value. In SQL, functions can be built-in (e.g., `SUM()`, `AVG()`) or user-defined. User-defined functions allow developers to create custom operations that can be used in SQL queries, similar to stored procedures but with the ability to return values directly.
### 11. Joins
A **join** is a SQL operation that combines rows from two or more tables based on a related column between them. Joins allow you to retrieve data from multiple tables in a single query. Common types of joins include:
- **INNER JOIN**: Returns only the rows that have matching values in both tables.
- **LEFT JOIN**: Returns all rows from the left table and the matched rows from the right table. If there is no match, NULL values are returned for columns from the right table.
- **RIGHT JOIN**: Returns all rows from the right table and the matched rows from the left table. If there is no match, NULL values are returned for columns from the left table.
- **FULL OUTER JOIN**: Returns all rows when there is a match in either left or right table. If there is no match, NULL values are returned for columns from the table without a match.
### 12. Subqueries
A **subquery** is a query nested inside another query. Subqueries can be used in various clauses of a SQL statement, such as `SELECT`, `WHERE`, and `FROM`. They allow you to perform operations that require multiple steps, such as filtering results based on aggregated values or retrieving data from related tables.
### 13. Aggregate Functions
**Aggregate functions** perform calculations on a set of values and return a single value. Common aggregate functions include:
- `SUM()`: Returns the total sum of a numeric column.
- `AVG()`: Returns the average value of a numeric column.
- `COUNT()`: Returns the number of rows that match a specified condition.
- `MAX()`: Returns the maximum value in a set of values.
- `MIN()`: Returns the minimum value in a set of values.
### 14. String Functions
**String functions** are used to manipulate and analyze string data in SQL. Common string functions include:
- `CONCAT()`: Concatenates two or more strings into one.
- `SUBSTRING()`: Extracts a portion of a string based on specified starting position and length.
- `LENGTH()`: Returns the length of a string.
- `UPPER()`: Converts a string to uppercase.
- `LOWER()`: Converts a string to lowercase.
### 15. Date Functions
**Date functions** are used to manipulate and analyze date and time data in SQL. Common date functions include:
- `NOW()`: Returns the current date and time.
- `DATEADD()`: Adds a specified time interval to a date.
- `DATEDIFF()`: Returns the difference between two dates.
- `YEAR()`: Extracts the year from a date.
- `MONTH()`: Extracts the month from a date.
- `DAY()`: Extracts the day from a date.
### 16. Mathematical Functions
**Mathematical functions** perform mathematical operations on numeric data in SQL. Common mathematical functions include:
- `ABS()`: Returns the absolute value of a number.
- `ROUND()`: Rounds a number to a specified number of decimal places.
- `CEILING()`: Returns the smallest integer greater than or equal to a number.
- `FLOOR()`: Returns the largest integer less than or equal to a number.
- `POWER()`: Returns the value of a number raised to the power of another number.
### 17. Logical Functions
**Logical functions** are used to perform logical operations in SQL. Common logical functions include:
- `AND`: Returns true if both conditions are true.
- `OR`: Returns true if at least one condition is true.
- `NOT`: Returns true if the condition is false.
- `CASE`: Evaluates a list of conditions and returns one of multiple possible result expressions.
### 18. User Management
**User management** in a database involves creating and managing user accounts, assigning permissions, and ensuring security. Common SQL commands for user management
include:
- `CREATE USER
`: Creates a new user account.
- `GRANT`: Assigns specific permissions to a user or role.
- `REVOKE`: Removes specific permissions from a user or role.
- `ALTER USER`: Modifies an existing user account.
- `DROP USER`: Deletes a user account from the database.
### 19. Backup and Restore
**Backup and restore** are critical processes for ensuring data safety and recovery in case of data loss or corruption. Common SQL commands for backup and restore include:
- `BACKUP DATABASE`: Creates a backup of the database.
- `RESTORE DATABASE`: Restores a database from a backup.
- `BACKUP LOG`: Creates a backup of the transaction log.
- `RESTORE LOG`: Restores a transaction log backup.
### 20. Performance Tuning
**Performance tuning** involves optimizing SQL queries and database configurations to improve the speed and efficiency of data retrieval and manipulation. Common techniques for performance tuning include:
- **Indexing**: Creating indexes on columns that are frequently used in WHERE clauses or JOIN conditions.
- **Query Optimization**: Analyzing and rewriting SQL queries to reduce execution time.
- **Partitioning**: Dividing large tables into smaller, more manageable pieces to improve query performance.
- **Caching**: Storing frequently accessed data in memory to reduce database load.
### 21. Security
**Database security** involves protecting the database from unauthorized access, breaches, and other security threats.
Common practices for database security include:
- **Access Control**: Implementing role-based access control (RBAC) to restrict user permissions based on their roles.
- **Encryption**: Encrypting sensitive data both at rest and in transit to prevent unauthorized access.
- **Auditing**: Keeping logs of database activities to monitor for suspicious behavior and ensure compliance.
- **Regular Updates**: Applying security patches and updates to the database software to protect against vulnerabilities.
### 22. Best Practices
- **Use appropriate data types**: Choose the most efficient data types for your columns to minimize storage and improve performance.
- **Avoid SELECT ***: Specify only the columns you need in your SELECT statements to reduce data transfer and processing overhead.
- **Use WHERE clauses effectively**: Ensure that your WHERE clauses are optimized to take advantage of indexes and reduce the number of rows scanned.
- **Limit the use of subqueries**: Subqueries can be resource-intensive; consider using JOINs or temporary tables as alternatives when possible.
- **Monitor and maintain indexes**: Regularly review and maintain your indexes to ensure they are providing optimal performance.
- **Regularly backup your database**: Implement a robust backup strategy to protect against data loss and ensure quick recovery in case of failures.
- **Use transactions for critical operations**: Ensure data integrity by using transactions for operations that involve multiple steps or affect multiple tables.
- **Implement security best practices**: Regularly review and update your database security measures to protect against evolving threats and vulnerabilities.   
### 23. Resources
- [SQL Tutorial](https://www.w3schools.com/sql/)
- [PostgreSQL Documentation](https://www.postgresql.org/docs/)
- [MySQL Documentation](https://dev.mysql.com/doc/)
- [MongoDB Documentation](https://docs.mongodb.com/)
- [Redis Documentation](https://redis.io/documentation)
- [Neo4j Documentation](https://neo4j.com/docs/)
- [Amazon DynamoDB Documentation](https://docs.aws.amazon.com/dynamodb/)
- [Amazon RDS Documentation](https://docs.aws.amazon.com/rds/)
- [Google Cloud SQL Documentation](https://cloud.google.com/sql/docs)
- [Database Normalization](https://www.essentialsql.com/get-ready-to-learn-sql-database-normalization-explained-in-simple-english/)
- [SQL Performance Tuning](https://www.sqlshack.com/sql-performance-tuning/)
- [Database Security Best Practices](https://www.csoonline.com/article/3533627/database-security-best-practices.html)

Note : This concepts are applicable to various database systems, and specific implementations may vary based on the DBMS being used. Always refer to the documentation of your chosen DBMS for details on syntax and features.


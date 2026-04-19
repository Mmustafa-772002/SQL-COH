# SQL-COH
SQL-COH is a comprehensive collection of SQL queries, commands, and best practices used to perform various database operations efficiently.

## TABLE OF CONTENTS
- [Database](#database)
- [Table](#table)
- [Data Types](#data-types)
- [Constraints](#constraints)
- [Indexes](#indexes)
- [Common Table Expressions (CTEs)](#ctes)
- [Window Functions](#window-functions)
- [Views](#views)
- [Stored Procedures](#stored-procedures)
- [Triggers](#triggers)
- [Functions](#functions)
- [Transactions](#transactions)
- [Joins](#joins)
- [Subqueries](#subqueries)
- [Aggregate Functions](#aggregate-functions)
- [String Functions](#string-functions)
- [Date Functions](#date-functions)
- [Mathematical Functions](#mathematical-functions)
- [Logical Functions](#logical-functions)
- [User Management](#user-management)
- [Backup and Restore](#backup-and-restore)
- [Performance Tuning](#performance-tuning)
- [Security](#security)
- [Best Practices](#best-practices)
- [Resources](#resources)

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


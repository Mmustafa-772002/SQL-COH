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
# Database 
A database is an organized collection of data that can be easily accessed, managed, and updated. It is designed to store, retrieve, and manage data efficiently. Databases are used in various applications, from small personal projects to large enterprise systems.
## Database types 
1. realtional databases (RDBMS):
A relational database is a type of database that organizes data into tables (or relations) consisting of rows and columns. Each table represents a specific entity, and the relationships between tables are established through keys. Examples of relational databases include MySQL, PostgreSQL, Oracle Database, and Microsoft SQL Server.
2. NoSQL databases:
NoSQL databases are designed to handle unstructured or semi-structured data and provide high scalability and flexibility. They do not use the traditional table-based structure of relational databases. Examples of NoSQL databases include MongoDB, Cassandra, Redis, and Couchbase.
3. In-memory databases:
In-memory databases store data in the main memory (RAM) rather than on disk, allowing for faster data access and processing. They are often used for real-time applications and caching. Examples of in-memory databases include Redis, Memcached, and SAP HANA.
4. Graph databases:Graph databases are designed to represent and manage data in the form of nodes, edges, and properties. They are particularly useful for applications that involve complex relationships between data, such as social networks and recommendation systems. Examples of graph databases include Neo4j, Amazon Neptune, and ArangoDB.
5. Time-series databases:   
Time-series databases are optimized for storing and querying time-stamped data, such as sensor data, financial data, and log data. They provide efficient storage and retrieval of time-series data. Examples of time-series databases include InfluxDB, TimescaleDB, and OpenTSDB.
6. Object-oriented databases:
Object-oriented databases store data in the form of objects, which can contain both data and methods. They are designed to work with object-oriented programming languages and provide a more natural way to represent complex data structures. Examples of object-oriented databases include ObjectDB, db4o, and Versant Object Database.
7. Columnar databases:
Columnar databases store data in columns rather than rows, which can improve query performance for certain types of analytical workloads. They are often used in data warehousing and business intelligence applications. Examples of columnar databases include Apache Cassandra, Amazon Redshift, and Google BigQuery.
8. Distributed databases:
Distributed databases are databases that are spread across multiple physical locations, often across different servers or data centers. They provide high availability, fault tolerance, and scalability. Examples of distributed databases include Apache Cassandra, Amazon DynamoDB, and Google Cloud Spanner.
9. Cloud databases:
Cloud databases are databases that are hosted and managed in the cloud, providing scalability, flexibility, and ease of access. They can be either relational or NoSQL databases. Examples of cloud databases include Amazon RDS, Microsoft Azure SQL Database, and Google Cloud SQL.
10. NewSQL databases:
NewSQL databases are a class of relational databases that aim to provide the scalability and performance of NoSQL databases while maintaining the ACID (Atomicity, Consistency, Isolation, Durability) properties of traditional relational databases. Examples of NewSQL databases include CockroachDB, VoltDB, and NuoDB.
11.Non-relational databases:
Non-relational databases, also known as NoSQL databases, are designed to handle unstructured or semi-structured data and provide high scalability and flexibility. They do not use the traditional table-based structure of relational databases. Examples of non-relational databases include MongoDB, Cassandra, Redis, and Couchbase.

---
#

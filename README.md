<h1 align="center"> Learn SQL for Data Analysis </h1>

I am building this repository for study purposes. I am on the journey to become a Data Analyst, and I want to share what I have learned along the way.

<p align="center"> <img src="https://www.dataquest.io/wp-content/uploads/2021/11/why-sql-consumes-so-much-memory-header.webp" alt="SQL" width="50%" height="10%"/> </a> </p>

The Structured Query Language (SQL) was first developed in 1970 by researchers at IBM. The initial version was created to manage and retrieve data from IBM's original relational databases called "System R". A few years later, the SQL language became publicly available. The American National Standards Institute (ANSI) and the International Standard Organization (ISO) then took the SQL language as the standard for communicating with relational databases. While some DBMS (Database Management Systems) have altered the language, the majority still follows the ANSI-approved version of SQL programs.

## About the Content

The content of this repository covers the essential SQL commands. Some of the material is based on the book ["Getting Started with SQL"](https://www.amazon.com/Getting-Started-SQL-Hands-Beginners/dp/1491938617/ref=sr_1_1?crid=RVXQWN6KCAGY&keywords=getting+started+with+sql&qid=1675856434&sprefix=getting+started+with+sql%2Caps%2C261&sr=8-1) by Thomas Nield, published by O'Reilly. However, the SQL code will always be written using MySQL, one of the many DMBS for relational databases available in the market. In some cases, I will highlight the differences in queries and commands between MySQL, SQL Server, and SQLite. Additionally, we will delve into SQL and some NoSQL databases for data analysis.

Note 1: All of this content is written in the form of "notes" by me. I encourage you to take some time and read the official documentation for the SQL language. I will always provide these references and others at the end of each topic.

Note 2: At the time of viewing this, I may still be in the process of developing the content and updating this repository. As a result, you may encounter some unclickable topics. The updates to these topics do not follow a specific order and are based on my needs and study progress. Follow me to stay updated on new upgrades.

## Prerequisites
1. Install [MySQL Community Server.](https://dev.mysql.com/downloads/) and the [MySQL Worbench.](https://dev.mysql.com/downloads/workbench/)
2. Have access and know [how to use terminal/command line.](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/windows-commands)

## Some of the Basics Commands

#### DQL (Data Query Language)

- SELECT: Retrieve data from database.

#### DML (Data Manipulation Language)

- INSERT: Insert data into a table.
- DELETE: Delete data from a database table.
- UPDATE: Update an existing data within a table.

#### DDL (Data Definition Language)

- ALTER: Change the structure of the database.
- CREATE: Create databases or objects, like tables and views.
- DROP: Delete objects from database.
- RENAME: This is used to rename an object existing in the database.

#### DCL (Data Control Language)

- GRANT: Give privileges access to database. 
- REVOKE: Withdraws the user's access privileges given by using the GRANT command.

#### TCL (Transaction Control Language) 

- COMMIT: Commits a Transaction. 
- ROLLBACK: Rollbacks a transaction in case of any error occurs.
- SAVEPOINT: Sets a save point within a transaction    

## Queries examples

Retrieves all data from table in a database:

```sql
    SELECT * FROM table_name;
```

Query anatomy:

- `SELECT` keyword retrieve data from a database.
- `*` symbol is used to select all columns in the table.
- `FROM` keyword specifies the name of the table from which the data will be retrieved.
- `table_name` is the name of the table in the database.


## Table of Contents

1. Select, Filter, Order and Operationals
2. Handling with Variables
3. Joining Tables
4. Aggregating Data for Analysis
5. Windows Function, Subqueries and Handling with date
6. Exploratory Data Analysis
7. Cleaning and Processing Data
8. Data Analysis
9. Programming
10. Optimizing SQL Queries

## Contact me 🔗 👇 

<a href="https://github.com/soareseric/" target="blank"><img align="center" src="https://img.shields.io/github/followers/soareseric?label=Follow&style=social&link=https://github.com/soareseric/" alt="EricSoares" height="20" width="90" /></a>
<a href="https://www.linkedin.com/in/eric-soares-maciel" target="blank"><img align="center" src="https://img.shields.io/badge/-EricSoares-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/eric-soares-maciel/" alt="EricSoares" height="20" width="100" /></a>

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

Sample use case: 

You are working for a logistics company that sends emails to customers to inform them about the status of their packages. The company has a database of all the emails sent, which includes the email ID, recipient email address, subject, body, and sending date.

1. Create the database and its tables:

```sql
    CREATE DATABASE logistics_email;
    
    USE logistics_email;
    
    CREATE TABLE emails (
        email_id INT AUTO_INCREMENT PRIMARY KEY,
        recipient VARCHAR(255) NOT NULL,
        subject VARCHAR(255) NOT NULL,
        body TEXT NOT NULL,
        sent_date DATE NOT NULL
     ); 
```

2. Insert values to those tables:

```sql
    INSERT INTO emails (recipient, subject, body, sent_date)
    VALUES
          ('recipient1@email.com', 'Package Update', 'Your package has been shipped', '2022-01-01'),
          ('recipient2@email.com', 'Package Delivery', 'Your package has been delivered', '2022-01-02'),
          ('recipient3@email.com', 'Package Delay', 'Your package has been delayed', '2022-01-03'),
          ('recipient4@email.com', 'Package Update', 'Your package is on its way', '2022-01-04'),
          ('recipient5@email.com', 'Package Arrival', 'Your package has arrived', '2022-01-05');
```

3. Update the email with the subject "Package Delivery" to "Package Delivery Update":

```sql
    UPDATE emails
    SET subject = 'Package Delivery Update'
    WHERE email_id = 2;
```

4. Add a new column called "status" with "Pending" as its default value:

```sql
    ALTER TABLE emails
    ADD COLUMN status VARCHAR(20) NOT NULL DEFAULT 'Pending';
```

5. Retrieve the number of emails sent to each recipient email address and the average length of the email bodies:

```sql
    SELECT 
        recipient,
        COUNT(email_id) as total_emails,
        AVG(LENGTH(body)) as avg_body_length
    FROM emails
    GROUP BY recipient;
```

6. Retrieve the number of emails sent to each recipient email address and the average length of the email bodies only for the emails sent in the last week:

```sql
    SELECT 
        recipient,
        COUNT(email_id) as total_emails,
        AVG(LENGTH(body)) as avg_body_length
    FROM emails
    WHERE sent_date >= DATE_SUB(NOW(), INTERVAL 7 DAY)
    GROUP BY recipient;
```

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

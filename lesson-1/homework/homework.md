# Lesson 1: Introduction to SQL Server and SSMS

> **Notes before doing the tasks:**
> - Tasks should be solved using **SQL Server**.
> - Case insensitivity applies.
> - Alias names do not affect the score.
> - Scoring is based on the **correct output**.
> - One correct solution is sufficient.

## Easy
1. Define the following terms: data, database, relational database, and table.
**Answer**
data- these are raw (unprocessed) facts, numbers, texts, or symbols about people, objects, events, or concepts that do not have any meaning in isolation.
database- it is a collection of data stored and organized in a way that allows for easy access, management, and updating of the data.
relational database- in this case, data is stored in tables and there are relationships between these tables.
table- a structure for storing data organized into rows and columns
2. List five key features of SQL Server.
**Answer**
Five key features of SQL Server for analytics and BI (business intelligence): 1) Support for different data types; 2) Analytics and reporting; 3) Comprehensive set of tools; 4) Built-in analytical services; 5) Performance and scalability.
3. What are the different authentication modes available when connecting to SQL Server? (Give at least 2)
**Answer**
There are two main authentication modes available when connecting to SQL Server: Windows Authentication (Windows authentication only) and Mixed Mode.

## Medium
4. Create a new database in SSMS named SchoolDB.
**Answer**
--create database SchoolDB
--use SchoolDB
5. Write and execute a query to create a table called Students with columns: StudentID (INT, PRIMARY KEY), Name (VARCHAR(50)), Age (INT).
**Answer**
use SchoolDB 
create table Students (StudentID int primary key, Name varchar(50), Age INT)
6. Describe the differences between SQL Server, SSMS, and SQL.
**Answer**
SQL Server is the database itself;
SSMS is the program for working with the database;
SQL is the language for writing queries.

## Hard
7. Research and explain the different SQL commands: DQL, DML, DDL, DCL, TCL with examples.
**Answer**

DQL - DQL commands are used to retrieve data from the database.
--SELECT
select * from BOOKS

DML - DML commands are used to manipulate the data within database tables.
--INSERT; UPDATE; DELETE
insert into BOOKS values
(1, 'Don Quixote', 'Miguel de Cervantes', 'Classic', 'readed')

DDL - DDL commands are used to define and manage the structure of database objects like tables, indexes, and views.
--CREATE; ALTER
create table BOOKS (BOOKID int, NAME varchar(50), AUTHOR varchar(50), GENRE varchar(50), STATUS varchar(15))

DCL - DCL commands are used to manage user permissions and access control to the database. 
--GRANT; REVOKE
grant select, insert on BOOKS TO 'user1'

TCL - TCL commands manage transactions in the database, ensuring data consistency. 
--COMMIT; ROLLBACK; SAVEPOINT

8. Write a query to insert three records into the Students table.
**Answer**
select * from Students
insert into Students values
(1, 'Alex', '25'),
(2, 'Josh', '38'),
(3, 'Justin', '28')
select * from Students

9. Restore AdventureWorksDW2022.bak file to your server. (write its steps to submit)
**Answer**
Tasks->Restored->Database->Devise->...->Add->sellect AdventureWorksDW2022.bak DB->Ok->write the name of the database. At the end the inscription appears: 'Database restored successfully'.
   You can find the database from this link :`https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorksDW2022.bak`

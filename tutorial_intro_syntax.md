## SQL intro
데이터베이스에 데이터를 저장, 처리, 검색하는 표준 언어.

#### SQL은 무엇인가?
 - Structured Query Language의 약자로, 데이터베이스에 접근 및 처리를 가능하게 하고 ANSI (American National Standards Institute) standard임.

#### What Can SQL do?
 - SQL can execute queries against a database
 - SQL can retrieve data from a database
 - SQL can insert records in a database
 - SQL can update records in a database
 - SQL can delete records from a database
 - SQL can create new databases
 - SQL can create new tables in a database
 - SQL can create stored procedures in a database
 - SQL can create views in a database
 - SQL can set permissions on tables, procedures, and views

#### Using SQL in Your Web Site
- To build a web site that shows data from a database, you will need:

	- An RDBMS database program (i.e. MS Access, SQL Server, MySQL)
	- To use a server-side scripting language, like PHP or ASP
	- To use SQL to get the data you want
	- To use HTML / CSS to style the page

#### RDBMS
 - Relational Database Management System.
 - the basis for SQL.
 - The data in RDBMS is stored in database objects called tables.
 - CustomerID, CustomerName, ContactName, Address, City, PostalCode and Country.

 
#### Database Tables
 - A database most often contains one or more tables. Each table is identified by a name (e.g. "Customers" or "Orders"). Tables contain records (rows) with data.

```
SELECT * from Customers;
```
The above SQL statement selects all the records in the "Customers" table.

#### 주의할 점...
 - SQL 키는 대소문자 구별이 없다: select는 SELECT와 같음.

#### Semicolon after SQL Statements?
 - Semicolon is the standard way to separate each SQL statement in database systems that allow more than one SQL statement to be executed in the same call to the server.

#### SQL 커맨드 중 중요한 것 몇가지
 - SELECT - extracts data from a database
 - UPDATE - updates data in a database
 - DELETE - deletes data from a database
 - INSERT INTO - inserts new data into a database
 - CREATE DATABASE - creates a new database
 - ALTER DATABASE - modifies a database
 - CREATE TABLE - creates a new table
 - ALTER TABLE - modifies a table
 - DROP TABLE - deletes a table
 - CREATE INDEX - creates an index (search key)
 - DROP INDEX - deletes an index


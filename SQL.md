## Database

- Database is a collection of data in digital format which can be easily accessed

- A software application used to manage our DB - `Database Management System`

## Types of Database:

- `relational DB`:stores data in tables (rows and columns) and uses relationships (keys) to connect data between tables.
  `Ex`:MySQL, PostgreSQL, Oracle, SQL Server.
- `Non relational DB`: A Non-Relational Database (NoSQL) stores data in non-tabular formats like JSON, key-value, or graphs.
  `Ex`:MongoDB, Cassandra, Redis, Neo4j.

## SQL

- its a programming language used to interact with relational DB
- SQL (Structured Query Language) is used to create, read, update, and delete data in a relational database.

* **`Table`**:A collection of data stored in rows and columns (like a spreadsheet).
* **`Column`**: A vertical field that defines a data type (e.g., name, age).
* **`Row`**: A single record of data in the table (one complete entry).

### `NOTE: put `;` at the end of query`

## Create a Database

- Query:
  - `CREATE DATABASE college`
- creating a database ,whose name is `college`

### NOTE: its madantory to write `USE db_name` before creating tables or doing any query

## Create a Table

- syntax:
  - _create table table_name(
    **col_name** **datatype** **constraints**
    )_
- Query:
  - `CREATE TABLE STUDENT(
  id INT PRIMARY KEY,
  name VARCHAR(50),
  age INT NOT NULL
)`;
- we created a table whose name is `STUDENT`
- `id`,`name`,`age`,these are the coloumns of the table with the provided datatypes

### NOTE

- `We can wirte sql commands in lowercase letters also`

## SQL Datatypes

- ![alt text](assets/SQL/image1.png.png)

### `CHAR` VS `VARCHAR`

- `CHAR`:Fixed length. Always uses full size.
- **Ex :** name CHAR(50)
- so if name is **arnav**,length is 5,but in memory 50 bytes has been alloted to `name` ,so the remaining space get wasted,thats why using `char` is ineffecient
- `VARCHAR`: Variable length. Uses only needed space
- **Ex :** name VARCHAR(50)
- so if name is **arnav**,length is 5,then only 5 bytes will get alloted to `name`,so it can use space upto 50
  Thats why use VARCHAR
- `we can use lowercase letters also for datatypes`

## Inserting some data`s

- **case 1 :** Inserting multiple datas
  - Query: - `INSERT INTO STUDENT (id,name,age) VALUES (1,"arnav",20),
(2,"Rathor",21)`;
- **cas 2 :** Inseting only single data(row)
  - Query:
    - `INSERT INTO STUDENT VALUES(1,"arnav",20)`;

### To read the table

- `Select`
- query: -`SELECT * FROM STUDENT`
- here `*` all coloumns,it will fetch all the rows and coloumns

Some Direct concepts to recap the knowledge on SQL 

#### __Delete vs truncate__ 

- Delete command deletes a row in table and you can rollback , this commands beong to data manipulation family.
- Truncate command deletes and cant rollback, faster than delete  -it belongs to Data definition.


__What are subsets of sql__ 

1. Ddl - Data Definition schema -  define schema 
2. DML - Data Manipulation Language 
3. DCL - Data control Language - right permission of data 
4. TCL - Transaction control language - rollback etc 

__What is DBMS__ 

DBMS interacts with user and database itself to capture and analyse data, data stored can be modifiedd , retrived, delected

hierarichal - tree
relational - 
network - many to many 
object-oriented -- conain objects 

__WHat is TABLE__

Table - table refers to collection of data in organised manner 
field - number of columns in a table 

__What are joins in SQL__

joins in sql - merge 2 table 

- innerjoin - this join return thoose records which have matching value in both tables

- full join - thsi join return all those recods which either have a match in left or right table 

- left join - this join returns records from left table and all recods which satisfy the condition from the right table

- right join - returns records from the right table and those records which satisfy the condition from left table 


__What is difference between char and varchar2__

These are datatype in sql 

- char - strings of sixed length 
- varchar 0 strings of variable length 


__What is primary key__ 

It is set of attributes that can uniquely identify every tuple is a primary key. 1 can be choosen as primary key 

__What are constraints__

Constraints specify the limit on the datatype of the table , it can be specified while creating or altering the table statement 
not null, unique, check(satisfy condition), default(if no value), index 


__What is difference between sql vs mysql__

sql - structure query language - standard language which is core of relational db 

Mysql - relational database management system , works on various platforms and is backed by oracle


__What is Unique Key__

This key uniquely identifies a single row in a table , multiple values are allowed per table , null values are allowed but duplicate not allowed.

__What is foreign key__

This key maintains referential integrity by enforcing a link between data in 2 tables.
foreign key in the child table references the primary key in the parent table. the contraint in foreign key prevents  actions that would destroy the links between child and parent table


__What is Data integrity__ 

It defines accuracy of data, consistency of data, Integrity constraints to enforce business rules on data 


__Differece between clutered index and non-clustered index__

- Clustered index - used for easy retrieval of data from database and is faster
one table can have only 1 clustered index

- Non clustered index - used for easy retrieval of data from database and is slower
1 table can have many non-clustered index

- unique index - this index doesnot allow field to have duplicate values if colum is unique indexed, if primary key is defined , unique index can be applied automatically.

__How will you display DISPLAY current date__

GETDATE()  2017, 2008R2, 2012, 2016 
select GETDATE();





__What is denormalisation__ 

A technique that increase the performance of the entire infrastructure as it introduces redundancey to the table
adds the redundant data to the table by add database queries that combine tdata from various tables in to a single table 


__what is Index__

 Performance tuning method allows faster retrieval of records from the table , creates and entry for each vallue

clustered  - reorders the physical order of table and searches based on key values (only 1 clustered index) 
nonclustered - does not reorders but maintains a logical order of data (many nc index)
, 



__What is normalisation__

process of organising data to avoid duplication and redundancy 
advantages - better db organisation, more tables with smaller rows, efficient data access, greater flexibility with queries, more compact db etc 


__drop vs truncate__

- drop - removes a table and it cannot be rolled back from database 
exa - drop object objectname

- truncate - removes all rows from the table and cannot be rolled back into database 
truncate table tablename


__What are Normalisation types and forms__

- 1nf - each cell with single record
- 2nf - apply single column primary key with 1NF 
- 3nf - transitive functional dependency with 2NF 
- bcnf - scenarios with anomalies (data in 3nf format) 


__What is ACID Property__ 

Data transactions are processesed reliably in the system 
Atomicity, Consistency, Isolation and Durability

- Atomicity -- transaction that are completely done or failed,  where transaction is single logic operation of data.
if one part of transaction fails than entire transaction fails , database is left unchanged

- Consistency - data must meet all validation rules, transaction never levaves the database without completeing its state

- Isolation - main goal is concurrency control 

- Durability - if a transaction has been commted, it will occur, whatever may come in between exa - crash or error


__What is Trigger in sql__

Special type of stored procedures that are defined to execute automatically in place or after data modifications
it allows you to execute a batch of code when an insert, update or any other query is executed against a specific table.


- before insert , after insert 
- before update after update 
- before delete , after delete 



__What are the operators in sql__

- Arithmetic, 
- Bitwise, 
- Comparison, 
- Compound, 
- Logical 


Null value vs zero or blank space -  NOT Same..

Null value is a unavailable value 
zero is a number
blank space is a character


__Difference between Cross join vs natural join__

cross join - cross product or cartesian product 
natural join -based on all column names having the same name and data types in both tables


__What is SUBquery in sql__

subquery is a query inside another query where a query is defined to retrieve data or informatioon back from db 

select ln, fn from employees whhere addresscode in (select addresscode from office where country = "india")


__What are different types of subqueries__

- correlated subquery - these are queries which select the data from a table referenced in the outer query,it is not considered an independent query as it refers to some column in the table 

- non-correlated subquery - this query is independent query where the output of subquery is substituted in main query. 


__How to count records ina a table__


1. select * from table; and then count 

2. select count(*) from table1;

3. select rows from sysindexes where id = object_id(table1) and indid < 2;



__Write an sql query to find the names of employees that begin with alphabet a__


- select * from table_name where empname like 'A%'

__Write sql query to find the names of employees that end with alphabet a__


- select * from table_name where empname like '%A'


__Write sql query to get the 3rd highest salary of an employee from employee table__


- select top 1 salary from (select top 3 salary from employee_table order by salary desc) as emp order by salary Asc;



__What are group functions__

avg, count,, max, min , sum,  variance, 


__What are relationships__

- relation or links are between entities that have some thing to do with each other,

- relationships are the connection between the tables in a database

1 to 1--- table a and table b 
1 to many - 1 record in table a related to many recorde in table b 
may to 1 - many in table a related to q in table b 
self referencing relationship 


ways to insert null value in column while inserting data 
1 implicitly by omitting column from column list 
2. explicitly by specifying null keyword in values clause



Difference between Between and in 
beetween - used to display result based on range of values in a row 
roll number between 10 and 15 

In - used to check values contained in specific set of values
roll_no in (1, 2, 3, 4,9)


sql functions 
to perform some calculation on the data 
to modify individual data items
to manipulate the output 
to format dates and numbers
to convert the datatypes


Merge - allows conditional update or insertion , if a row exists or not 




Recursive stored procedure - refers to a  stored procedure which calls by itself until it reaches some boundary condition 
thsi recursive function or procedure helps the programmers to use the same set of codde n number of times


clause - limit the result by providing a condition to query. clause helps to filter the row from wntire set of records 

WHere and Having 

having clause - can be used only with sleect statement , usually used in group by clause
where clause - applied to each row befor they are part of group by function in a query 


case manipulation function in sql 
lower - returns string in lower
upper - in upper
initcap - titlecase


different set operator in sql 
Union - result bothe from left and rigt query 
intersect - only the ones common to both 
minus - left - right -keeps rows from left that are not in right



ALIAS - name given to any table or column, identifies a table or coolumn 

select <> from empl as <alias> where <>=<>

aggregate function - math calcs that return single value - count, mean, sum, min, max
scalar funct - return single values based on inputs 

 
pattern matching like "A%"  , Like "ABC_"

SQL vs plsql - sql is a query language that allows u to issue a single query or single incert update or delecat 

pl/sql - is oracles procedural language swl which allows u to write programeme
(loops variables etc) to accomplisg multiple operations successfully select , inser, update delete 


STORED procedure - a function with many sql statements to acces sthe database system

several sql statements are consolidated into a stored procedure and are executed whenever and wherever required. , thsi saves time and avoid writing code again and again 

advantages - used for modular programmin, create once and call multiple tmes, supports faster execution, reduces network traffic.

disadvantages - only disadv is that it can be executed only in database and utilises more memory in database server 


local vs global variables
local - exiss inside the function 
global - accessed throughout the program



Autoincrement in sql - allows the user to create a unique number to get generated wherever a  new record is inserted in to the table 
thsi keyword is usually required whenever primary key is used
auto increment keyword can be used in oracle and identity keyword can be used in sql server 




datawarehouse - refers to a central repository of data where the data is assembled from multiple sources of information
consolidated, transformed and processed.


stuff fuction overwrites existing char or inserts a string into another string 

replace function replaces existing chars of all occurences

STUFF(string, start, lenth, replacementchars)

Replace(string, search-string, replacemet-string)

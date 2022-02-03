# MySQL

---------------------------------------- MySQL ------------------------------------------------
       MySQL is a Database Management System/ or a software why which we can manage our database.

       Database: is a collection of data stored in a format that can easily be accessible.[update/delete/add]



                                            Collection of Data
                                    ------------------------------------
                                    |  Name          | Age  |   Gender    
                                    |----------------|------|------------
                                    |  Ram Kumar     |  21  |    Male     
                                    |  Meera Khan    |  22  |    Female       
                                    |  Sarita Kumari |  21  |    Female
                                    |  Anil Kapoor   |  22  |    Male
                                    -----------------------------------





        Client<------------->DBMS<-----------------> DataBase
                DBMS helps to access data to client from database 
                Some popular DBMS software:
                    * Oracle
                    * MySQL
                    * MS SQL Server
                    * PostgreSQL
                    * MongoDB

        There are two Types of database:
            1. Relational 
            2. NoSQL

            1> Relational database:

                        ---------------
                        |             |                                           -------------    
                        |             |                                           |           |
                        |  TABLE-1    |                                           |           |
                        |             |                                           |  TABLE-2  |
                        |             |-----------------------------------------> |           |
                        |             |                                           |           |
                        |             |                                           |           |
                        |             |                                           |           |
                        |             |                                           |           |
                        ---------------                                           -------------
                              |          
                              |          
                        -------------                        ---------------
                        |           |                        |             |                  
                        |           |                        |   TABLE-4   |                  
                        |  TABLE-3  |                        |             |                  
                        |           |                        |             |                  
                        |           | ---------------------> |             |                  
                        |           |                        |             |                  
                        |           |                        |             |                  
                        |           |                        |             |                  
                        -------------                        ---------------
                             |
                             |
                        -------------                        ---------------               --------------
                        |           |                        |             |               |             |
                        |           |                        |  TABLE-6    |               |             |
                        |  TABLE-5  |                        |             |               |  TABLE-7    |
                        |           |----------------------->|             |-------------->|             |
                        |           |                        |             |               |             |
                        |           |                        |             |               |             |
                        |           |                        |             |               |             |
                        |           |                        |             |               |             |
                        -------------                        ---------------               ---------------

        * Every table is linked to eachother that's why this is called RDMBS[Relational DataBase Management System].
        * RDMBS use a language to communicate with database that is known as SQL.





            2> NoSQL 
                * NoSQL is not a Table-based Database.
                * NoSQL databases are document based.
                * MongoDB, Redis, Cassandra etc.



    ------------------- Advanatage of MySQL
    * Cross Platform we can write code in any platoform, means any os, window,mac,linux etc.
    * Used with multiple languages (PHP, NodeJS,Python, etc).
    * MySQL is RDBMS: means we can access data by writing a single command
    * The MySQL Database Server is very fast, reliable, scalable, and easy to use.
    * MySQL Server works in client/server or embedded systems.


    Popular website using MySQL
        * Facebook
        * Twitter
        * Google
        * Wikipedia
        * youtube
        * Pinterest



    ------------------ MySQL Create Table
    for making table required three things:
         Table_Name: Student Information.
         Columns    : Name,age,gender
         ColumnData type : Name->string,age->numeric,gender->string


         commands for create table:
                CREATE TABLE table_name(
                    column1 datatype,
                    column2 datatype,
                    column3 datatype,
                    ......
                );

    ----------------- Datatypes in MySQL
    Three types of category in Datatypes:
        1. String
        2. Numeric
        3. Data and Time

        1. String datatype in sql: use for store string difference for length only.
                1. CHAR(size)       :   0 to 255    size=5//only 5 char can be stored
                2. VARCHAR(size)    :   0 to 65535
                3. BINARY(size)     : same like above but here we can store only binary value.
                4. VARBINARY(size)
                5. TINYTEXT         : 255 characters fixed
                6. TEXT(size)       : 65,535 bytes data save in byte
                7. MEDIUMTEXT       : 16,777,215 characters
                8. LONGTEXT         : 4,294,967,295 characters
                9. TINYBLOB         : 2255 bytes    [these blog stored data in the form of blog]
                10. BLOB(size)      : 65,535 bytes
                11. MEDIUMBLOB      : 16,777,215 bytes
                12. LONGBLOB        : 4,294,967,295 bytes
                13. ENUM(val1,val2,val3,...)    : list up to 65535 values
                14. SET(val1,val2,val3,....)    : list up to 64 values


        2. Numeric Datatypes in MySQL : use fo store numeric data.
                1. BIT(size)           : 1 to 64 number
                2. TINYINT(size)       : 128 to 127
                3. INT(size)           : -2147483648 to 2147483647
                4. INTEGER(size)       : same as int
                5. SMALLINT(size)      : -32768 to 32767
                6. MEDIUMINT(size)     : -8388608 to 8388607 
                7. BIGINT(size)        : -9223372036854775808 to 9223372036854775807
                8. BOOL                : 0/1
                9. BOOLEAN             : 0/1
                10. FLOAT(p)           :  float and double are same
                11. DOUBLE(size,d)     :  255.568 [d-> we can decide how many digit are come after dot]
                12. DECIMAL(size,d)    :  size=60,d=30 
                13. DEC(size,d)        :   same as decimal
            

        3. Date & Time Datatypes in MySQL
                1. DATE             : 1000-01-01 to 9999-12-31 'yymmdd' -> formate are same.
                2. DATETIME(fsp)    : YY-MM-DD hh:mm:ss
                3. TIMESTAMP(fsp)   : past time formate like 2nd
                4. TIME(fsp)        : hh:mm:ss //only for store time
                5. YEAR             : four-digit format : 1901




    ---------------- practice
    create DATABASE student;

    Example : suppose we have a database name of student;
    * Commands:
        use student;        //use student database ->select student database
        CREATE TABLE personal(
            id INT,                     //id of student
            name VARCHAR(50),         // name with 50 char
            DOB DATE,               //date of birth
            phone VARCHAR(1),      // 12 digit for phone number 
            gender VARCHAR(1)       //f->femail, m ->mail
        )

    o|p:    id      name        DOB         phone       gender          //these are the filed created.


    *********** another table.
        //p-> product;
        CREATE TABLE product(
            pid INT,
            pname VARCHAR(50),
            pcompany VARCHAR(50),
            pprice INT
        )

        -------------------------------------------------------------------------------------------
        |linux command to start sql
        |    
        |    mysql -u "userName" -p          //it as a password to start sql
        |
        |    set username and password
        |    systemctl status mysql.service      //show which database is installed.
        |    \! clear            // clear screen.
        |    \q                  //for exit the sql console.
        |    sudo /usr/bin/mysql_secure_installation     //change root password if not set yet.
        -------------------------------------------------------------------------------------------


================================================== SQL Commands ======================================

    ACID properties in transaction:

        A : Atomicity   [if transaction not commit then it rollback to initial state.(either it is done or not do anything.)]
        C : Consistency [before transacation start and after the transaction complete, sum of money should be same] A+B =befor start total money.
         A-1000
         B+1000
         total money = A-1000+B+1000=A+B(total money)after complete total money.
        I : Isolation : we try to convert parallel transaction to serial transaction.{they are interface in each other operation.}
            [by this we got consistency.]
        D : Durability : all changes in database are permanat.


    Primary Key : {Unique + Not null}
        use for uniqly identify data record.
        it can not be null.
        example: roll no. or registration number.
        Note: only one primary key is present in database.

    Candidate key : uniquly identify but it may be null.

    Foreign Key : it is an attribute or set of attribute.that provides a link between data in two tables.
        [reference integrity]. foreign key referenced to primary key of any table.









    Types of sql commands : use for deal with structure data, in the form of table form data or realtion data.

    DDL[Data Definition Language]   DML[Data Manipulation Language]     DCL[Data Control Lanauge]
    *Create                             *Selecte                           * Grant
    *Alter                              *Insert                            * Revoke
    *Drop                               *Update 
    *Truncate                           *Delete
    *Rename
    
    table schema are used for store data in sql.
    alter : use for change name.
    drop  : delete table/structure.
    truncate : delete data from structure.

    Grant : given the permision to access structure.
    revoke : remove permision.



    Create Command:
        use for create table in data base.

        CREATE table table_name(
            Id int,
            name VARCHAR(20),
            address VARCHAR(30)
        )

 op :   | Id   |   Name   |   Address|       



 Selection query:
    select c1,c2;       //selection only c1 & c2
    select c4,c3;       //select c4 first then c3.
    select * ;          //select every thing .
    select * marks+5        //give after add 5 in marks.
    

   

    1. Select all the details of Bank Branches.?
        Ans: select * from branch;
    2. Find the name of all customers having bank account.
        Ans: select C_name from Depositor. or select distinct c_name from Depositor. //select only unique name. 
    3. Find each loan along with amount.
        Ans: slect loan_no, amount from Loan;
    4. Find all account no and balance wit 6% yearly interest.
        Ans: select Account_no,balance*1.06 from Account;


    Select with where:
        use for specified codition.

        we can use keyword:<,>,<=,>=,=,<> etc, or, and, or, not etc, allow between operator.


    1. All account number where balance is less than 1000.
        Ans: 

        select Account_no
        from Account
        where balance<1000;

    2. Find branch name which is situated in delhi and having assets <100000.
        Ans: select Branch_name
             from   Branch
             where Branch_City = 'Delhi' and assets <100000;

    3. Find branch_name, and Account_no, where balace is >=100 and <=1000
        Ans: select Branch_name, Account_no
             from Account
             where balance>=100 and balance <=1000; or where balacnce between 100 and 1000.[boundry value included.]




============================SQL=================================
1. show databases;              //show database
2. create database [db_name]    //create database
3. use [db_name]                //use database
4. drop database [db_name]      //delete database
5. create table [table_name] (col1, col2, col3, col4, ......);      //create table.
6. show tables;
7. desc [tb_name]           //show complete description
8. drop table [table_name]      //delete table
9. alter table [old table name] rename to [new name]        //change table name.
10. truncate table [table name]                                             //The TRUNCATE TABLE command deletes the data inside a table, but not the table itself. 
11. insert into [table name](id,name,city) values(12,"sheesh","Dhanaura");
12. insert into [table name]values(12,"Sheeshpal","Dhanaura");
13. alter table [table name] add col1_name data_type;                    //add one more col into table
14. alter table table_name rename column Col_name to new_col_name;      //change attribute name.
    or  
    alter talbe table_name chanage col_name new_col_name char(50);      //change attribute name with data type 
15. update table_name set country="India" where name = "Sheeshpal";
    update [table_name] set col= value , col = value where col=value;


example:
    create table users (id int primary key,name VARCHAR(30) not null,address VARCHAR(50));          //create table of user with three attribute.


16. delete from Student where id=12;        //delete id=12 student;     without condition it delete everything from table.

-----------------****************
mysql> select * from student;
+----------+---------+---------+---------+
| id       | name    | city    | country |
+----------+---------+---------+---------+
|       23 | ankit   | delhi   | ind     |
|       24 | sanket  | lucknow | india   |
|      234 | ishant  | lucknow | india   |
|      246 | sumit   | lucknow | india   |
|     2334 | aman    | kanpur  | india   |
| 24234236 | ramsigh | lucknow | india   |
+----------+---------+---------+---------+
6 rows in set (0.00 sec)





mysql> select * from student;
+----------+---------+---------+---------+
| id       | name    | city    | country |
+----------+---------+---------+---------+
|       23 | ankit   | delhi   | ind     |
|       24 | sanket  | lucknow | india   |
|      234 | ishant  | lucknow | india   |
|      246 | sumit   | lucknow | india   |
|     2334 | aman    | kanpur  | india   |
| 24234236 | ramsigh | lucknow | india   |
+----------+---------+---------+---------+
6 rows in set (0.00 sec)







mysql> select * from student where city='lucknow';
+----------+---------+---------+---------+
| id       | name    | city    | country |
+----------+---------+---------+---------+
|       24 | sanket  | lucknow | india   |
|      234 | ishant  | lucknow | india   |
|      246 | sumit   | lucknow | india   |
| 24234236 | ramsigh | lucknow | india   |
+----------+---------+---------+---------+
4 rows in set (0.00 sec)








mysql> select * from student where country='india';
+----------+---------+---------+---------+
| id       | name    | city    | country |
+----------+---------+---------+---------+
|       24 | sanket  | lucknow | india   |
|      234 | ishant  | lucknow | india   |
|      246 | sumit   | lucknow | india   |
|     2334 | aman    | kanpur  | india   |
| 24234236 | ramsigh | lucknow | india   |
+----------+---------+---------+---------+
5 rows in set (0.00 sec)





mysql> select * from student where country='india';
+----------+---------+---------+---------+
| id       | name    | city    | country |
+----------+---------+---------+---------+
|       24 | sanket  | lucknow | india   |
|      234 | ishant  | lucknow | india   |
|      246 | sumit   | lucknow | india   |
|     2334 | aman    | kanpur  | india   |
| 24234236 | ramsigh | lucknow | india   |
+----------+---------+---------+---------+
5 rows in set (0.00 sec)








mysql> select name,city,country from student where country='india';
+---------+---------+---------+
| name    | city    | country |
+---------+---------+---------+
| sanket  | lucknow | india   |
| ishant  | lucknow | india   |
| sumit   | lucknow | india   |
| aman    | kanpur  | india   |
| ramsigh | lucknow | india   |
+---------+---------+---------+
5 rows in set (0.00 sec)






mysql> select name as  "USERNAME" , city as "CITYNAME" from student ;   //alias concept
+----------+----------+
| USERNAME | CITYNAME |
+----------+----------+
| ankit    | delhi    |
| sanket   | lucknow  |
| ishant   | lucknow  |
| sumit    | lucknow  |
| aman     | kanpur   |
| ramsigh  | lucknow  |
+----------+----------+
6 rows in set (0.00 sec)









mysql> select * from student where city='kanpur';
+------+------+--------+---------+
| id   | name | city   | country |
+------+------+--------+---------+
| 2334 | aman | kanpur | india   |
+------+------+--------+---------+
1 row in set (0.00 sec)







mysql> select * from student;
+----------+---------+---------+---------+
| id       | name    | city    | country |
+----------+---------+---------+---------+
|       23 | ankit   | delhi   | ind     |
|       24 | sanket  | lucknow | india   |
|      234 | ishant  | lucknow | india   |
|      246 | sumit   | lucknow | india   |
|     2334 | aman    | kanpur  | india   |
| 24234236 | ramsigh | lucknow | india   |
+----------+---------+---------+---------+
6 rows in set (0.00 sec)



mysql> select country from student;
+---------+
| country |
+---------+
| ind     |
| india   |
| india   |
| india   |
| india   |
| india   |
+---------+
6 rows in set (0.00 sec)





mysql> select distinct(country) from student;
+---------+
| country |
+---------+
| ind     |
| india   |
+---------+
2 rows in set (0.00 sec)





mysql> select * from student;
+----------+---------+---------+---------+
| id       | name    | city    | country |
+----------+---------+---------+---------+
|       23 | ankit   | delhi   | ind     |
|       24 | sanket  | lucknow | india   |
|      234 | ishant  | lucknow | india   |
|      246 | sumit   | lucknow | india   |
|     2334 | aman    | kanpur  | india   |
| 24234236 | ramsigh | lucknow | india   |
+----------+---------+---------+---------+
6 rows in set (0.00 sec)




mysql> select * from student where country='india' and  city='lucknow';
+----------+---------+---------+---------+
| id       | name    | city    | country |
+----------+---------+---------+---------+
|       24 | sanket  | lucknow | india   |
|      234 | ishant  | lucknow | india   |
|      246 | sumit   | lucknow | india   |
| 24234236 | ramsigh | lucknow | india   |
+----------+---------+---------+---------+
4 rows in set (0.00 sec)

mysql> select * from student where country='india' or city='lucknow';
+----------+---------+---------+---------+
| id       | name    | city    | country |
+----------+---------+---------+---------+
|       24 | sanket  | lucknow | india   |
|      234 | ishant  | lucknow | india   |
|      246 | sumit   | lucknow | india   |
|     2334 | aman    | kanpur  | india   |
| 24234236 | ramsigh | lucknow | india   |
+----------+---------+---------+---------+
5 rows in set (0.00 sec)






mysql> select * from student;
+----------+---------+---------+---------+
| id       | name    | city    | country |
+----------+---------+---------+---------+
|       23 | ankit   | delhi   | ind     |
|       24 | sanket  | lucknow | india   |
|      234 | ishant  | lucknow | india   |
|      246 | sumit   | lucknow | india   |
|     2334 | aman    | kanpur  | india   |
| 24234236 | ramsigh | lucknow | india   |
+----------+---------+---------+---------+
6 rows in set (0.00 sec)

mysql> select * from student where id >=24 and id<=2334;
+------+--------+---------+---------+
| id   | name   | city    | country |
+------+--------+---------+---------+
|   24 | sanket | lucknow | india   |
|  234 | ishant | lucknow | india   |
|  246 | sumit  | lucknow | india   |
| 2334 | aman   | kanpur  | india   |
+------+--------+---------+---------+
4 rows in set (0.00 sec)

mysql> select * from student where id between 24 and 2334;
+------+--------+---------+---------+
| id   | name   | city    | country |
+------+--------+---------+---------+
|   24 | sanket | lucknow | india   |
|  234 | ishant | lucknow | india   |
|  246 | sumit  | lucknow | india   |
| 2334 | aman   | kanpur  | india   |
+------+--------+---------+---------+
4 rows in set (0.00 sec)

mysql> select * from student where id >24 and id<2334;
+-----+--------+---------+---------+
| id  | name   | city    | country |
+-----+--------+---------+---------+
| 234 | ishant | lucknow | india   |
| 246 | sumit  | lucknow | india   |
+-----+--------+---------+---------+
2 rows in set (0.00 sec)

mysql> select * from student;
+----------+---------+---------+---------+
| id       | name    | city    | country |
+----------+---------+---------+---------+
|       23 | ankit   | delhi   | ind     |
|       24 | sanket  | lucknow | india   |
|      234 | ishant  | lucknow | india   |
|      246 | sumit   | lucknow | india   |
|     2334 | aman    | kanpur  | india   |
| 24234236 | ramsigh | lucknow | india   |
+----------+---------+---------+---------+
6 rows in set (0.00 sec)

mysql> select * from student where id=23 or id=234 or id=246;
+-----+--------+---------+---------+
| id  | name   | city    | country |
+-----+--------+---------+---------+
|  23 | ankit  | delhi   | ind     |
| 234 | ishant | lucknow | india   |
| 246 | sumit  | lucknow | india   |
+-----+--------+---------+---------+
3 rows in set (0.00 sec)

mysql> select * from student where id in(23,234,246);
+-----+--------+---------+---------+
| id  | name   | city    | country |
+-----+--------+---------+---------+
|  23 | ankit  | delhi   | ind     |
| 234 | ishant | lucknow | india   |
| 246 | sumit  | lucknow | india   |
+-----+--------+---------+---------+
3 rows in set (0.00 sec)

mysql> select * from student;
+----------+---------+---------+---------+
| id       | name    | city    | country |
+----------+---------+---------+---------+
|       23 | ankit   | delhi   | ind     |
|       24 | sanket  | lucknow | india   |
|      234 | ishant  | lucknow | india   |
|      246 | sumit   | lucknow | india   |
|     2334 | aman    | kanpur  | india   |
| 24234236 | ramsigh | lucknow | india   |
+----------+---------+---------+---------+
6 rows in set (0.00 sec)

mysql> select * from student limit 4;
+-----+--------+---------+---------+
| id  | name   | city    | country |
+-----+--------+---------+---------+
|  23 | ankit  | delhi   | ind     |
|  24 | sanket | lucknow | india   |
| 234 | ishant | lucknow | india   |
| 246 | sumit  | lucknow | india   |
+-----+--------+---------+---------+
4 rows in set (0.00 sec)

mysql> select * from student limit 2 2;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near '2' at line 1
mysql> select * from student limit 2 offset 2;          //offset used for leaver first 2 record.
+-----+--------+---------+---------+
| id  | name   | city    | country |
+-----+--------+---------+---------+
| 234 | ishant | lucknow | india   |
| 246 | sumit  | lucknow | india   |
+-----+--------+---------+---------+
2 rows in set (0.00 sec)

mysql> select * from student;
+----------+---------+---------+---------+
| id       | name    | city    | country |
+----------+---------+---------+---------+
|       23 | ankit   | delhi   | ind     |
|       24 | sanket  | lucknow | india   |
|      234 | ishant  | lucknow | india   |
|      246 | sumit   | lucknow | india   |
|     2334 | aman    | kanpur  | india   |
| 24234236 | ramsigh | lucknow | india   |
+----------+---------+---------+---------+
6 rows in set (0.00 sec)

mysql> select * from student order by id;
+----------+---------+---------+---------+
| id       | name    | city    | country |
+----------+---------+---------+---------+
|       23 | ankit   | delhi   | ind     |
|       24 | sanket  | lucknow | india   |
|      234 | ishant  | lucknow | india   |
|      246 | sumit   | lucknow | india   |
|     2334 | aman    | kanpur  | india   |
| 24234236 | ramsigh | lucknow | india   |
+----------+---------+---------+---------+
6 rows in set (0.00 sec)

mysql> select * from student order by id desc;
+----------+---------+---------+---------+
| id       | name    | city    | country |
+----------+---------+---------+---------+
| 24234236 | ramsigh | lucknow | india   |
|     2334 | aman    | kanpur  | india   |
|      246 | sumit   | lucknow | india   |
|      234 | ishant  | lucknow | india   |
|       24 | sanket  | lucknow | india   |
|       23 | ankit   | delhi   | ind     |
+----------+---------+---------+---------+
6 rows in set (0.00 sec)

mysql> select * from student order by name desc;
+----------+---------+---------+---------+
| id       | name    | city    | country |
+----------+---------+---------+---------+
|      246 | sumit   | lucknow | india   |
|       24 | sanket  | lucknow | india   |
| 24234236 | ramsigh | lucknow | india   |
|      234 | ishant  | lucknow | india   |
|       23 | ankit   | delhi   | ind     |
|     2334 | aman    | kanpur  | india   |
+----------+---------+---------+---------+
6 rows in set (0.00 sec)

mysql> select * from student order by name asc;
+----------+---------+---------+---------+
| id       | name    | city    | country |
+----------+---------+---------+---------+
|     2334 | aman    | kanpur  | india   |
|       23 | ankit   | delhi   | ind     |
|      234 | ishant  | lucknow | india   |
| 24234236 | ramsigh | lucknow | india   |
|       24 | sanket  | lucknow | india   |
|      246 | sumit   | lucknow | india   |
+----------+---------+---------+---------+
6 rows in set (0.00 sec)

mysql> select * from student order by name;
+----------+---------+---------+---------+
| id       | name    | city    | country |
+----------+---------+---------+---------+
|     2334 | aman    | kanpur  | india   |
|       23 | ankit   | delhi   | ind     |
|      234 | ishant  | lucknow | india   |
| 24234236 | ramsigh | lucknow | india   |
|       24 | sanket  | lucknow | india   |
|      246 | sumit   | lucknow | india   |
+----------+---------+---------+---------+
6 rows in set (0.00 sec)

mysql> select * from student;
+----------+---------+---------+---------+
| id       | name    | city    | country |
+----------+---------+---------+---------+
|       23 | ankit   | delhi   | ind     |
|       24 | sanket  | lucknow | india   |
|      234 | ishant  | lucknow | india   |
|      246 | sumit   | lucknow | india   |
|     2334 | aman    | kanpur  | india   |
| 24234236 | ramsigh | lucknow | india   |
+----------+---------+---------+---------+
6 rows in set (0.00 sec)

mysql> select * from student order by id desc limit 2;
+----------+---------+---------+---------+
| id       | name    | city    | country |
+----------+---------+---------+---------+
| 24234236 | ramsigh | lucknow | india   |
|     2334 | aman    | kanpur  | india   |
+----------+---------+---------+---------+
2 rows in set (0.00 sec)

mysql> update student set name='ram singh' where id=24234236;
Query OK, 1 row affected (0.02 sec)
Rows matched: 1  Changed: 1  Warnings: 0

mysql> select * from student;
+----------+-----------+---------+---------+
| id       | name      | city    | country |
+----------+-----------+---------+---------+
|       23 | ankit     | delhi   | ind     |
|       24 | sanket    | lucknow | india   |
|      234 | ishant    | lucknow | india   |
|      246 | sumit     | lucknow | india   |
|     2334 | aman      | kanpur  | india   |
| 24234236 | ram singh | lucknow | india   |
+----------+-----------+---------+---------+
6 rows in set (0.00 sec)

mysql> select * from student;
+----------+-----------+---------+---------+
| id       | name      | city    | country |
+----------+-----------+---------+---------+
|       23 | ankit     | delhi   | ind     |
|       24 | sanket    | lucknow | india   |
|      234 | ishant    | lucknow | india   |
|      246 | sumit     | lucknow | india   |
|     2334 | aman      | kanpur  | india   |
| 24234236 | ram singh | lucknow | india   |
+----------+-----------+---------+---------+
6 rows in set (0.00 sec)

Note:
    * : for evrything.
    % : one or more character.
    _ : single chracter.
    



mysql> select * from student where name like 'a%';
+------+-------+--------+---------+
| id   | name  | city   | country |
+------+-------+--------+---------+
|   23 | ankit | delhi  | ind     |
| 2334 | aman  | kanpur | india   |
+------+-------+--------+---------+
2 rows in set (0.00 sec)

mysql> select * from student where city like "_u%";
+----------+-----------+---------+---------+
| id       | name      | city    | country |
+----------+-----------+---------+---------+
|       24 | sanket    | lucknow | india   |
|      234 | ishant    | lucknow | india   |
|      246 | sumit     | lucknow | india   |
| 24234236 | ram singh | lucknow | india   |
+----------+-----------+---------+---------+
4 rows in set (0.00 sec)

mysql> select * from student where city like "%o_";
+----------+-----------+---------+---------+
| id       | name      | city    | country |
+----------+-----------+---------+---------+
|       24 | sanket    | lucknow | india   |
|      234 | ishant    | lucknow | india   |
|      246 | sumit     | lucknow | india   |
| 24234236 | ram singh | lucknow | india   |
+----------+-----------+---------+---------+
4 rows in set (0.00 sec)

mysql> select * from student;
+----------+-----------+---------+---------+
| id       | name      | city    | country |
+----------+-----------+---------+---------+
|       23 | ankit     | delhi   | ind     |
|       24 | sanket    | lucknow | india   |
|      234 | ishant    | lucknow | india   |
|      246 | sumit     | lucknow | india   |
|     2334 | aman      | kanpur  | india   |
| 24234236 | ram singh | lucknow | india   |
+----------+-----------+---------+---------+
6 rows in set (0.00 sec)

mysql> select SUM(id) from student;
+----------+
| SUM(id)  |
+----------+
| 24237097 |
+----------+
1 row in set (0.00 sec)

mysql> select SUM(id) as "Total Salary" from student;
+--------------+
| Total Salary |
+--------------+
|     24237097 |
+--------------+
1 row in set (0.00 sec)

mysql> select AVG(id) from student;
+--------------+
| AVG(id)      |
+--------------+
| 4039516.1667 |
+--------------+
1 row in set (0.00 sec)

mysql> select COUNT(id) from student;
+-----------+
| COUNT(id) |
+-----------+
|         6 |
+-----------+
1 row in set (0.00 sec)

mysql> select MIN(id) from student;
+---------+
| MIN(id) |
+---------+
|      23 |
+---------+
1 row in set (0.00 sec)




mysql> select name from student where id = (select MIN(id) from student) ;
+-------+
| name  |
+-------+
| ankit |
+-------+
1 row in set (0.00 sec)

mysql> select name from student where id = (select MAX(id) from student) ;
+-----------+
| name      |
+-----------+
| ram singh |
+-----------+
1 row in set (0.00 sec)

mysql> show tables;
+-----------------+
| Tables_in_learn |
+-----------------+
| student         |
+-----------------+
1 row in set (0.00 sec)

mysql> select * from student;
+----------+-----------+---------+---------+
| id       | name      | city    | country |
+----------+-----------+---------+---------+
|       23 | ankit     | delhi   | ind     |
|       24 | sanket    | lucknow | india   |
|      234 | ishant    | lucknow | india   |
|      246 | sumit     | lucknow | india   |
|     2334 | aman      | kanpur  | india   |
| 24234236 | ram singh | lucknow | india   |
+----------+-----------+---------+---------+
6 rows in set (0.00 sec)

mysql> create table laptops(lid int primary key, lmodel varchar(200), studentId int , foreign key(studentId) references student(id));
Query OK, 0 rows affected (0.09 sec)

mysql> show tables;
+-----------------+
| Tables_in_learn |
+-----------------+
| laptops         |
| student         |
+-----------------+
2 rows in set (0.00 sec)

mysql> desc student;
+---------+--------------+------+-----+---------+-------+
| Field   | Type         | Null | Key | Default | Extra |
+---------+--------------+------+-----+---------+-------+
| id      | int          | NO   | PRI | NULL    |       |
| name    | varchar(100) | NO   |     | NULL    |       |
| city    | varchar(50)  | YES  |     | NULL    |       |
| country | varchar(50)  | YES  |     | NULL    |       |
+---------+--------------+------+-----+---------+-------+
4 rows in set (0.00 sec)

mysql> desc laptops;
+-----------+--------------+------+-----+---------+-------+
| Field     | Type         | Null | Key | Default | Extra |
+-----------+--------------+------+-----+---------+-------+
| lid       | int          | NO   | PRI | NULL    |       |
| lmodel    | varchar(200) | YES  |     | NULL    |       |
| studentId | int          | YES  | MUL | NULL    |       |
+-----------+--------------+------+-----+---------+-------+
3 rows in set (0.00 sec)

mysql> insert into laptops values(13414,'HP',96418565);
ERROR 1452 (23000): Cannot add or update a child row: a foreign key constraint fails (`learn`.`laptops`, CONSTRAINT `laptops_ibfk_1` FOREIGN KEY (`studentId`) REFERENCES `student` (`id`))



mysql> insert into laptops values(13414,'HP',23);
Query OK, 1 row affected (0.00 sec)

mysql> select * from laptops;
+-------+--------+-----------+
| lid   | lmodel | studentId |
+-------+--------+-----------+
| 13414 | HP     |        23 |
+-------+--------+-----------+
1 row in set (0.00 sec)




mysql> insert into laptops values(13414,'Dell',24);
ERROR 1062 (23000): Duplicate entry '13414' for key 'laptops.PRIMARY'


mysql> insert into laptops values(134132454,'Dell',24);
Query OK, 1 row affected (0.00 sec)

mysql> select * from laptops;
+-----------+--------+-----------+
| lid       | lmodel | studentId |
+-----------+--------+-----------+
|     13414 | HP     |        23 |
| 134132454 | Dell   |        24 |
+-----------+--------+-----------+
2 rows in set (0.00 sec)

mysql> select * from student;
+----------+-----------+---------+---------+
| id       | name      | city    | country |
+----------+-----------+---------+---------+
|       23 | ankit     | delhi   | ind     |
|       24 | sanket    | lucknow | india   |
|      234 | ishant    | lucknow | india   |
|      246 | sumit     | lucknow | india   |
|     2334 | aman      | kanpur  | india   |
| 24234236 | ram singh | lucknow | india   |
+----------+-----------+---------+---------+
6 rows in set (0.00 sec)




mysql> select student.name,student.city , laptops.lmodel from student , laptops where student.id=laptops.studentId;
+--------+---------+--------+
| name   | city    | lmodel |
+--------+---------+--------+
| ankit  | delhi   | HP     |
| sanket | lucknow | Dell   |
+--------+---------+--------+
2 rows in set (0.00 sec)




mysql> select student.name,student.city , laptops.lmodel from student , laptops where student.id=laptops.studentId and student.name='Ankit';
+-------+-------+--------+
| name  | city  | lmodel |
+-------+-------+--------+
| ankit | delhi | HP     |
+-------+-------+--------+
1 row in set (0.00 sec)




mysql> select student.name , laptops.lmodel from student inner join laptops on student.id=laptops.studentId;
+--------+--------+
| name   | lmodel |
+--------+--------+
| ankit  | HP     |
| sanket | Dell   |
+--------+--------+
2 rows in set (0.00 sec)






---------------- Primary key and Foreign key in sql*********
Primary key:
The primary key constraint uniquely identifies each record in a table. primary keys
must constain UNIQUE values, and cannot contain NULL values.
    syntax:
        create table table_name(
            stud_id int not null,
            name varchar(55),
            age int,
            primary key(stud_id)        //assign primary key to id.
        );


Foreign key:
A foreign key is a key used to link two tables together. A foreign key is a field( or collection
of fields) in one table that referes to the PRIMARY key in another table.

Example:
    create table customers(cid int not null auto_increment primary key,
                            cname varchar(55),
                            cemail varchar(100)
                            );
    create table orders(oid int not null auto_increment primary key,
                        orderdate date,
                        cid int,
                        foreign key(cid) references customers(cid)
                        );

insert data:
    insert into customers(cid,cname,email) values(1,"Sheeshpal","sheeshpal@gmail.com"),
                                            (2,"Sheesh","sheesh@gmial.com"),
                                            (3,"Singh","singh@gmail.com");

    insert into orders (oid,orderdate,oamount,cid) values(1,"2019/05/05",55,1),
                                                    (2,"2019/08/06",85,2),
                                                    (3,"2019/08/05",155,1),
                                                    (4,"2019/05/12",95,3);


    select * from customers, orders;



---------------------sql joins--------------------
A join is used to combine rows from two or more tables, based on a related column between them.
 

    Different types of SQL joins:

    1. (inner) join: return records that have matching values in both tables.
    2. left(outer) join: returns all records from the left table, and the matched records
                         from the right table.
    3. right(outer) join: Returns all records from the right table, and the matched records from 
                          the left table.


    1. Inner Join:

        without join:
            select * from customers, orders where customers.cid = orders.cid order by orderdate;

        with join:
            select cname,cemail,orderdate from customers inner join orders on customers.cid=orders.cid;

            select * from customers join orders on customers.cid=orders.cid;
            [customers.cid=orders.cid->joining part]

            if Column 'cid' in field list is ambiguous-> show error 
            for that used customers.cid & orders.cid they are in differet table.



    2. Left sql join:
        return all records from the left table and the matched records from the right table.
        the result is null from the right side, if there is no match.

        Example:
            select column_name from table1 left join table2 on table1.coulumn_name=table2.column_name.

            select customers.cid,cname,oamount
            from customers
            left join orders
            on customers.cid=orders.cid;




    3. Right sql:
        returns all records from the left table and the matched records from the right table
        the result is null from the right side, if there is no match.

        Example:
            select column_name from table1 right join table2 
            on table1.column_name = table2.column_name;

            select cname,email,orderdate from customers right join orders 
            on customers.cid=orders.cid;
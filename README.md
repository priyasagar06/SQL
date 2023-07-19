<h1> SQL </h1>

<h3> Bulk upload of data </h3><br>

```
LOAD DATA INFILE  
'file path'
into table table_name
FIELDS TERMINATED by ','
ENCLOSED by '"'
lines terminated by '\n'
IGNORE 1 ROWS;
```
<h3>Auto incerement in primary key</h3><br>

```
create table if not exists test ( 
test_id int not null auto_increment,
test_name varchar(30), 
test_mailid varchar(30),
test_adress varchar(30),
primary key (test_id))
```
<h3>Insert Values in above created table</h3><br>

```
insert into test (tast_name, test_mailid, test_adress) 
values ('x','x@gmail.com','Mumbai'),
('y','y@gmail.com', 'Pune')
```
<h3>Check constraint on create table</h3><br>

```
create table if not exists test2( 
test_id int not null,
test_name varchar(30), 
test_mailid varchar(30),
test_adress varchar(30),
test_salary int check(test_salary > 10000))
```
Check constraint will always check the condition before insertion of any record.<br>
If salary > 10000, then only the record will be added in the table, else it will give an error.<br>



















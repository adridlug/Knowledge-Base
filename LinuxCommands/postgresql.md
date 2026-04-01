# Install and start postgres
## install postgress
```
apt-get install -y postgresql postgresql-contrib
```
## check psql version
```
psql --version
```
## start service
```
service postgresql start
```
## switch to postgres user   
```
su - postgres
```
## start postgres client
```
psql
```
# Usage
## switch to db user
```
sudo -i -u postgres
```

## Access DB Shell

```sh
psql
```

## List Databases

```sql
\l
```

## Create Database

```sql
CREATE DATABASE $dbname;
```

## Drop Database

```sql
DROP DATABASE $dbname;
```

## Create DB User

```sql
CREATE USER $username WITH PASSWORD '$pw';
```

## Grant Privileges to User

```sql
GRANT ALL PRIVILEGES ON DATABASE $dbname TO $username;
```

## Connect to Database

```sql
\c $dbname
```

## Create Table

```sql
CREATE TABLE employees (
   id SERIAL PRIMARY KEY,
   name VARCHAR(100),
   position VARCHAR(100),
   salary NUMERIC
);
```

## Create Table with Default Values

```sql
CREATE TABLE employees (
   id serial primary key,
   name text,
   price integer default -1,
   alias text
);
```

## Create Table with Foreign Key

```sql
CREATE TABLE tests (
   subject_id SERIAL,
   subject_name text,
   highestStudent_id integer REFERENCES students (student_id)
);
```
## create table with integer max value
```
CREATE TABLE flat_10
(
  pk_flat_id bigint DEFAULT 1,
  rooms      integer NOT NULL,
  room_label CHAR(1) NOT NULL,

  PRIMARY KEY (flat_id), 
  constraint valid_number 
      check (pk_flat_id <= 999999999)
);
```

## example with foreign key, constraints, default values and different types
```
create table employees (id serial primary key, boss_id integer references boss(id), col1 VARCHAR(20), col2 integer default 0, col2 integer default 0, flag boolean default false, flag1 boolean default false, constraint max_col1 check(col1 <= 65535 ), constraint min_col1 check(col1 >= 0), constraint min_col2 check(col2 >= 0));
```
## list users
```
\du
\du+
```
## list tables
```
\dt
```
## show table infos 
```
\d $tablename
```
## insert into table
```
INSERT INTO $tablename ($column1, $column2) VALUES ('value1', 'value2');
```
## grant select privileges to user
```
\c $dbname
GRANT SELECT ON TABLE $table TO $user; 
```
## grant insert privileges to user
```
GRANT INSERT ON TABLE $table to $user;
GRANT USAGE, SELECT ON SEQUENCE $table_id_seq TO $dbuser;
```
## update table
```
UPDATE $table
SET $column1 = $value1,
    $column2 = $value2,
    ...
WHERE $condition;
```
## 
```
```
## 
```
```
## 
```
```
## 
```
```
## 
```
```
## 
```
```
## 
```
```
## 
```
```
## 
```
```
## 
```
```
## 
```
```

# MySQL Basic Command

> We can use tab to completion command in MySQL.

Connect to MySQL.

```shell
mysql -uroot -p
```

Show all databases.

```mysql
show databases;
```

Change/Select database.

```mysql
use ${database name};
```

Show all tables;

```mysql
show tables;
```

Show table structure.

```mysql
show create table ${table name};
```

## Transaction

Show mysql transaction isolation level.

```MySQL
select @@global.transaction_isolation;

select @@session.transaction_isolation;
```

Start transaction in mysql CLI.

```mysql
start transaction;
select * from table where xxx;
update table set yyy where xxx;
commit/rollback;
```

Change mysql transaction isolation level:

```mysql
SET SESSION TRANSACTION ISOLATION LEVEL READ UNCOMMITTED;

SET SESSION TRANSACTION ISOLATION LEVEL READ COMMITTED;

SET SESSION TRANSACTION ISOLATION LEVEL REPEATABLE READ;

SET SESSION TRANSACTION ISOLATION LEVEL SERIALIZABLE;
```

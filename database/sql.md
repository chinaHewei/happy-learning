# SQL #

## 基本类型 ##

* char(n): **固定长度**的字符串，n 为长度
* varchar(n): **可变长度**的字符串。n 为长度
* int: 整数类型
* smallint: 小整数类型
* numeric(p, d): 定点数，精度由用户指定。这个数有 p 位数字（加上符号位），其中 d
  位数字在小数点右边。`numeric(3,1)` 可精确存储 `44.5`
* real, double percision: 浮点数与双精度浮点数
* float(n): 精度至少为 n 位的浮点数

## 初级 SQL ##

### 基本模式定义 ###

#### 创建表 ####

> create table r<br>
> (<br>
>  A1    D1,<br>
>  A2    D2,<br>
>  A3    D3,<br>
>  <完整性约束>,<br>
>  <完整性约束><br>
> );<br>

```sql
create table department
(
  dept_name varchar(20),
  building  varchar(15),
  budget    numeric(12, 2),
  primary key (dept_name)
);
```

#### 修改表 ####

> alter table r add A D;

```sql
alter table department add alias varchar(20);
```

#### 插入数据 ####

```sql
insert into department values ('name', 'building', 100.23, 'alias');
```

#### 删除数据 ####

> delete from r;

```sql
delete from department;
```

#### 删除表 ####

> drop table r;

```sql
drop table department;
```

### 基本查询 ###

关系就是表的意思。

#### 单关系查询 ####

```sql
select * from department;
```

```sql
select dept_name from department;
```

`distinct` 关键字可对查询出来的行去重。

```sql
select distinct dept_name from department;
```

```sql
select * from department where dept_name = '' and building = '';
```

#### 多关系查询 ####

## 中级 SQL ##

## 高级 SQL ##


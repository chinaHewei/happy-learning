#  SQL 基础 #

## 基本类型 ##

* char(n): **固定长度**的字符串，n 为长度
* varchar(n): **可变长度**的字符串。n 为长度
* int: 整数类型
* smallint: 小整数类型
* numeric(p, d): 定点数，精度由用户指定。这个数有 p 位数字（加上符号位），其中 d
  位数字在小数点右边。`numeric(3,1)` 可精确存储 `44.5`
* real, double percision: 浮点数与双精度浮点数
* float(n): 精度至少为 n 位的浮点数

## 创建表 ##

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

## 修改表 ##

> alter table r add A D;

```sql
alter table department add alias varchar(20);
```

## 插入数据 ##

```sql
insert into department values ('name', 'building', 100.23, 'alias');
```

## 删除数据 ##

> delete from r;

```sql
delete from department;
```

## 删除表 ##

> drop table r;

```sql
drop table department;
```

## 单关系查询 ##

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

## 多关系查询 ##

> select A1, A2, A3, ..., An<br>
> from r1, r2, r3, ..., rn<br>
> where<br>

如何理解查询所代表的运算呢？**首先为 from，然后是 where，最后是 select**

```sql
select * from department, user;
```

首先 from 出来的结果是怎么样的呢？其实是两个关系的**笛卡尔积**，可以这么理解：

```txt
for each 元祖t1 in 关系r1
  for each 元祖t2 in 关系r2
    ...
      for each 元祖tn in 关系rn
        把t1, t2, ..., tn 链接成单个元祖 t
        把 t 加入到结果关系中
```

对于 department 和 user 表的笛卡尔积的关系模式为：

```txt
(department.dept_name, department_building, department.alias, user.id, user.name, user.alias)
```

然后在 from 出来的结果上按照 where 的条件筛选符合的元祖。**where** 子句中的谓词
是用来限制笛卡尔积所建立的组合，只留下哪些对所需答案有意义的组合。

## 对查询出来的结果进行操作 ##

### 排序操作 ###

> order by A asc/desc

* asc: 升序（默认）
* desc: 降序

```sql
select * from user order by name asc;
select * from user order by name asc, id desc;
```

### 去重操作 ###

> distinct A

```sql
select distinct dept_name from department;
```

# 一、MySQL

#### 1.1 数据库介绍

- 数据库概念

- 术语介绍

#### 1.2 MySQL数据库安装配置

- 下载、安装、配置、卸载
- MySQL客户端工具安装及使用

#### 1.3 SQL 结构化查询语言

- 什么是SQL
- SQL操作数据库（CRUD操作：添加、查询、修改、删除）

#### 1.4 SQL 高级

- 存储过程
- 索引
- 触发器、视图

#### 1.5 数据库设计

- 数据库设计步骤
- 数据库设计范式
- E-R图
- PowerDesigner建模工具、PDMan

#### 1.6 数据库事务

- 什么是事务
- 事务特性ACID
- 事务隔离级别
- 事务管理

# 二、数据库介绍

#### 2.1 数据库概念

> 数据库（DateBase，简称DB）是长期存储在计算内部有结构、大量的、共享的数据集合

- 长期存储：持久存储

- 有结构

  - 类型：数据库不仅可以存放数据，而且存放的数据还是有类型的


  - 关系：存储数据与数据之间的关系

- 大量：大多数数据库都是文件系统的（关系型数据库），也就是说存储在数据库中的数据实际上就是存储在磁盘的文件中

- 共享：多个应用程序可以通过数据库实现数据的共享																																																												

#### 2.2 关系型数据库与非关系型数据库

- 关系型数据库

  > 关系型数据库，采用了关系模型来组织数据的存储，以行和列的形式存储数据并记录数据与数据之间的关系 —— 将数据存储在表格中，可以通过建立表格与表格之间的关联来维护数据与数据的关系。	

- 非关系型数据库

  > 非关系型数据库，采用键值对的模型存储数据结构，只完成对数据的记录，不会记录数据与数据的关系。在非关系型数据库中基于其特定的存储结构来解决一些大数据应用的难题，非关系型数据库也叫NoSQL（No only SQL）数据库	

#### 2.3 常见的数据库产品

###### 关系型数据库产品

- `MySQL`（免费开源）
  - MariaDB
  
  - Percona Server
  
- PostgreSQL

- `Oracle` 收费

- SQL Server

- Access

- Sybase

- 达梦数据库

###### 非关系型数据库

- 面向检索列式存储 Column--Oriented
  - HaBase（Hadoop）
  - BigTable（Google）

- 面向高并发的缓存存储 Key-Value
  - `Redis`
  - MemcacheDB

- 面向海量数据访问的文档存储 Document-Oriented
  - `MongoDB`
  - CouchDB

#### 2.4 数据库术语

- `数据库（DataBase）`：存储的数据的集合，提供数据存储的服务
- `数据（Data）`：实际上指描述事物的符号记录
- `数据库管理系统（DataBase Management System，DBMS）`：数据管理系统是位于用户和操作系统之间的一层数据管理软件数据库
- `数据库系统管理员（DataBase System Administrator，DBA）`：负责数据库创建、使用及维护的专门人员
- `数据库系统（DataBase System，DBS）`：数据库系统管理员、数据库管理系统及数据库组成的整个单元

# 三、MySQL数据库环境准备

> MySQL下载、安装、配置、卸载、安装DBMS、使用DBMS

#### 3.1 数据库版本及下载

###### 3.1.1 版本

- MySQL 是Oracle的免费的关系型数据库，官网：https://www.mysql.com/

- MySQL 目前的最新版本为 8.0.28，在企业项目中主流版本：5.0 --- 5.5 --- 5.6 --- 5.7 --- 8.0.28

  - 5.x  ---  2020年 5.7.32

  - 8.x  ---  2018年 8.0.11  ---  2019年 8.0.16  ---  2021年 8.0.26 

- MySQL 8.x新特性

  - 性能：官方8.x比5.7速度要快2倍

  - 支持NoSQL存储：5.7版本开始提供NoSQL支持，8.0.x做了进一步改进
  - 窗口函数
  - 索引：隐藏索引、降序索引
  - 可用性、可靠性

###### 3.1.2 下载

- 官网下载：https://dev.mysql.com/downloads/installer/

- - 需要注册oracle账号
  - 服务器在国外，下载速度很慢

- 镜像下载：https://www.filehorse.com/download-mysql-64/download/

#### 3.2 MySQL安装

> ​	傻瓜式安装（直接安装下一步）

###### 3.2.1安装类型选择

![img](F:\App\YoudaoNote\qq2234AFC6AEC7CB2086CD3D92FD3F7547\ae896d2bef094a57b9d2cb44433d0066\clipboard.png)

**选择`Developer Default`模式安装**

此模式会安装开发人员需要的常用组件，在安装这些组件时需要对应的环境依赖，我们要暂停先去安装依赖的环境

例如：

![image-20220303231305985](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220303231305985.png)

**选择自定义`Custom`安装**

![image-20220303232441438](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220303232441438.png)

#### 3.3 数据库配置

###### 3.3.1 端口配置

- MySQL的默认端口时3306

![image-20220303235246226](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220303235246226.png)

###### 3.3.2 账号密码配置

账号：root	密码：root

![image-20220303235557146](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220303235557146.png)

###### 3.3.2服务名称

![image-20220303235843949](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220303235843949.png)

![image-20220304000015203](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220304000015203.png)

#### 3.4 MySQL服务的启动与停止

> MySQL是以服务的形式运行在系统中

###### 3.4.1 计算机管理窗口

`此电脑` --- `打开服务`

![image-20220304001116157](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220304001116157.png)

###### 3.4.2 windows 命令行

以管理员身份打开命令行

```shell
net stop mysql80 ## 关闭mysql
net start mysql80 ## 开启mysql
```

#### 3.5 MySQL卸载

- 关闭服务

  ```shell
  ## 以管理员身份打开命令行
  net stop mysql80
  ```

- 卸载软件

  `打开控制面板` --- `程序与功能`  --- 删除全部mysql组件

- 删除目录

  - MySQL的安装目录：`C:\Program Files\MySQL`
  - MySQL的数据文件目录（默认隐藏）：`C:\ProgramData\MySQL`

- 删除注册表

  - 打开注册表 `HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Services\MySQL80`
  - 搜索MySQL相关项删除（`非必须`）



# 四、MySQL的管理工具

> 当完成数据库的安装之后，mysql是以服务的形式运行在windows/linux系统，用户通过DBMS工具来对MySQL进行操作，当我们安装完成MySQL之后默认安装了`mysql Commcand line Client`，此工具是一个命令行形式的工具，通常我们会单独安装可视化的DBMS工具：
>
> - SQLyog
> - Navicat for MySQL

#### 4.1 MySQL Command line Client使用

- 打开 `MySQL Command line Client`：开始菜单 --- MySQL --- MySQL 8.0 Command line Client

- 连接MySQL：`输入密码` 即可（如果密码错误或者mysql服务没有启动，窗口会闪退）

  ![image-20220304140851286](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220304140851286.png)

- 关闭 MySQL Command line Client：输入 `exit` 指令回车

#### 4.2 可视化工具Navicat使用

###### 4.2.1 Navicat下载及安装

> 傻瓜式安装

4.2.2 创建连接

- 打开navicat工具
- 创建连接：

<img src="C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220304152640851.png" alt="image-20220304152640851" style="zoom: 80%;" />



# 五、MySQL的逻辑结构

> MySQL可以存储数据，但是存储在MySQL中的数据需要按照特定的结果进行存储

#### 5.1 逻辑结构

![image-20220304161120597](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220304161120597.png)

#### 5.2 记录/元组

![image-20220304161418909](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220304161418909.png)

# 六、SQL

#### 6.1 SQL概述

> SQL（Structured Query language）结构化查询语言，用于存取、查询、更新数据以及管理关系型数据库

###### 6.1.1 SQL发展

- SQL实在1981年由IBM公司推出，一经推出基于其简洁的语法在数据库中得到广泛的应用，成为主流数据库的通用规范
- SQL由ANSI组织确定规范
- 在不同的数据库产品中遵守SQL的通用规范，但是也对SQL有一些不同的改进，形成了一些数据库专有指令
  - MySQL：limit
  - SQL Server：top
  - Oracle：rownum

###### 6.1.2 SQL的分类

> 根据SQL指令完成数据库操作的不同，可以将SQL指令分为四类：

- **DDL Data Definition Language 数据定义语言**
  - 用于完成对数据库对象（数据库、数据表、视图、索引等）的创建、删除和修改

- **DML Data Manipulation Language 数据操作/操纵语言**
  - 用于完成对数据库表中的数据的添加、删除、修改操作

- **DQL Data Query Language 数据查询语言**
  - 用于将数据表的数据查询出来

- **DCL Data Control Language 数据控制语言**
  - 用于完成事务管理等控制性操作



#### 6.2 SQL基本语法

> 在MySQL Command line Client 或者Navicat等工具中都可以编写SQL命令

- SQL指令不区分大小写
- 每条SQL表达式结束之后都以`;`结束
- SQL关键字之间以`空格`进行分隔
- SQL之间可以不限制换行（有空格的地方就可以换行）



#### 6.3  DDL 数据定义语言

###### 6.3.1 DDL-数据库操作

> 使用DDL语句可以创建数据库、查询数据库、修改数据库、删除数据库

**查询数据库**

```sql
## 显示当前mysql中的数据库列表
show databases;

## 显示指定名称的数据库创建的SQL指令
show create database <dbName>;
```

**创建数据库**

```sql
## 创建数据库 dbName是数据库名称
create database <dbName>;

## 创建数据库，指定名称数据库不存在时创建
create database if not exists <dbName>;

## 创建数据库，指定数据库字符集（数据库存储在数据中采用的编码格式 utf8、gbk）
create database <dbName> character set utf8;
```

**修改数据库**

```sql
## 修改数据库字符集
alter database <dbName> character set gbk;
```

**删除数据库**	删除数据库时会删除数据库中所有表和表中的数据

```sql
## 删除数据库
drop database <dbName>;

## 如果数据库存在则删除数据库
drop database if exists <dbName>;
```

**使用数据库**

```sql
## 使用数据库
use <dbName>;
```



###### 6.3.2 DDL-数据表操作

**创建数据表**

> 数据表实际上是一个二维的表格，一个表格是由多列组成，表格中的每一列称为数据表的字段

```sql
-- 创建students数据表，（字段名 数据类型 约束）
create table students(
	stu_num char(8) not null unique,
    stu_name varchar(20) not null,
    stu_gender char(2) not null,
    stu_age int not null,
    stu_tel char(11) not null,
    stu_qq varchar(13) unique
);
```

**查询数据表**

```sql
show tables;
```

**查询表结构**

```sql
desc <tablename>;
```

**删除数据表**

```sql
-- 删除数据表
drop table <tableName>;
-- 当数据表存在时删除数据表
drop table if exists <tableName>;
```

**修改数据表 **

```sql
-- 修改表名
alter table <tableName> rename to <newTbaleName>;

-- 数据表也是有字符集的，默认字符集和数据库一样
alter table <tableName> character set utf8;

-- 添加字段（列）
alter table <tableName> add <columnName> <type>;

-- 修改字段（列）和类型
alter table <tableName> change <oldColumnName> <newColumnName> <type>;

-- 只修改字段（列）类型
alter table <tableName> modify <columnName> <newType>;

-- 删除字段（列）
alter table <tableName> drop <columnName>;
```



#### 6.4 数据类型

> 数据类型，指的是数据表中的字段支持存放的数据的类型

######  6.4.1 数值类型

在mysql中有多种数据类型可以存放数值，不同的类型存放的数值的范围和形式是不同的

| 类型              | 内存空间大小 | 范围                                             | 说明                                                |
| ----------------- | ------------ | ------------------------------------------------ | --------------------------------------------------- |
| tinyint           | 1byte        | 有符号  -128 ~ 127<br>无符号  0 ~ 255            | 特小型整数                                          |
| smallint          | 2byte        | 有符号  32768 ~ 32767<br>无符号  0 ~ 65535       | 小型整数                                            |
| mediumint         | 3byte        | 有符号  -2^23^ ~ 2^23^ - 1<br/>无符号  0 ~ 2^24^ | 中型整数                                            |
| **`int/integer`** | 4byte        | 有符号  -2^23^ ~ 2^23^ - 1<br/>无符号  0 ~ 2^24^ | 整数                                                |
| **bigint**        | 8byte        | 有符号  -2^63^ ~ 2^63^ - 1<br/>无符号  0 ~ 2^64^ | 大型整数                                            |
| float             | 4byte        | 有符号  -2^23^ ~ 2^23^ - 1<br/>无符号  0 ~ 2^24^ | 单精度                                              |
| **double**        | 8byte        | 有符号  -2^63^ ~ 2^63^ - 1<br/>无符号  0 ~ 2^64^ | 双精度                                              |
| decimal           |              |                                                  | decimal(10,2)，<br>表示数值一共有10位，小数位有两位 |

```sql
create table students(
	stu_num tinyint
);
```



###### 6.4.2 字符串类型

> 存储字符串类型

| 类型         | 字符长度（Byte） | 说明                                                         |
| ------------ | ---------------- | ------------------------------------------------------------ |
| `char(n)`    | 0 ~ 255          | 定长字符串，最多可以存储255个字符；<br/>当指定字段范围为char(10)此列中的数据最长为10可字符，<br/>如果添加的数据少于10个，则补空格（‘\n0000’）至10个 |
| `varchar(n)` | 0 ~ 65535        | 可变长度字符串，此类型最大长度为65535                        |
| tinyblob     | 0 ~ 255          | 存储二进制字符串                                             |
| blob         | 0 ~ 65535        | 存储二进制字符串                                             |
| mediumblob   | 0 ~ 1677215      | 存储二进制字符串                                             |
| longblob     | 0 ~ 4294967295   | 存储二进制字符串                                             |
| tinytext     | 0 ~ 255          | 文本数据（字符串）                                           |
| text         | 0 ~ 65535        | 文本数据（字符串）                                           |
| mediumtext   | 0 ~ 1677215      | 文本数据（字符串）                                           |
| `longtext`   | 0 ~ 4294967295   | 文本数据（字符串）                                           |

###### 6.4.3 日期类型

> 在MySQL数据库中，我们可以使用字符串来存储时间，但是如果我们需要基于时间字段进行查询（查询在某个时间段内的数据）就不便于查询实现

| 类型      | 格式                | 说明                        |
| --------- | ------------------- | --------------------------- |
| date      | 2022-03-05          | 日期，只存储年月日          |
| time      | 11:12:12            | 时间，只存储时分秒          |
| year      | 2022                | 年份                        |
| datetime  | 2022-03-05 19:45:30 | 日期+时间，存储年月日时分秒 |
| timestamp | 20220305 194530     | 日期+时间（时间戳）         |



#### 6.5 字段约束

###### 6.5.1 约束介绍

> 在创建数据表的时候，指定的对数据表的列的数据限制性的要求（限制）

为什么要给表中的列添加约束呢？

- 保证数据的有效性
- 保证数据的完整性
- 保证数据的正确性

字段常见的约束有哪些呢？

- 非空约束（not null）：限制此列的值必须提供，不能为null
- 唯一约束（unique）：一列中的数据不能重复
- 主键约束（primary key）：非空+唯一，语义是数据表中一条数据的唯一标记
- 外键约束（foreign key）：建立不同表之间的关联关系

###### 6.5.2 非空约束

> 限制数据表中此列的值必须提供	

- 创建表：设置books表的book_name not null（非空）

```sql
create table books(
	book_isbn char(4),
	book_name varchar(30) not null,
	book_auther varchar(10)
);
```

- 添加数据

![image-20220305202112884](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220305202112884.png)

###### 6.5.3 唯一约束

> 在表中的多条数据，此列的值不能重复

- 创建表：设置图书表的book_isbn为unique

```sql
create table books(
	book_isbn char(4) unique,
	book_name varchar(30) not null,
	book_auther varchar(10)
);
```

- 添加数据

![image-20220305203251937](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220305203251937.png)

###### 6.5.4 主键约束

> 主键——就是数据表中记录的唯一标记，在一张表中只能有一个主键（主键可以是一个列，也可以是多个列的组合）
>
> 当一个字段声明为主键之后
>
> - 此字段数据不能为null
> - 此字段数据不能重复

创建表时添加主键约束

```sql
create table books(
	book_isbn char(4) primary key,
	book_name varchar(10) not null,
	book_auther varchar(6)
);
```

或者

```sql
create table books(
	book_isbn char(4),
	book_name varchar(10) not null,
    bool_auther varchar(6),
    primary key(book_isbn)
);
```

**删除数据表主键约束**

```sql
alter table <tableName> drop primary key;
```

**创建表之后添加主键约束**

```sql
alter table books modify book_isbn char(4) primary key;
```

###### 6.5.5 主键的自动增长

> 创建数据库的时候，如果表中数据没有合适的字段作为主键，通常会定义一个与数据无关的int类型字段（id字段）作为主键，设置主键`自动增长`，这样添加数据时就不需要提供主键的值

**定义主键自动增长**

- 定义int类型字段自动增长：`auto_increment`

```sql
create table types(
	id int primary key auto_increment,
    type_name varchar(20) not null,
    type_remark varchar(100)
);
```

注意：自动增长从1开始，每添加一条记录，主键（id字段）自动+1，当我某条记录删除之后在添加数据，自动增长的数据不会重复生成（自动增长只保证唯一性、不保证连续性）

###### 6.5.6 联合主键

> 联合主键——将数据表中的多列组合在一起设置为表的主键

![image-20220305223021866](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220305223021866.png)

定义联合主键

```sql
create table grades(
	stu_num char(8),
    course_id int,
    score int,
    primary key(stu_num.course_id)
);
```

注意：在实际项目中的数据库设计中，联合主键使用频率不高；当一张数据表中没有明确的字段可以作为主键时，我们通常额外添加一个id字段作为主键

###### 6.5.7 外键约束



#### 6.6 DML 数据操控语言

> 用于完成对数据表的插入、删除、修改操作

```sql
## 创建students数据表，（字段名 数据类型 约束）
create table students(
	stu_num char(8) primary key,
    stu_name varchar(20) not null,
    stu_gender char(2) not null,
    stu_age int not null,
    stu_tel char(11) not null,
    stu_qq varchar(13) unique
);
```



###### 6.6.1 插入数据

**语法**

```sql
insert into <tableName>(columnName1,columnName2....) values(value1,value2....); 
```

**示例**

```sql
## 像数据表中指定的列添加数据（不允许为空的列必须提供数据）
insert into stus(stu_num,stu_name, stu_gender, stu_age, stu_tel, stu_qq) 
values('20220101', 'kobe', '男', 18,  '10086', '123456');

## SQL中的字段名列表顺序可以与表中的不一致，但是values中的值要跟字段列表对应
insert into stus(stu_num, stu_name,stu_age, stu_tel, stu_gender)
values('20200105', 'zhangsan', 22, '123123', '男');

## 当要向全部字段添加数据时，数据表后面的字段列表可以省略，但是values中的值要和表结构的字段保持一致
insert into stus values('20200106', 'lisi', '男', 21, '123123','123123');

## 注意，在项目开发中，为了保持SQL的可读性和稳定性，即使要向所有列添加数据，也建议把所有字段名写出来
insert into stus(stu_num,stu_name, stu_gender, stu_age, stu_tel, stu_qq) values('20200106', 'lisi', '男', 18, '123123','123123');
```

###### 6.6.2 删除数据

> 从数据表中删除满足特定条件或者所有的记录

**语法**

```sql
delete from <tbaleName> [where conditions];
```

**实例**

```sql
## 删除学号为20200102的学生信息
delete from stus where stu_num='20220102';

## 删除年龄年龄大于20的学生(满足where的记录有多条，则删除多条)
delete from stus where stu_age>20;

## 如果没有where子句或者where子句总是为真（where 1=1），则删除表中所有记录
delete from stus
delete from stus where 1=1;
```

###### 6.6.3 修改数据

> 对数据表中已经添加的记录进行修改

**语法**

```sql
update <tableName> set columnName=value [where=conditions]
```

**实例**

```sql
## 将学号为20200109的学生姓名修改为zhong（只修改一列）
update stus set stu_name='zhong' where stu_num='20200109';

##将学号为20200109的学生姓名修改为zhongbf，年龄修改28（修改多列）
update stus set stu_name='zhongbf',stu_age=28 where stu_num='20200109';

##如果update语句没有where子句，将修改当前表中所有记录（行）
update stus set stu_name='zhongbf',stu_age=28;
```



#### 6.7 DQL 数据查询语言

> 从数据库中提取满足条件的记录
>
> - 单表查询
> - 多表联合查询

###### 6.7.1 查询基础语法

```sql
select columnName1[,coumnName2,columnName3....] from <tableName>;
## 如果要查询全部列，可以用 * 代替字段名列表（在项目开发中不建议使用*）
select * from <tableName>;
```

###### 6.7.2 where子句

> 在删除、修改及查询的语句后都可以添加where子句，用于筛选满足特定条件的删除、修改及查询

```sql
delete from <tableName> where conditions;
update <tableName> set ... where conditions;
select ... from <tableName> where conditions;
```

**条件关系运算符**

```sql
## = 等于
select * from stus where stu_num='20200109';

## !=或者<> 不等于
select * from stus where stu_num!='20200109';

## > 大于
select * from stus where stu_age>20;

## < 小于
select * from stus where stu_num<20;

## >= 大于等于
select * from stus where stu_age>=20;

## <=小于等于
select * from stus where stu_age<=20;

## between and 区间查询 between v1 and v2(包括v1和v2)[v1,v2]
select * from stus where stu_age between 18 and 20;
```

**条件逻辑运算符**

> 在where子句中，可以将多个条件通过逻辑预算（and or not）进行运算，通过多个条件来筛选要操作的数据

```sql
## and 并且 筛选多个条件同时满足的记录
select * from stus where stu_age=28 and stu_name='kobe';

## or 或 筛选多个条件中至少满足一个条件的记录
select * from stus where stu_age=28 or stu_name='kobe';

## not 非
select * from stus where stu_age  not between 18 and 20;
```

###### 6.7.3 LIKE 子句

>在where子句的条件中，我们可以使用like关键字来实现模糊查询

**语法**

```sql
select * from <tableName> where columnName like 'reg';
```

- 在like关键字后的reg表达式中
  - `%`表示任意多个字符【`%o%` 包含字母o】
  - _ 表示任意一个字符 【_o% 第二个字母为o】

**实例**

```sql
# 查询学生姓名包含字母o的学生信息
select * from stus where stu_name like '%o%';

# 查询学生姓名第一个字为'张'的学生信息
select * from stus where stu_name like '张%';

# 查询学生姓名最后一个字母为o的学生信息
select * from stus where stu_name like '%o';

# 查询学生姓名中第二个字母为o的学生信息
select * from stus where stu_name like '_o%';
```

###### 6.7.4 对查询结果的处理

**设置查询的列**

> 声明显示查询结果的指定列

```sql
select columnName1,columnName2.... from stus where stu_age>20;
```

**计算列**

> 对从数据表中查询的记录的列进行一定的运算之后显示出来

```sql
## 直接用字段名进行计算
select stu_name,2022-stu_age from stus;
+----------+--------------+
| stu_name | 2022-stu_age |
+----------+--------------+
| zhongbf  |         1994 |
| kobe     |         1994 |
| abc      |         2004 |
+----------+--------------+
```

**as 字段别名**

> 我们可以为查询结果的列名去一个具有语义的别名，`as`也可以省略

```sql
select stu_name,2022-stu_age as stu_birth_year  from stus;
+----------+----------------+
| stu_name | stu_birth_year |
+----------+----------------+
| zhongbf  |           1994 |
| kobe     |           1994 |
| abc      |           2004 |
+----------+----------------+
```

**distinct 消除重复行**

> 从查询的结果中将重复的记录消除 `distinct`

```sql
## 只能写在select后面，所以要把目标字段移到第一个
select distinct stu_age,stu_name from stus;
```

###### 6.7.5 order by 排序

> 将查询到满足条件的记录按照指列的值进行升序/降序排序

**语法**

```sql
select * from <tableName> where conditons order by columnName asc|desc;
```

- order by columnName 表示将查询结果按照指定的列排序
  - asc 按照指定的列升序（默认）
  - desc 按照指定的列降序

**实例**

```sql
# 单字段排序 按照字段stu_gender进行降序
select * from stus where stu_age>15 order by stu_gender desc; 
# 多字段排序：先满足第一个排序规则，当第一个排序的列的值相同时再按照第二个列的规则排序
select * from stus order by stu_gender desc,stu_age asc;
```

###### 6.7.6 聚合函数

> SQL中提供了一些可以对查询的记录的列进行计算的函数——聚合函数
>
> - count()	计算总数
> - max()      求最大值
> - min()       求最小值
> - sum()      求和
> - avg()        求平均值

- `count()` 统计函数，统计满足条件的指定字段值的个数（记录数）

  ```sql
  # 统计学生表中学生总数
  select count(*) from stus;
  +----------+
  | count(*) |
  +----------+
  |        3 |
  +----------+
  ```

- `max()` 计算最大值，查询满足条件的记录中指定列的最大值

  ```sql
  select max(stu_age) from stus;
  +--------------+
  | max(stu_age) |
  +--------------+
  |           28 |
  +--------------+
  ```

- `min() `计算最小值，查询满足条件的记录中指定列的最小值

  ```sql
  select min(stu_age) from stus;
  +--------------+
  | min(stu_age) |
  +--------------+
  |           18 |
  +--------------+
  ```

- `sum() `求和，查询满足条件的记录中指定列的总和

  ```sql
  select sum(stu_age) from stus;
  +--------------+
  | sum(stu_age) |
  +--------------+
  |           74 |
  +--------------+
  ```

- `avg()` 求平均值，查询满足条件的记录中指定列的平均值

  ```sql
  select avg(stu_age) from stus;
  +--------------+
  | avg(stu_age) |
  +--------------+
  |      24.6667 |
  +--------------+
  ```


###### 6.6.7 日期函数和字符串函数

**日期函数**

>  当我们向日期类型的列添加数据时，可以通过字符串类型赋值（格式必须时yyyy:MM:dd hh:mm:ss）
>
> 如果我们想要获取当前系统时间添加到日期类型的列，可以使用`now()`或`sysdate`

**实例**

```sql
# 通过字符串类型给日期类型的列赋值
insert into stus(stu_num,stu_name,stu_gender,stu_age,stu_tel,stu_qq,stu_enterence)
values('20221011','Kobe','男',18,'123123','123345','2022:03:05 15:35:30');

# 通过now()/sysdate()获取当前时间
insert into stus(stu_num,stu_name,stu_gender,stu_age,stu_tel,stu_qq,stu_enterence)
values('20221012','Kobe','男',18,'12323123','12312345',now());

# 通过now()和sysdate()获取当前时间
mysql> select now();
+---------------------+
| now()               |
+---------------------+
| 2022-03-06 15:47:13 |
+---------------------+
1 row in set (0.00 sec)
```



**字符串函数**

> 通过SQL指令对字符串进行处理

 **实例**

```sql
# concat(column1,column2) 字符串拼接
select concat(stu_name,'-',stu_gender) from stus;
+---------------------------------+
| concat(stu_name,'-',stu_gender) |
+---------------------------------+
| zhongbf-男                      |
| kobe-男                         |
| abc-女                          |
| Kobe-男                         |
| Kobe-男                         |
+---------------------------------+

# upper(column)将字段的值转换成大写
select upper(stu_name) from stus;
+-----------------+
| upper(stu_name) |
+-----------------+
| ZHONGBF         |
| KOBE            |
| ABC             |
| KOBE            |
| KOBE            |
+-----------------+

# lower(column) 将指定列的值转换成小写
mysql> select lower(stu_name) from stus;
+-----------------+
| lower(stu_name) |
+-----------------+
| zhongbf         |
| kobe            |
| abc             |
| kobe            |
| kobe            |
+-----------------+

# substring(column,start,length) 截取指定列的字符串
mysql> select stu_name,substring(stu_tel,2,3) from stus;
+----------+------------------------+
| stu_name | substring(stu_tel,2,3) |
+----------+------------------------+
| zhongbf  | 231                    |
| kobe     | 008                    |
| ABC      | 231                    |
| Kobe     | 231                    |
| Kobe     | 232                    |
+----------+------------------------+
```

###### 6.7.8 分组查询

> 分组——就是将数据表中的记录按照指定的类进行分组

**语法**

```sql
select 分组字段/聚合函数 
from 表名 
[where 条件] 
[group by 分组列名 having 条件]
[order by]
# 注意，having必须与分组一起使用
```

- `select` 分组使用 `*` 显示对查询结果进行分组之后，显示每组的第一条记录（通常这种显示时没意思的）
- `select` 后通常显示分组字段和聚合函数（对分组后的数据进行统计、求和、平均值）
- 语句执行顺序：①先根据where条件从数据库查询记录②group by对查询记录进行分组③执行having对分组后的数据进行筛选

**实例**

```sql
# 先对查询的学生信息按性别进行分组（分成了男、女两组），然后再分别统计每组学生的个数
select stu_gender,count(*) from stus group by stu_gender;
+------------+----------+
| stu_gender | count(*) |
+------------+----------+
| 男         |        4 |
| 女         |        1 |
+------------+----------+

#先对查询的学生信息按性别进行分组（分成了男、女两组），然后再分别统计每组学生的平均年龄
select stu_gender,avg(stu_age) from stus group by stu_gender;
+------------+--------------+
| stu_gender | avg(stu_age) |
+------------+--------------+
| 男         |      20.2500 |
| 女         |      28.0000 |
+------------+--------------+

# 先对学生按年龄进行分组，然后统计各组学生的数量，最后对结果按年龄排序
select stu_age,count(*) from stus group by stu_age order by stu_age asc;
+---------+----------+
| stu_age | count(*) |
+---------+----------+
|      17 |        1 |
|      18 |        2 |
|      28 |        2 |
+---------+----------+

# 按年龄分组，然后统计每组的认输，再筛选当前人数>1的组显示出来（分组后筛选）
select stu_gender,count(*) 
from stus 
group by stu_gender having count(*)>1 
order by stu_age asc;
+------------+----------+
| stu_gender | count(*) |
+------------+----------+
| 男         |        4 |
+------------+----------+
```

###### 6.7.9 分页查询

> 当数据表中的记录比较多的时候，如果一次性全部查询显示出来给用户，用户的可读性/体验性就不好，因此我们可以将这些数据分页展示

**语法**

```sql
 select ....
 from ....
 where ....
 limit param1,param2
```

- param1 int，表示获取查询结果中的第一条数据的索引（索引从0开始）
- param2 int，表示获取的查询记录的条数（如果剩下的数据条数少于param2，则返回剩下的所有数据）



**案例**

对数据表中的学生信息进行分页显示，总共有10条数据，每页显示3条

> 总记录数 count：10
>
> 每页显示 pageSize：3
>
> 总页数：pageCount = count%pageSize == 0 ？count / pageSize ： count / pageSize + 1

```sql
# 查询第一页
select * stus [where ....] limit 0,3;   (1-1)*3,3

# 查询第二页
select * stus [where ....] limit 3,3;	(2-1)*3,3

# 查询第三页
select * stus [where ....] limit 6,3;	(3-1)*3,3

# 查询第四页
select * stus [where ....] limit 9,3;	(4-1)*3,3

# 如果在一张数据表中国
# pageNum表示查询的页码
# pageSize表示每页显示的条数
# 通用分页语句如下
select * from <tableName> [where ....] limit (pageNum-1)*PageSize,PageSize;


```



# 七、数据表的关联关系

#### 7.1 关联关系介绍

> MySQL是一个关系型数据库，不仅可以存储数据，还可以维护数据与数据之间的关系——通过再数据表中添加字段建立外键约束

![](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220306225519768.png)

数据与数据之间的关联关系分为四种：

- 一对一关联
- 一对多关联
- 多对一关联
- 多对多关联

#### 7.2 一对一关联

> 人——身份证	一个人只有一个身份证，一个身份证只对应一个人
>
> 学生——学籍	一个学生只有一个学籍，一个学籍只能对应一个学生
>
> 用户——用户详请	一个用户只有一个详情、一个详情也只对应一个用户

**方案1：**主键关联——两张数据表中主键相同的数据为相互对应的数据

![image-20220306230313901](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220306230313901.png)

**方案2：**唯一外键——再任意一张表中添加一个字段与另一张表主键关联，并且将外键添加唯一约束

![image-20220306231714009](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220306231714009.png)

#### 7.3 一对多与多对一关联

> 班级——学生（一对多）一个班级有多个学生，一个学生只能属于一个班级
>
> 学生——班级（多对一）	
>
>
> 图书——图书分类
>
> 商品——商品分类

**方案：**在多的一方（n）添加一个外键，与另一张表（1）的主键关联

![image-20220306233047691](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220306233047691.png)

#### 7.4 多对多关联

> 学生——课程	一个学生可以选择多门课程，一门课程也可以由多个学生选择
>
> 会员——社团	一个会员可以参加多个社团，一个社团也可以招纳多个会员

**方案：**额外创建一张关系表来维护对对多关联——在关系表中定义两个外键，分别与两个数据表的主键关联

![image-20220306235143146](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220306235143146.png)



#### 7.5 外键约束

> 外键约束——将一个列添加外键约束与另一张表的主键（唯一列）进行关联之后，这个外键约束的列添加的数据必须要在关联的主键字段中存在

案例：学生表 与 班级表（在学生表加外键与班级表的主键关联）

1. 先创建班级表

   ```sql
   create table classes(
   	class_id int primary key auto_increment,
   	class_name varchar(20) not null unique,
   	class_remark varchar(255)
   );
   ```

2. 创建学生表

   ```sql
   # 【方式1】 在创建表的时候，定义cid字段，并添加外键约束
   # 由于cid字段要与classes表的class_id进行关联，因此cid字段类型要与class_id的字段类型一致
   create table students(
       stu_num char(4) primary key,
       stu_name varchar(10) not null,
       stu_gender char(2) not null,
       stu_age int not null,
       cid int,
       constraint FK_STUDENT_CLASSES foreign key(cid) references classes(class_id)
   );
   
   # 【方式二】先创建表，再添加外键约束
   create table students(
       stu_num char(4) primary key,
       stu_name varchar(10) not null,
       stu_gender char(2) not null,
       stu_age int not null,
       cid int,
   );
   # 在创建students后，在为cid添加外键约束
   alter table students add constraint FK_STUDENT_CLASSES foreign key(cid) references classes(class_id);
   
   # 删除外键约束
   alter table students drop foreign key FK_STUDENT_CLASSES;
   ```

3. 向班级表添加信息

   ```sql
   insert into classes(class_name,class_remark) values('Java1012','...');
   insert into classes(class_name,class_remark) values('Java1013','...');
   insert into classes(class_name,class_remark) values('Java1014','...');
   insert into classes(class_name,class_remark) values('Java1015','...');
   insert into classes(class_name,class_remark) values('Python1015','...');
   
   select * from classes;
   +----------+------------+--------------+
   | class_id | class_name | class_remark |
   +----------+------------+--------------+
   |        1 | Java1012   | ...          |
   |        2 | Java1013   | ...          |
   |        3 | Java1014   | ...          |
   |        4 | Java1015   | ...          |
   |        5 | Python1015 | ...          |
   +----------+------------+--------------+
   ```

4. 向学生表中添加学生信息

   ```sql
   insert into students(stu_num,stu_name,stu_gender,stu_age,cid)
   values('2020', '李四','男',18,4);
   
   # 添加学生表信息，学生表的外键cid必须是其关联的班级表主键class_id，
   insert into students(stu_num,stu_name,stu_gender,stu_age,cid)
   values('2020', '李四'，'男',18,6); 
   ```



#### 7.6 外键约束 — 级联

> 当学生表存在外键与班级表主键关联时，班级表的主键不能修改和删除，如下：

```sql
# 班级表
+----------+------------+--------------+
| class_id | class_name | class_remark |
+----------+------------+--------------+
|        1 | Java1012   | ...          |
|        2 | Java1013   | ...          |
|        3 | Java1014   | ...          |
|        4 | Java1015   | ...          |
|        5 | Python1015 | ...          |
+----------+------------+--------------+
# 学生表
+---------+----------+------------+---------+------+
| stu_num | stu_name | stu_gender | stu_age | cid  |
+---------+----------+------------+---------+------+
| 1020    | 科比     | 男         |      24 |    1 |
| 2020    | 李四     | 男         |      18 |    4 |
+---------+----------+------------+---------+------+
mysql> update classes set class_id=6 where class_name='Java1012'; # 修改报错
mysql> delete from classes where class_id=1; # 删除报错
```

> 如果一定要修改Java1012的班级id，该如何实现
>
> - 将关联Java1012班级的外键cid改为NULL
> - 再修改班级信息表中Java1012的主键class_id
> - 最后将外键重新关联Java1012的新主键

```sql
mysql> update students set cid=NULL where cid=1;
# 将关联Java1012班级的外键cid改为NULL
+---------+----------+------------+---------+------+
| stu_num | stu_name | stu_gender | stu_age | cid  |
+---------+----------+------------+---------+------+
| 1020    | 科比     | 男         |      24 | NULL |
| 2020    | 李四     | 男         |      18 |    4 |
+---------+----------+------------+---------+------+
# 再修改班级信息表中Java1012的主键class_id=6
+----------+------------+--------------+
| class_id | class_name | class_remark |
+----------+------------+--------------+
|        2 | Java1013   | ...          |
|        3 | Java1014   | ...          |
|        4 | Java1015   | ...          |
|        5 | Python1015 | ...          |
|        6 | Java1012   | ...          |
+----------+------------+--------------+
# 最后将外键重新关联Java1012的新主键
+---------+----------+------------+---------+------+
| stu_num | stu_name | stu_gender | stu_age | cid  |
+---------+----------+------------+---------+------+
| 1020    | 科比     | 男         |      24 |    6 |
| 2020    | 李四     | 男         |      18 |    4 |
+---------+----------+------------+---------+------+
```

**`使用级联操作可以实现关联表的同时修改和删除`**

1. 在添加外键时，设置**级联修改** 和 **级联删除**

   ```sql
   # 如果已经存在外键就删除
   alter table students drop foreign key FK_STUDENT_CLASSES;
   # 重新添加外键，并设置联级修改和删除
   alter table students add constraint FK_STUDENTS_CLASSES foreign key(cid) references classes(class_id) ON UPDATE CASCADE ON DELETE CASCADE;
   ```

2. 测试联级修改

   ```sql
   # 班级表
   +----------+------------+--------------+
   | class_id | class_name | class_remark |
   +----------+------------+--------------+
   |        2 | Java1013   | ...          |
   |        3 | Java1014   | ...          |
   |        4 | Java1015   | ...          |
   |        5 | Python1015 | ...          |
   |        6 | Java1012   | ...          |
   +----------+------------+--------------+
   # 学生表
   +---------+----------+------------+---------+------+
   | stu_num | stu_name | stu_gender | stu_age | cid  |
   +---------+----------+------------+---------+------+
   | 1020    | 科比     | 男         |      24 |    6 |
   | 2020    | 李四     | 男         |      18 |    4 |
   +---------+----------+------------+---------+------+
   # 修改class_id=6的记录，关联的学生表的cid也会同步修改
   update classes set class_id=1 where class_id=6;
   +----------+------------+--------------+
   | class_id | class_name | class_remark |
   +----------+------------+--------------+
   |        1 | Java1012   | ...          |
   |        2 | Java1013   | ...          |
   |        3 | Java1014   | ...          |
   |        4 | Java1015   | ...          |
   |        5 | Python1015 | ...          |
   +----------+------------+--------------+
   +---------+----------+------------+---------+------+
   | stu_num | stu_name | stu_gender | stu_age | cid  |
   +---------+----------+------------+---------+------+
   | 1020    | 科比     | 男         |      24 |    1 |
   | 2020    | 李四     | 男         |      18 |    4 |
   +---------+----------+------------+---------+------+
   ```

3. 测试级联删除

   ```sql
   # 删除class_id=1的班级信息，学生表关联这条信息的记录也会被删除
   delete from classes where class_id=1;
   +----------+------------+--------------+
   | class_id | class_name | class_remark |
   +----------+------------+--------------+
   |        2 | Java1013   | ...          |
   |        3 | Java1014   | ...          |
   |        4 | Java1015   | ...          |
   |        5 | Python1015 | ...          |
   +----------+------------+--------------+
   +---------+----------+------------+---------+------+
   | stu_num | stu_name | stu_gender | stu_age | cid  |
   +---------+----------+------------+---------+------+
   | 2020    | 李四     | 男         |      18 |    4 |
   +---------+----------+------------+---------+------+
   
   ```


`注意：在项目上这种物理外键因为存在性能慢、增加设计复杂性、扩展性差，项目上一般使用逻辑外键，用程序逻辑去解决表与表的关联问题`

# 八、连接查询

> 通过对DQL的学习，我们可以很轻松的从一张表中查询出需要的数据；在企业的应用开发中，我们经常需要从多张表中查询数据（例如：我们查询学生信息的时候需要同时查询学生的班级信息）
>
> 可以通过连接查询从多张数据表提取数据
>
> 在MySQL中可以使用join实现多表的联合查询——连接查询，join按照其功能不同分为三个操作
>
> - inner join 内连接
> - left join  左查询
> - right join 右查询

#### 8.1 数据准备

###### 8.1.1 创建数据表

```sql
create table classes(
	class_id int primary key auto_increment,
	class_name varchar(20) not null unique,
	class_remark varchar(255)
);
create table students(
	stu_id int primary key auto_increment,
	stu_num char(6) not null unique,
	stu_name varchar(10) not null,
	stu_gender char(2) not null,
	stu_age int not null,
	cid int,
	constraint FK_STUDENTS_CLASSES foreign key(cid) references classes(class_id) ON UPDATE CASCADE ON DELETE CASCADE
);
```

###### 8.1.2 添加数据

```sql
# 添加班级
insert into classes(class_name,class_remark) values('PHP1010','This is PHP');
insert into classes(class_name,class_remark) values('PHP1011','This is PHP');
insert into classes(class_name,class_remark) values('PHP1012','This is PHP');
insert into classes(class_name,class_remark) values('Java1010','This is Java');
```

```sql
# 添加学生信息
insert into students(stu_num,stu_name,stu_gender,stu_age,cid) values('131401','kobe','男',18,1);
insert into students(stu_num,stu_name,stu_gender,stu_age,cid) values('131402','Juli','女',20,1);
insert into students(stu_num,stu_name,stu_gender,stu_age,cid) values('131403','San','男',28,1);
insert into students(stu_num,stu_name,stu_gender,stu_age,cid) values('131501','张三','男',22,2);
insert into students(stu_num,stu_name,stu_gender,stu_age,cid) values('131502','lisi','男',15,2);
insert into students(stu_num,stu_name,stu_gender,stu_age,cid) values('131503','wangwu','男',18,2);

insert into students(stu_num,stu_name,stu_gender,stu_age) values('202211','小明','男',18);
insert into students(stu_num,stu_name,stu_gender,stu_age) values('202212','小红','男',18);
```



#### 8.2 内连接 INNER JOIN

**语法**

```sql
select ... from tableName1 inner join tableName2 ON 匹配条件 [where 条件];
```

###### 8.2.1 笛卡尔积

- 笛卡尔积（A集合和B集合）：使用A中的每个记录一次关联B中每个数据，笛卡尔积的总数=A总数*B总数
- 如果直接执行`select ... from tableName1 inner join tableName2;`会获取两种数据表中的数据集合的笛卡尔积（依次使用tableName1中的每一条记录去匹配tableName2的每条记录）

###### 8.2.2 内连接条件

> 两张表时用inner join连接查询之后生产的笛卡尔积数据中很多数据都是无意义的
>
> 如何消除无意义的数据？——添加两张表进行连接查询的条件

- 使用`on`设置两张表连接查询的匹配条件

  ```sql
  # 使用 where 连接过滤条件：会先生成笛卡尔积，再从笛卡尔积筛选数据（效率低）
  select * from classes INNER JOIN students where classes.class_id = students.cid;
  
  # 先判断ON设置的连接查询条件：先判断条件是否成立，如果成立两张条进行组合再生成一条结果记录
  select * from classes INNER JOIN students ON classes.class_id = students.cid;
  ```

- 结果：只获取两张表中匹配条件成立的数据，任何一张表在另一张表中如果没有找到对应匹配则不会出现在查询结果中



#### 8.3 左连接 LEFT LOIN

> 需求：请查询出所有的学生信息，如果学生有关联的班级信息，则将关联班级表的信息查询出来

左连接：显示左表中的所有数据，如果右表中存在与左表记录满足匹配条件的数据，则进行匹配，如果右表中不存在匹配数据，则显示为NULL

```sql
# 语法
select ... from leftTable LEFT JOIN rightTable ON 匹配条件 [where 条件]
# 左连接 显示左表的所有数据
select * from classes LEFT JOIN students ON classes.class_id = students.cid;
```

![image-20220308003530509](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220308003530509.png)

#### 8.4 右连接 RIGHT JOIN

> 一般不使用，只要调换表的位置就可以继续使用左连接

```sql
# 右连接：显示右表中的所有记录
# 语法
select ... from leftTable RIGHT JOIN rightTable ON 匹配条件 [where 条件]
```

![image-20220308003657754](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220308003657754.png)

#### 8.5 数据表别名

> 如果在连接查询的多张表中存在相同名字的字段，我们可以使用`数据表.字段名`来进行区分，如果表名太长则不便于SQL语句的编写，我们可以使用数据库别名（使用关键字`as` | 也可以不写）

```sql
select s.*,c.class_name
from classes c
right JOIN students s
ON c.class_id = s.cid;
```



#### 8.6 子查询/嵌套查询

> 子查询——先进行一次查询，第一查询的结果作为第二次查询的源/条件（第二次查询是基于第一次查询结果来进行的）

###### 8.6.1 子查询 返回单个值——单行单列

**案例1：**`查询班级名称为‘PHP1010’班级中的学生信息（只知道班级名称，不知道班级ID）`

- 传统的方式：

  ```sql
  # a.查询PHP1010班的主键；
  select class_id from classes where class_name='PHP1010';
  
  # b.查询此主键下的学生信息
  select * from students where cid=1;
  ```

- 子查询

  ```sql
  select * from students where cid=(select class_id from classes where class_name='PHP1010');
  ```

###### 8.6.2 子查询 返回多个值——多行单列

**案例2**：`查询所有PHP班级中的学生信息`

- 传统的方式

   ```sql
   # a.查询所有PHP班的class_id
   select class_id from classes where class_name like 'PHP%';
   +----------+
   | class_id |
   +----------+
   |	 1	   |
   |	 2	   |
   |	 3     |
   +----------+
   
   # b.查询这些班级编号中的学生信息(用union将多个查询结果语句整合起来)
   select * from students where cid=1
   union
   select * from students where cid=2
   union
   select * from students where cid=3;
   ```

- 子查询

  ```sql
  # 如果子查询返回的结果是多个值(单列多行)，条件使用IN / NOT IN 
  select * from students where cid in(select class_id from classes where class_name like 'PHP%');
  ```


###### 8.5.3 子查询 返回多个值——多行多列

**案例3：**`查询cid=1的班级中性别为男的学生信息`

- 传统的方式

  ```sql
  # 多条件查询
  select * from students where cid=1 and stu_gender='男';
  ```

- 子查询

  ```sql
  # 子查询 先查询cid=1班级中的所有学生信息，将这些信息作为一个整体虚拟表（多行多列）
  # 在基于这个虚拟表查询性别为男的学生(‘虚拟表’需要别名)
  select * from (select * from students where cid=1) as t where t.stu_gender='男';
  ```





# 九、存储过程

#### 9.1 存储过程介绍

###### 9.1.1 SQL指令执行过程

![image-20220308104806151](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220308104806151.png)

从SQL执行的流程中我们分析存在的问题：

1. 如果我们需要重复多次执行相同的SQL，SQL执行都需要通过连接传递到MySQL，并且需要经过编译和执行的步骤;

2. 如果我们需要连续执行多个SQL指令，并且第二个SQL指令需要使用第一个SQL指令执行的结果作为参数;

###### 9.1.2 存储过程介绍

> 存储过程（Stored Procedure）是一种在数据库中存储复杂程序，以便外部程序调用的一种数据库对象。
>
> 存储过程是为了完成特定功能的SQL语句集，经编译创建并保存在数据库中，用户可通过指定存储过程的名字并给定参数(需要时)来调用执行。
>
> 存储过程思想上很简单，就是数据库 SQL 语言层面的代码封装与重用。

###### 9.1.3 存储过程优缺点分析

 **存储过程优点：**

1. SQL指令无需客户端编写，通过网络传送，可以节省网络开销，同时避免SQL指令在网络传输过程中被恶意篡改保证安全性

2. 存储过程经过编译创建并保存在数据库中的，执行过程无需重复的进行编译操作，对SQL指令的执行过程进行了性能分析

3. 存储过程中多个SQL指令之间存在逻辑关系，支持流程控制语句（分支、循环）。可以实现更为复杂的业务

**存储过程的缺点**

 存储过程缺点：

1. 存储过程时根据不同的数据库进行编译、创建并存储在数据库中；当我们需要切换到其他的数据库产品，需要重新编写存储过程

2. 存储过程受限于数据库产品，如果需要高性能优化会成为问题

3. 在互联网项目中如果需要数据库的高并发访问，使用存储过程会增加数据库的连接执行时间（因为我们将业务交给数据库进行处理）

#### 9.2 创建存储过程

######  9.2.1 存储过程创建语法

```sql
-- 语法
create procedure <proc_name>([IN/OUT args])
begin
	# SQL
end
-- 输入参数相当于参数
-- 输出参数相当于返回值
```

**实例**

```sql
-- 创建一个存储过程加法运算：
create procedure proc_add(IN a int,IN b int,OUT c int)
begin
	SET c = a + b;
end
```



#### 9.3 调用存储过程

```sql
-- 调用存储过程

-- 定义变量@m
SET @m = 0;\

-- 调用存储过程，将3传递给a，将2传递给b，将@m传递给c
call proc_add(3,2,@m);

-- 显示变量值
select @m from dual;
```



#### 9.4 存储过程中变量的使用

> 存储过程中的变量分为两种：
>
> - 局部变量
> - 用户变量

######  9.4.1 定义局部变量

局部变量：定义在存储过程中的变量，只能在存储过程内部使用

- 局部变量语法

  ```sql
  -- 局部变量要定义在存储过程中，而且必须定义在存储过程开始
  create procedure <proc_name>([IN/OUT args])
  begin
  	declare <name> <type> [default value]; 
  end
  ```

- 实例

  ```sql
  # 创建一个过程，b等于a的平方 + a/2
  create procedure test(IN a int,OUT b int)
  begin
  	declare x int default 0; -- 定义局部变量x
  	declare y int; -- 定义局部变量y
  	set x = a*a;
  	set y = a/1;
  	
  	SET b =  x+y;
  end;
  ```

###### 9.4.2 定义用户变量

用户变量：相当于全局变量，定义的用户变量可以通过`select @attrName from dual`进行查询

```SQL
-- 用户变量会存储在mysql数据库的数据字典中(dual)
-- 用户变量定义使用set关键字直接定义，变量名要以@开头
set @n = 1;
```

###### 9.4.3 给变量设置值

- 无论是局部变量还是用户变量，都是使用set关键字修改值

```sql
SET @n = 1;
call test(6,@n);
select @n from dual;
```

###### 9.4.4 将查询结果赋值给变量

在存储过程中使用`select...into..给`变量赋值

```SQL
--  创建存储过程：查询学生的数量并返回
create procedure porc_count_stu(OUT c int)
begin
	select count(*) INTO c from students;
end

-- 调用存储过程
call porc_count_stu(@n);
select @n from dual;
```

9.4.5 用户变量使用注意事项

> 因为用户变量相当于全局变量，可以在SQL指令以及多个存储过程中共享，在开发中建议尽量少使用用户变量，用户变量过多会导致程序不易理解、难以维护



#### 9.5 存储过程的参数

> MySQL存储过程的参数一共有三种：IN 、OUT、INOUT

###### 9.5.1 IN 输入参数

输入参数——在调用存储过程中传递数据给存储过程的参数（在调用过程中必须为具有实际值的变量）

```sql
-- 创建存储过程，添加学生信息
create procedure proc_insert_stu(IN snum char(6),IN sname varchar(10), IN sgender char(2),IN sage int,IN cid int,IN remark varchar(255))
begin
	insert into students(stu_num,stu_name,stu_gender,stu_age,cid,remark)
	values(snum,sname,sgender,sage,cid,remark);
end;
call proc_insert_stu('202299','Jack','男',18,1,'...');
```

###### 9.5.2  OUT 输出参数

输出参数——将存储过程中产生的数据返回给过程调用者，相当于Java方法的返回值，但不同的是一个存储过程可以有多个输出参数

```sql
-- 创建存储过程，根据学生学号，查询学生姓名
create procedure proc_sel_name(IN snum char(6),OUT sname varchar(10))
begin
	select stu_name INTO sname from students where stu_num=snum;
end;
set @name='';
call proc_sel_name('202299',@name);
select @name from dual;
```

###### 9.5.3 INOUT 输入输出参数

集可以当输入参数又可以当输出参数（不建议使用，代码可读性差）

```sql
create procedure proc_sel_name1(INOUT str varchar(10))
begin
	select stu_name INTO str from students where stu_num=str;
end;
set @name='202299';
call proc_sel_name1(@name);
```



#### 9.6 存储过程中流程控制

> 在存储过程中支持流程控制语言用于实现逻辑的控制

###### 9.6.1 分支语句

- if-then-else

  ```sql
  -- 单分支：如果条件成立，则执行SQL
  if conditions then
  	-- sql
  end if
  -- 如果参数阿德值为1，则添加一条班级信息
  create procedure proc_test2(IN a int)
  begin
  	if a=1 then
  		insert into classes(class_name,remark) values('1班','...');
  	end if;
  end;
  ```

  ```sql
  -- 双分支：如果条件成立则执行SQL1，否则执行SQL2
  if condition then
  	-- SQL1
  else
  	-- SQL 2
  end if
  -- 实例：
  create procedure proc_test3(IN a int)
  begin
  	if a=1 then
  		insert into classes(class_name,remark) values('1班101','...');
  	else
  		insert into students(stu_num,stu_name,stu_gender,stu_age,cid,remark) values('202298','xiao 2','男',20,1,'...');
  	end if;
  end;
  ```

- case

  ```sql
  create procedure proc_test4(IN a int)
  begin
  	case a
  	when 1 then
  		-- SQL1
  		insert into students(stu_num,stu_name,stu_gender,stu_age,cid,remark) values('202297','then1','男',20,1,'...');
  	when 2 then
  	  -- SQL
  		insert into students(stu_num,stu_name,stu_gender,stu_age,cid,remark) values('202296','then2','男',20,1,'...');
  	else
  		insert into students(stu_num,stu_name,stu_gender,stu_age,cid,remark) values('202295','else','男',20,1,'...');
  	end case;
  end;
  ```


###### 9.6.2 循环语句

- while

  ```sql
  -- while
  create procedure proc_test5(IN a int)
  begin
  	declare i int;
  	set i = 0;
  	while i<a do
  		insert into classes(class_name,remark) values(CONCAT('Java',i),'....');
  		set i = i+1;
  	end while;
  end;
  
  call proc_test5(3);
  ```

- repeat

  ```sql
  -- repeat
  create procedure proc_test6(IN a int)
  begin
  	declare i int;
  	set i = 1;
  	repeat
  		
  		insert into classes(class_name,remark) values(CONCAT('SQL',i),'....');
  		set i = i + 1;
  		
  	until i > a end repeat;
  end;
  
  call proc_test6(3);
  ```

- loop

  ```sql
  -- loop
  create procedure proc_test7(IN a int)
  begin
  	declare i int;
  	set i = 1;
  	myloop:loop
  		insert into classes(class_name,remark) values(CONCAT('HTML',i),'....');
  		set i = i + 1;
  		if i=a then
  			leave myloop;
  		end if;
  	end loop;
  end;
  
  call proc_test7(5);
  ```


#### 9.7 存储过程管理

###### 9.7.1 查询存储过程

> 存储过程时属于某个数据库的，

```sql
-- 根据数据库名，查询当前数据库的存储过程
show procedure status where db='db_test2';
-- 查询存储过程的创建细节
show create procedure db_test2.proc_test5; 
```

###### 9.7.2 修改存储过程

> 修改存储过程指的是修改存储过程的特征

````sql
alter procedure <proc_name> 特征1 特征2 ....
````

存储过程的特征参数：

- `CONTAINS SQL`表示子程序包含SQL语句，但不包含读或写数据的语句
- `NO SQL`表示子程序中不包含SQL语句
- `READS SQL DATA`表示子程序包含读数据的语句
- `MODIFIES SQL DATA`表示子程序包含写数据的语句
- `SQL SECURITY`{ DEFINER | INVOKER} 指明谁有权限来执行
  -  `DEFINER`表示只有定义者自己才能够执行
  - `INVOKER`表示调用者可以执行

- `COMMENT ‘string’`表示注释信息

```sql
alter procedure proc_test1 NO SQL;
```

###### 9.7.3 删除存储过程

```sql
-- 删除存储过程
-- dorp 删除数据库中的对象 数据库、数据表、列、存储过程、视图、触发器、索引.....
drop procedure proc_test1;
```



#### 9.8 存储过程练习案例

> 使用存储过程解决项目开发过程中的问题
>
> 案例：使用存储过程完成借书操作

###### 9.8.1 数据准备

```sql
-- 创建图书信息表
create table books(
	book_id int primary key auto_increment,
	book_name varchar(10) not null,
	book_auther varchar(20) not null,
	book_price decimal(10,2) not null,
	book_stock int not null,
	book_desc varchar(255)
);

-- 添加图书信息
insert into books(book_name,book_auther,book_price,book_stock,book_desc)
values('数据库基础概论','小明',56.30,10,'This is Databases');
insert into books(book_name,book_auther,book_price,book_stock,book_desc)
values('计算机硬件基础','小红',80.20,20,'This is Computer');


-- 创建学生表
create table students(
  stu_id int primary key auto_increment,
	stu_num char(6) not null unique,
	stu_name varchar(10) not null,
	stu_gender char(2) not null,
	stu_age int not null
);

-- 添加学生信息
insert into students(stu_num,stu_name,stu_gender,stu_age) values('202201','Anne','女',18);
insert into students(stu_num,stu_name,stu_gender,stu_age) values('202202','Bob','男',19);
insert into students(stu_num,stu_name,stu_gender,stu_age) values('202203','Cindy','女',22);
```

**需求分析**

> 创建一个存储过程实现借书的操作：那个学生借那本书，借了多少本？
>
> 操作：
>
> - 保存借书记录
> - 修改图书库存
>
> 条件：
>
> - 判断学生是否存在
> - 判断图书是否存在、库存是否充足

**创建借书记录表**

```sql
-- 借书记录表（书本和学生两个实体时多对多的关系）
create table records(
	rid int primary key auto_increment,
	sid int not null,
	bid int not null,
	borrow_num int not null,
	is_return int not null, -- 0:未还; 1:已还
	borrow_date datetime not null
)
```

###### 9.8.2 创建存储过程

```sql
-- 实现借书业务
-- 参数1：s 输入参数 学号
-- 参数2：b 输入参数 图书编号
-- 参数3：m 输入参数 借书的数量
-- 参数4：state 输出参数 借书的状态（1 借书成功，2 学号不存在，3 图书不存在，4 库存不足）
create procedure proc_borrow_book(IN s int,IN b int,IN m int,OUT state int)
begin
	declare stu_count int default 0; -- 学生数量
	declare bstock int default 0; -- 图书库存
	declare book_count int default 0; -- 图书
	
	-- 学生是否存在
	select count(*) INTO stu_count from students where stu_num = s;
	if stu_count>0 then
		-- 学生存在
		-- 判断图书是否存在
		select count(*) INTO book_count from books where book_id = b;
		if book_count >= 1 then
			-- 图书存在
			-- 判断图书库存
			select book_stock INTO bstock from books where book_id = b;
			
			if bstock>m then
				-- 库存充足
				-- 生成借书记录
				insert into records(sid,bid,borrow_num,is_return,borrow_date) values(s,b,m,0,sysdate());
				-- 修改库存
				update books set book_stock = bstock - m where book_id = b;
				set state = 1;
			else
				-- 库存不足
				set state = 4;
			end if;
		else
			-- 图书不存在
			set state = 3;
		end if;
	else
		-- 学生不存在
		set state = 2;
	end if;
end;

-- 调用存储过程
set @state = 0;
call proc_borrow_book('202202',2,5,@state);
select @state from dual;
```



#### 9.9 游标

> 问题：如果我们要创建一个存储过程，需要返回查询到的多条数据（结果集）

###### 9.1.1 游标的概念

游标可以用来依次取出查询结果集中的每一条数据——逐条读取结果集中的记录

###### 9.1.2 游标的使用不走

**1、声明游标**

- 语法

  ```sql
  -- 声明游标
  DECLARE <cursor_name> CURSOR FOR <select>;
  -- 打开游标
  open mycursor;
  -- 使用游标：提取当前指向的记录（提取之后游标自动下移）
  FETCH mycursor INTO bname,bauther,bprice;
  ```

- **实例**

  ```sql
  create procedure proc_test2(OUT result varchar(255))
  begin
  	declare bname varchar(20);
  	declare bauther varchar(20);
  	declare bprice decimal(10,2);
  	declare num int;
  	declare i int;
  	declare str varchar(50);
  	-- 此查询语句执行之后返回的时一个结果集（多条记录）,使用游标可以来遍历查询结果集
  	declare mycursor cursor for select book_name,book_auther,book_price from books;
  	select count(*) INTO num from books;
  	-- 打开游标
  	open mycursor;
  	-- 使用游标要结合循环语句
  	set i = 0;
  	while i<num do
  		-- 使用游标：提取当前指向的记录（提取之后游标自动下移）
  		FETCH mycursor INTO bname,bauther,bprice;
  		set i = i + 1;
  		set str = concat_ws('~',bname,bauther,bprice);
  		set result = concat_ws(',',result,str);
  	end while;
  	
  	-- 关闭游标
  	close mycursor;
  end;
  
  set @r = '';
  call proc_test2(@r);
  select @r from dual;
  ```



# 十、触发器

#### 10.1 触发器的介绍

> 触发器，就是一种特殊的存储过程。触发器和存储过程一样是一个能够完成特定功能、存储在数据库服务器上的SQL片段，但是触发器无需调用，当对数据表中的数据执行DML操作时自动触发这个SQL片段的执行，无需手动调用
>
> 在MySQL只有执行insert、delete、update操作才能触发触发器的执行

#### 10.2 触发器的使用

###### 10.2.1 案例说明

案例：当向学生信息表添加、删除和修改学生信息时，使用触发器自动进行日志记录

```sql
-- 创建学生表
create table students(
  stu_id int primary key auto_increment,
	stu_num char(6) not null unique,
	stu_name varchar(10) not null,
	stu_gender char(2) not null,
	stu_age int not null
);
-- 日志信息表
create table logs(
	id int primary key auto_increment,
	time datetime,
	log_text varchar(200)
);
```

```sql
-- 操作students表时，记录日志
insert into students(stu_num,stu_name,stu_gender,stu_age) values('202211','Eve','男',32);
-- 手动添加日志
insert into logs(time,log_text) values(now(),'添加202210学生');
```

###### 10.2.2 创建触发器

**语法**

```sql
create trigger <triggerName>
<before|after> <insert|delete|update> ON <tableName>
for each row	-- 行级触发器（影响多少行，触发多少次）
sql_statement 	-- 触发器操作
```

**实例**

```sql
-- 创建触发器：操作students，写入日志
create trigger tri_test1
after insert on students
for each row
insert into logs(time,log_text) values(now(),concat('insert',NEW.stu_num,'学生信息'));

-- 测试触发器
insert into students(stu_num,stu_name,stu_gender,stu_age) values('202211','Eve','男',32);
-- 插入两条数据时，触发了两次
insert into students(stu_num,stu_name,stu_gender,stu_age) values('202212','Eve','男',32),('202213','Fofo','男',20);
```

###### 10.2.3 查看触发器

```sql
show trigger;
```

###### 10.2.4 删除触发器

```sql
drop trigger tri_test1;
```



#### 10.3 NEW与OLD

> 触发器用于监听对数据表中数据的insert、delete、update操作，在触发器中通常处理一些DML的关联操作；我们可以使用`NEW`和`OLD`关键字触发器中操作的数据
>
> - NEW：在触发器中用于获取insert操作添加的数据、update操作修改后的数据
> - OLD：在触发器中用于获取delete操作删除前的数据、update操作修改前的数据

- insert操作（`NEW`）

  ```sql
  create trigger tri_test1
  after insert on students
  for each row
  insert into logs(time,log_text) values(now(),concat('insert了',NEW.stu_num,'的学生信息'));
  ```

- update操作（`NEW`代表修改后的数据；`OLD`代表修改前的数据）

  ```sql
  create trigger tri_test2
  after update ON students for each row
  insert into logs(time,log_text) values(now(),concat('修改后：',NEW.stu_name,'修改前：',OLD.stu_name));
  ```

- delete操作（`OLD`）

  ```sql
  create trigger tri_test3
  after delete ON students for each row
  insert into logs(time,log_text) values(now(),concat('删除了：',OLD.stu_name));
  ```


#### 10.4 触发器使用总结

###### 10.4.1 优点

- 触发器时自动执行的，当对触发器相关的表执行DML操作时立即执行

- 触发器可以实现表中的数据级联操作（关系操作），有利于保证数据的完整性；（应该用事务）

- 触发器可以对DML操作的数据进行更为复杂的合法性校验


###### 10.4.1缺点

- 使用触发器实现的业务逻辑如果出现问题将难以定位，后期维护困难
- 大量使用触发器容易导致代码结构杂乱，增加了程序的复杂性；
- 当触发器操作的数据量比较大时，执行效率会大大降低

###### 10.4.3 使用建议

- 在互联网项目中，应避免适应触发器；
- 对于并发量不大的项目可以选择使用存储过程，但是在互联网应用中不提倡使用存储过程（原因：存储过程将实现业务的逻辑交给数据库处理，一则增加了数据库的负载，二则不利于数据库的迁移）



# 十一、视图

#### 11.1 视图的概念

视图，就是`由数据库中一张表或者多张表根据特定的条件查询出的数据结构`的虚拟表

#### 11.2 视图的作用

- **安全性**：如果我们直接将数据授权给用户操作，那么用户可以CRUD数据表中的所有数据，加入我们想要对数据表的部分数据进行保护，可以将公开的数据生成视图，授权用户访问视图：用户通过查询视图可以获取数据表中公开的数据，从而达到将数据表中的部分数据对用户隐藏。
- **简单性**：如果我们需要查询的数据来源于多张数据表，可以使用多表连接查询来实现；我们通过视图将这些连表查询的结果对用户开放，用户则可以直接通过查询视图获取多表数据，操作更便捷

#### 11.3 创建视图 

**语法**

```sql
create view <ciewName>
AS
<selectSql>
```

**实例**

```SQL
-- 创建视图实例:查询学生借书的信息（学生名、图书名、借书数量）
create view view_test2
as
select stu_name,book_name,borrow_num from records r
left join students s on r.sid=s.stu_num
left join books b on r.bid=b.book_id;

-- 查询视图
select * from view_test2;
```

#### 11.4 视图数据的特性

> 视是虚拟表，查询视图的数据是来源于数据表的。当对视图进行操作时，对原数据表中的数据是否有影响？

**查询操作：**原数据表的数据的改变会影响视图的查询数据

**新增数据：**如果在视图中添加数据，数据会被添加到原数据表（单张表）

**删除数据：**如果从视图删除数据，数据也将从原表中删除（单张表）

**修改操作：**如果修改视图数据，则也将修改原数据表中的数据（单张表）

`视图的使用建议`：对复杂查询简化操作，并且不会对数据进行修改的情况下可以使用视图

#### 11.5 查询视图结构

```sql
-- 查询视图结构
desc <viewName>;
```

#### 11.6 修改视图

```sql
-- 方式1：重新创建覆盖
create or replace view view_test1
as
select * from students where stu_gender='女';
-- 方式2：用alter view
alter view view_test1
as
select * from students where stu_gender='男';

```

#### 11.7 删除视图

- 删除视图不会影响表中的数据

```sql
drop view <viewName>;
```



# 十二、索引

> 数据库是用来存储数据的，在互联网应用中数据库存储的数据可能会很大（大数据），`数据表中数据的查询速度会随着数据量的增长逐渐变慢`，从而导致响应用户请求的速度变慢——用户体验差，我们如何提高数据库的查询效率呢？

#### 12.1 索引的介绍

>  索引：就是用来提高数据表中数据查询效率的。索引将数据表中某一列/某几列的值取出来构造成便于查找的结构进行存储，生成数据表的目录，当我们进行数据查询的时候，则先在`目录`中进行查找得到对应的数据的地址，然后再到数据表中根据地址快速的获取数据记录，避免全表扫描

![image-20220310131746615](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220310131746615.png)



#### 12.2 索引的分类

MySQL中的索引，根据创建索引的列的不同，可以分为：

- 主键索引：在数据表的主键字段创建的索引，这个字段必须被primary key约束，每张表只能偶一个主键
- 唯一索引：在数据表中的唯一列创建的索引（unique），此列的所有值不能重复，可以为NULL
- 普通索引：在普通字段上创建的索引，没有唯一性的限制
- 组合索引：两个及以上字段联合起来创建的索引
- 全文索引：MySQL5.6版本新增的索引，可以实现通过关键字的检索（模糊查询like，但是比它快），但是在应用开发中通常时通过搜索引擎（数据库中间件）实现全文检索

`说明`

1. 在创建数据表时，将字段声明为主键（添加主键约束），会自动在主键字段创建主键索引
2. 在创建数据表时，将字段声明为唯一键（添加唯一约束），会自动在唯一字段添加唯一索引



#### 12.3 创建索引

 **唯一索引**

```sql
-- 语法
create unique index <indexNane> on 表名(字段名);
-- 创建唯一索引
create unique index index_test1 on tb_testindex(tid);
```

**普通索引**

```sql
-- 语法
create index <indexName> on 表名(字段名);
-- 创建普通索引
create index index_test2 on tb_testindex(name);
```

**组合索引**

```sql
-- 语法
create index <indexNane> on 表名(字段名1，字段名2);
-- 创建组合索引
create index index_test3 on tb_testindex(tid,name);
```

**全文索引**

```sql
create fulltext index <indexName> on 表名(字段名);
```



#### 12.4 索引使用

> 索引创建完成之后无需调用，当根据创建索引的列进行数据查询的时候，会自动使用索引
>
> 组合索引需要根据创建索引的所有字段进行查询时触发

- 在命令窗口查看查询语句的查询规划（查看使用的索引）

  ```sql
  explain select * from tb_testindex where fid=400000\G;
  ```

  ![image-20220310154337677](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220310154337677.png)

#### 12.5 查看索引

```sql
-- 查看索引
show create table tb_testindex/G; -- 命令行
show indexes from tb_testindex;
show keys from tb_testindex
```

#### 12.6 删除索引

```sql
drop index <indexName> on <tableName>;
-- 实例
drop index fi on tb_testindex;
```



#### 13.7 索引的使用总结

**优点：**

- 索引大大降低了数据库服务器在执行查询操作时扫描的数据，提高了查询数据的速度
- 索引可以避免服务器排序、将随机IO编程顺序IO

**缺点**

- 索引时根据数据表列来创建的，当数据表中发生DML操作时，索引需要更新
- 索引文件也会占用数据库空间

**注意事项**

- 数据表中数据不多时，不使用索引，全表扫描可能更快
- 数据量大但是DML操作很频繁时，不建议使用索引
- 不要再数据重复度高的列上创建索引（如性别）
- 创建索引之后，要注意查询SQL语句的编写，避免索引失效



# 十三、数据库事务

#### 13.1 数据库事务介绍

- 我们把完成特定的业务的多个数据库DML操作步骤称之为一个事务
- 事务，就是完成同一个业务的多个DML操作

```sql
-- 事务1 借书业务 
-- 操作1：在借书记录表中添加记录
insert into records(sid,bid,borrow_num,is_return,borrow_date) values(s,b,m,0,sysdate());
-- 操作2：修改图书库存
update books set book_stock = bstock - m where book_id = b;

-- 事务2 银行转账业务：张三给李四转账1000
-- 操作1：李四的账号+1000
-- 操作2：张三的账户-1000
```



#### 13.2 数据库事务的特性

**原子性**（Atomicity）：一个事务中的多个DML操作，要么同时执行成功，要么同时失败

**一致性**（Consistency）：事务执行之前和事务执行之后，数据库中的数据是一致的，完整性和一致性不能被破坏

**隔离性**（Isolation）：数据库允许多个事务同时执行，多个并行的事务之间不能互相影响

**持久性**（Durability）：事务完成之后，对数据库的操作是永久的



#### 13.3 MySQL的事务管理

###### 13.3.1 自动提交和手动提交

- 在MySQL中，默认DML指令的执行是自动提交的，当我们执行一个DML指令之后，自动同步到数据库中

![image-20220310214057247](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220310214057247.png)

###### 13.3.2 事务管理

> 开启事务，就是关闭自动提交——手动提交

- 在开始事务第一个操作之前，执行`start transaction`开启事务
- 依次执行事务中的每个DML操作
- 如果在执行的过程中的任何位置出现异常，则执行`rollback`回滚事务
- 如果事务中所有DML操作都执行成功，则在最后执行commit 提交事务

![image-20220310222717794](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220310222717794.png)

```sql
-- 借书业务 

-- 【开启事务】(关闭自动提交————手动提交)
start transaction;

-- 操作1：在借书记录表中添加记录
insert into records(sid,bid,borrow_num,is_return,borrow_date) values('202213',3,1,0,sysdate());

-- 发生异常
-- select aaa;

-- 【事务回滚】(清除连接缓存中的操作，撤销当前事务)
-- rollback;

-- 操作2：修改图书库存
update books set book_stock = 9 where book_id = 3;

-- 【提交事务】（将连接缓存的操作写入数据文件）
commit;
```



#### 13.4 事务隔离级别

> 数据库允许多个事务并行，多个事务之间是隔离的、相互独立的；如果多个事务之间不相互隔离并且操作同一数据时，可能会导致数据的一致性被破坏，并发事务处理也会带来一些问题：脏读、不可重复读（虚读）、幻读

MySQL数据事务隔离级别：

**读未提交**（read uncommitted）：T2可以读取T1执行但未提交的数据；可能会导致脏读

> 脏读，一个事务（T2）读取到了另一个事务（T1）中未提交的数据，但未提交的事务异常回滚了

![image-20220310233948527](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220310233948527.png)

**读已提交**（read committed）：只能读取到事务提交的数据，避免了脏读，可能会导致不可重复读（虚读）  

> 不可重复读（虚读）：在同一个事务中，两次查询操作读取到的数据不一致  
>
> 例如：在一个事务中（T2）先后进行了两次查询说数据，由于另一个事务（T1）在两次查询之间修改提交了数据，由于只能读取事务提交的的数据，两次查询的数据不一致

![image-20220310234411832](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220310234411832.png)

**可重复读**（repeatable read）：当一个事务对数据进行查询后，在事务结束之前其他事务不能修改对应的数据；避免了不可重复读（虚读），但可能会导致幻读

> 幻读，一个事务中以相同条件重新查询以前查询过的数据，发现另一个事务插入了满足其查询条件的新数据，这种现象就称为“幻读”

**串行化**（serializable）:同时只允许一个事务对数据表进行操作：避免了脏读、不可重复读（虚读）、幻读

| 隔离级别         | 脏读 | 不可重复读（虚读） | 幻读 |
| ---------------- | ---- | ------------------ | ---- |
| read uncommitted | √    | √                  | √    |
| read committed   | ×    | √                  | √    |
| repeatable read  | ×    | ×                  | √    |
| serializable     | ×    | ×                  | ×    |

###### 13.4.1 设置数据库隔离级别

> 我们可以通过设置数据默认的事务隔离级别来控制事务之间的隔离性：
>
> 也可以通过客户端与i数据库连接设置事务间的隔离性（在应用程序中--Spring）
>
> MySQL数据库默认的隔离级别为可重复读

- 查看MySQL数据库默认的隔离级别

  ```sql
  -- 在MySQl8.0.3之前
  select @@tx_isolation;
  -- 在MySQL8.0.3之后
  select @@transaction_isolation;
  ```

- 设置MySQL默认隔离级别

  ```sql
  set session transaction isolation level <read committed>;
  ```



# 十四、数据库设计

> MySQL数据作为数据库存储的介质为应用系统提供数据存储的服务，我们如何设计出合理的数据库、数据表以满足应用系统的数据存储需求呢？

- 车库：用来存放车辆的，车库都需要划分车位，如果不划分，车子杂乱无章的存放可能会导致车辆堵塞，同时也可能造成场地的浪费——有限的场地能够停放最多的车辆，同时方便每一辆车的出入
- 数据库：用来存放数据的，我们需要设计合理的数据表——能够完成数据的存储，同时能够方便的提取应用系统所需的数据

#### 14.1 数据库设计流程

> 数据库时为应用系统服务的，数据库存储什么样的数据也是由应用系统来决定的。
>
> 当我们进行应用系统开发时，我们首先明确应用系统的功能需求——软件系统的需求分析

1. 根据应用系统的功能，分析数据实体（实体，就是要存储的存储对象）

   电商系统：商品、用户、订单......

   教务关系系统：学生、课程、成绩......

2. **提取实体的数据项**（数据项就是实体的属性）

   商品（商品名称、商品价格、商品图片.......）

   用户（登录名、登录密码.......）

3. **根据数据库设计三范式规范实体的数据项** 检查实体的数据项是否满足数据库设计的三范式

   `如果实体的数据项不满足三范式，可能会导致数据的冗余，维护困难，破快数据一致性等问题`

4. **绘制E-R图**（实体关系图，直观的展示实体与实体之间的关系）
5. **数据库建模**
   - 三线图进行数据库设计
   - PowerDesigner
   - PDMan

6. **建库建表** 编写SQL指令创建数据库、数据表

7. **添加测试数据，SQL测试**



#### 14.2 数据库设计案例

> 学校图书馆图书管理系统（借书）

###### 14.2.1 数据实体

- 学生
- 图书类别
- 图书
- 借书记录
- 图书管理员

###### 14.2.2 提取数据项

- 学生（学号、姓名、年龄、....）
- 院系（院系编号、院系名称、院系说明）
- 图书类别（类别ID、类别名称、类别描述）
- 图书（图书ID、图书名称、图书作者、图书封面、图书价格、图书库存....）
- 借书记录（记录ID、学生ID、图书ID、借书数量、是否归还、借书日期、还书日期）
- 管理员（管理员ID、登录名、登录密码、）
- 员工信息（员工编号、员工姓名、手机、QQ、邮箱）

###### 14.2.3 数据库设计三范式

`第一范式`：要求数据表中的字段不可再分

以下表不满足第一范式

![image-20220311130738355](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220311130738355.png)

`第二范式`：不存在非关键字段对关键字段的部份依赖，就是一个表只能保存一种数据，不可以把多种数据保存在同一张表

以下表不满足第二范式

![image-20220311131703065](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220311131703065.png)

将每个关键字段列出来、关键字段的组合也列出来，依次检查每个给关键字段

![image-20220311131712490](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220311131712490.png)

`第三范式`：不存在非关键字段的传递依赖

以下数据表不满足第三范式

![image-20220311134305254](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220311134305254.png)

将关键字段和被依赖的非关键字段分别作为主键，依次检查所有的非关键字段的依赖关系

![image-20220311133655831](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220311133655831.png)

###### 14.2.4 数据库建库（E-R图）

> E-R（Entity - Relationship）实体关系图，用于直观的体现实体与实体之间的关联关系（一对一、一对多、多对多）

![image-20220311145517778](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220311145517778.png)

E-R图实例：

![image-20220311145629512](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220311145629512.png)

**三线图** 统一数据实体的表结构

> 每个实体创建一张数据表
>
> 多对多关联：需额外创建一张数据表维护关系，关系表分别创建外键与两张表关联
>
> 一对多、多对一关联：在多的一端添加外键与一的一端的主键建立外键约束

![image-20220312010304915](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220312010304915.png)



###### 14.2.5 数据库建模（PD）

> E-R图实际上就是数据库建模的一部分
>
> - 1.E-R图  2.数据表设计  3.建库建表
> - PowerDesigner建模工具 导出数据表
> - PDMam建模工具

1. `下载并安装PowerDesigner建模工具`

2. `PowerDesigner使用`

   - 概念数据模型（选择workspace→右键new→Conceptual Data Model），相当于E-R图

     ![image-20220311235130499](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220311235130499.png)

   - 逻辑数据模型（打开概念模型：tools→Generate Logical Data Model），体现了的主外键关联（程序员视角）

     ![image-20220311235559129](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220311235559129.png)

   - 物理数据模型（打开逻辑模型：tools→Generate Physical Data Model，选择数据库类型）

     - 可以对物理数据模型进行微调

     - 可以通过物理数据模型生成建库建表的SQL语句（在物理模型窗口中→Database工具栏→Genceate Database→生成SQL）

     - 通过数据库管理工具执行SQL文件就可以完成数据库的创建

       ![image-20220312003104776](C:\Users\Zhongbf\AppData\Roaming\Typora\typora-user-images\image-20220312003104776.png)

   - 面向对象模型（tools→Generate Object Orentited Model）

     - 生成实体类

     > 在实际项目开发中，我们通常不会使用建模工具来生成数据表、实体类，生成的代码不合规范



###### 14.2.6  数据库建模（PDMan）

- 下载安装PDMan
- 创建项目--在项目中创建数据表
- 在项目中生成关系图





# 思维导图

![](F:\Mindmaster\MySQL数据库.jpg)

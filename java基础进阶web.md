<center><h1>java结合web进阶</h1><center>

### 回顾数据库相关知识

#### sql语句的分类

+ ddl 定义数据库对象   结构有关系 create  table
+ dml  数据操作语言  进行更新数据表  update  delete   insert
+ dql   用来查询数据表结构
+ dcl 数据控制语言   创建用户    定义数据库访问权限

### 常用的命令

#### 对数据库的操作

+ create  database  xxx character set gbk  //创建带编码的数据库
+ show databases 查看数据库
+ show create database xxxx   查看数据库的结构编码
+ dop database xxx   删除数据裤
+ use xxx  选择选用哪个数据库
+ select  database();   //查看当前使用的数据库

#### 对表的操作

+ create table xxx  //创建数据表  
+ xxxx  类型  【约束】  对每个字段的定义
+ show  tables// 查看所有表
+ show create table   xxxx;   //详细查看   包括表的字符集
+ desc  xxxx 查看表的结构
+ drop   table xxxx  删除一个表
+ alter table   xxxx add   字段   类型  【约束】  添加一列
+ alter table xxx  modify   字段   类型（长度） 【约束】   修改一列
+ alter table xxx  change    old（列名）   new （新列名）   类型（长度） 【约束】   修改一列

+ alter table   xxxx drop 列名;   //删除一列
+ rename table   xxxx  to   newtablename;   //修改表的名字
+ alter table xxx    character  set    utf8;   //设置表的字符集

#### 字段的类型

+ int类型
+ double(m, d)
+ decimal(m, d) //用于表示钱数的时候
+ datatime
+ timestamp
+ varchar

#### 对表记录的操作

+ insert into xxxx  values()
+ update xxxx  set  xxx=xx  where...
+ delete from  xxxx  where  ....    truncate  (删除整个表   然后创建一个一样的表  和事务配合无法找回)

#### 事务（tansaction 关键字）

+ start     transaction  
+ 
#数据库操作SQLite
[教程网站](!http://www.runoob.com/sqlite/sqlite-tutorial.html)
相关知识
1. [RDBMS](!) Relational Database Management System
	数据库管理系统

##SQLite储存类:
> NULL 一个null值
> INTEGER 带符号的整数
> REAL 浮点值,8个字节的IEEE浮点数
> TEXT 文本字符串,使用数据库编码(UTF-8,UTF-16,UTF-16LE
> BLOB blob数据,完全根据输入的字节存储

#SQLite语法
##大小写敏感性
> SQLite是不区分大小写的,但是有些命令是大小写敏感的,比如: GLOB和glob在SQLite的语句中有不用的含义

##注释
> SQLite注释是附加的注释,可以在SQLite代码中添加,可以出现在空白处,表达式内,和其他SQL语句的中间,
> SQL注释以两个连续的"-"字符开始(ASCII 0x2d)并扩展至下一个换行符(ASCII 0x0a)或直到输入结束,以先到者为准
> 也可以使用C的风格注释,以"/*"开始,并扩展至下一个"*/"字符,

##SQLite语句
> 所有的SQLite语句可以以任意关键字开始, 如: SELECT(选择),
> INSERT(插入),UPDATE(更新),DELETE(删除),ALTER(改变),DROP

## SQLite ANALYZE:
> ANALYZE;
> or
> ANALYZE database_name;
> or
> ANALYZE database_name.table_name;

##SQLite AND/OR:
>SELECT column1, column2...columnN
>FORM table_name
>WHERE CONDITION-1 {AND|OR} CONDITION-2;

##SQLite ALTER TABLE:
> ALTER TABLE table_name ADD COLUMN column_def...;

##SQLite ALTER TABLE (Reaname):
> ALTER TABLE table_name RENAME TO new_table_name;

##SQLite ATTACH DATABASE:
> ATTACH DATABASE 'DatabaseName' As 'Alias-Name'

##SQLite BEGIN TRANSACTION:
> BEGIN;
> or
> BEGIN EXCLUSIVE TRANSACTION;

##SQLite CREATE TABLE:
> CREATE TABLE tbale_name(
>  column1 datatype,
>  column2 datatype,
>  column3 datatype,
>  .....
>  colunmN datatype
>  PRIMARY KEY(one or more columns)
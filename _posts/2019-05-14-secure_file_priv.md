---
layout: post
title: MySQL secure_file_priv
categories: Analytics
---

MySQL使用时经常碰到下面问题：

Error Code: 1290. The MySQL server is running with the --secure-file-priv option so it cannot execute this statement

原因在于[Mysql --secure-file-priv](https://dev.mysql.com/doc/refman/8.0/en/server-options.html#option_mysqld_secure-file-priv)限制了数据的导入和导出操作。

$mysql -u root -p

mysql>SHOW VARIABLES LIKE "secure_file_priv";

secure_file_prive=null   -- 限制mysqld 不允许导入导出

secure_file_priv=/tmp/   -- 限制mysqld的导入导出只能发生在/tmp/目录下

secure_file_priv=' '     -- 不对mysqld 的导入 导出做限制

修改 /etc/my.cnf 文件

```
[mysqld_safe]
[mysqld]
secure_file_priv=""
```

重启mysql server
mysql
=====

mysql-phpmyadmin



mysql有时候忘记密码了怎么办?我给出案例和说明!

　　Windows下的实际操作如下

　　1.关闭正在运行的MySQL。

　　2.打开DOS窗口，转到mysql\bin目录。

　　3.输入mysqld --skip-grant-tables回车。如果没有出现提示信息，那就对了。

　　4.再开一个DOS窗口(因为刚才那个DOS窗口已经不能动了)，转到mysql\bin目录。

　　5.输入mysql回车，如果成功，将出现MySQL提示符 >

　　6. 连接权限数据库>use mysql; (>是本来就有的提示符,别忘了最后的分号)

　　6.改密码：> update user set password=password("520") where user="root"; (别忘了最后的分号)

　　7.刷新权限(必须的步骤)>flush privileges;

　　8.退出 > \q

　　9.注销系统，再进入，开MySQL，使用用户名root和刚才设置的新密码123456登陆。

　　第一步

　　C:\Documents and Settings\Administrator>cd D:\web\www.php100.com\Mysql\MySQL Se

　　rver5.5\bin

　　C:\Documents and Settings\Administrator>d:

　　D:\web\www.php100.com\Mysql\MySQL Server5.5\bin>mysqld --skip-grant-tables

　　第二步

　　Microsoft Windows [版本 5.2.3790]

　　(C) 版权所有 1985-2003 Microsoft Corp.

　　C:\Documents and Settings\Administrator>cd D:\web\www.php100.com\Mysql\MySQL Se

　　rver5.5\bin

　　C:\Documents and Settings\Administrator>d:

　　D:\web\www.php100.com\Mysql\MySQL Server5.5\bin>mysql

　　Welcome to the MySQL monitor. Commands end with ; or \g.

　　Your MySQL connection id is 1

　　Server version: 5.5.10 MySQL Community Server (GPL)

　　Copyright (c) 2000, 2010, Oracle and/or its affiliates. All rights reserved.

　　Oracle is a registered trademark of Oracle Corporation and/or its

　　affiliates. Other names may be trademarks of their respective

　　owners.

　　Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

　　mysql> use mysql;

　　Database changed

　　mysql> update user set password=password("520") where user="root";

　　Query OK, 1 row affected (0.00 sec)

　　Rows matched: 1 Changed: 1 Warnings: 0

　　mysql> flush privileges;

　　Query OK, 0 rows affected (0.00 sec)

　　mysql> \q

　　Bye

　　D:\web\www.php100.com\Mysql\MySQL Server5.5\bin>
　　

Do not install anything on a button to your website directory, you'll destroy your site database data, remember to local backup database data

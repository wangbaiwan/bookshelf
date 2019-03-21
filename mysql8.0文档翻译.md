---
title: mysql8.0文档翻译
tags: mysql
grammar_cjkRuby: true
---
[toc]
# 第一章 概览
## 1.1 关于这个文档
## 1.2 排版和语法约定
## 1.3 Mysql数据库管理系统概述
## 1.4 Mysql8.0新特性
## 1.5 Mysql8.0中添加、弃用和移除的服务器和状态变量以及操作
## 1.6 更多Mysql信息
## 1.7 如何反馈bug和问题
## 1.8 Mysql遵循的标准
## 1.9 致谢
# 第二章 安装和更新
## 2.1 安装指导
## 2.2 在Unix/Linux上使用二进制文件安装
## 2.3 在Windows上安装
## 2.4 在macOS上安装
## 2.5 在Linux上安装
## 2.6 使用ULN安装（Unbreakable Linux Network）
## 2.7 在Solaris上安装
## 2.8 在FreeBSD上安装
## 2.9 通过源码安装
## 2.10 安装后的工作与测试
## 2.11 升级Mysql
## 2.12 降级Mysql
## 2.13 Perl安装说明
# 第三章 教程
本章通过展示如何使用mysql客户端程序创建和使用一个简单数据库，来提供MySQL的教程介绍。mysql（有时称为“终端监视器”或只是“监视器”）是一个交互式程序，你可以连接到MySQL服务器，运行查询和查看结果。 mysql也可以在批处理模式下使用，事先将查询放在文件中，然后告诉mysql执行文件的内容。这两种使用方法都会在下文中介绍。

要查看mysql提供的选项列表，请使用--help选项调用它：
```shell
> mysql --help
```
本章假设你已安装了mysql，并且你可以连接MySQL服务器。如果不是这样，请联系你的MySQL管理员。 （如果你是管理员，请参看手册的相关部分，例如第5章，MySQL服务器管理。）

本章介绍了设置和使用数据库的整个过程。如果您只对访问现有数据库感兴趣，则可能需要跳过描述如何创建数据库及其包含的表的部分。

因为本章本质上是教程，所以必须省略许多细节。有关此处所涉及主题的更多信息，请参阅手册的相关章节。
## 3.1 连接和断开服务器
要连接到服务器，通常需要在调用mysql时提供MySQL用户名，一般还需要密码。 如果服务器在登录的计算机以外的计算机上运行，则还需要指定主机名。 请从管理员那获取接参数进行连接（即，要使用的主机，用户名和密码）。 一旦知道了正确的参数，就应该能够像这样连接：
```shell
> mysql -h host -u user -p
Enter password:********
```
***host*** 和 ***user*** 分别代表Mysql服务器的主机名和你的Mysql账号用户名，请用你自己的值代替。********代表你的密码，当显示 **Enter password:** 时输入。

如果一切顺利，你可以看到一些介绍信息，以及 **mysql>** 提示符：
```shell
> mysql -h host -u user -p
Enter password: ********
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 25338 to server version: 8.0.17-standard

Type 'help;' or '\h' for help. Type '\c' to clear the buffer.

mysql>
```

**mysql>** 提示符是告诉你mysql已经准备好输入SQL语句了

如果你在运行MySQL的同一台计算机上登录，则可以省略主机，只需使用以下命令：
```shell
> mysql -u user -p
```

当你尝试登录，得到一条类似 **ERROR 2002 (HY000): Can't connect to local MySQL server through socket '/tmp/mysql.sock' (2)** 的提示，这意味着MySQL服务器 守护程序（Unix）或服务（Windows）未运行。请咨询管理员或参阅第2章“安装和升级MySQL”中你操作系统对应的内容。

如果登录过程中遇到其他问题，参看第B.6.2节“使用MySQL程序时的常见错误”。

某些MySQL安装允许用户以匿名（未命名）用户身份连接到本地主机上运行的服务器。 如果你的机器上是这种情况，你应该可以通过调用没有任何选项的mysql连接到该服务器：
```shell
> mysql
```

成功连接后，您可以随时在 **mysql>** 提示符下键入 **QUIT** （或 **\ q** ）来断开连接：
```shell
mysql> QUIT
Bye
```

在Unix上，您也可以通过按Control + D断开连接。

后续章节中大多数示例都假定您已连接到服务器。 它们通过 **mysql>** 提示符表明这一点。
## 3.2 输入查询
## 3.3 创建和使用数据库
## 3.4 获取有关数据库和表的信息
## 3.5 在批处理模式下使用mysql
## 3.6 常见查询示例
## 3.7 在Apache中使用MySQL


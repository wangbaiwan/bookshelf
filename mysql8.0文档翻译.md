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
本章介绍如何获取和安装MySQL。以下是程序的摘要，后面的部分提供了详细信息。如果您计划将现有版本的MySQL升级到较新版本而不是首次安装MySQL，请参见第2.11节“升级MySQL”，了解有关升级过程以及升级前应考虑的问题的信息。

如果您有兴趣从其他数据库系统迁移到MySQL，请参见第A.8节“MySQL 8.0常见问题解答：迁移”，其中包含有关迁移问题的一些常见问题的答案。

MySQL的安装通常遵循以下步骤：

确定MySQL是否在您的平台上运行并受支持。

请注意，并非所有平台都适用于运行MySQL，并且并非所有运行MySQL的平台都由Oracle Corporation正式支持。有关官方支持的平台的信息，请参阅MySQL网站上的https://www.mysql.com/support/supportedplatforms/database.html。

选择要安装的分发版。

有几个版本的MySQL可用，大多数都有几种分发格式。您可以从包含二进制（预编译）程序或源代码的预打包发行版中进行选择。如有疑问，请使用二进制分发。 Oracle还为那些想要查看最新开发和测试新代码的人提供了对MySQL源代码的访问。要确定应使用的版本和分发类型，请参见第2.1.1节“要安装的MySQL版本和分发版本”。

下载要安装的发行版。

有关说明，请参见第2.1.2节“如何获取MySQL”。要验证分发的完整性，请使用第2.1.3节“使用MD5校验和或GnuPG验证程序包完整性”中的说明。

安装发行版。

要从二进制发行版安装MySQL，请使用第2.2节“在Unix / Linux上使用通用二进制文件安装MySQL”中的说明。

要从源代码分发版或当前开发源代码树安装MySQL，请使用第2.9节“从源代码安装MySQL”中的说明。

执行任何必要的安装后设置。

安装MySQL后，请参见第2.10节“安装后设置和测试”以获取有关确保MySQL服务器正常工作的信息。另请参阅第2.10.4节“保护初始MySQL帐户”中提供的信息。本节介绍如何保护初始MySQL root用户帐户，该帐户在分配密码之前没有密码。无论您是使用二进制文件还是源代码分发安装MySQL，本节均适用。

如果要运行MySQL基准脚本脚本，必须提供对MySQL的Perl支持。请参见第2.13节“Perl安装说明”。

有关在不同平台和环境中安装MySQL的说明，请参见平台：

Unix，Linux，FreeBSD

有关使用通用二进制文件（例如，.tar.gz包）在大多数Linux和Unix平台上安装MySQL的说明，请参见第2.2节“使用通用二进制文件在Unix / Linux上安装MySQL”。

有关从源代码发行版或源代码库完全构建MySQL的信息，请参见第2.9节“从源代码安装MySQL”

有关从源代码安装，配置和构建的特定平台帮助，请参阅相应的平台部分：

Linux，包括有关分发特定方法的说明，请参见第2.5节“在Linux上安装MySQL”。

IBM AIX，请参见第2.7节“在Solaris上安装MySQL”。

FreeBSD，请参见第2.8节“在FreeBSD上安装MySQL”。

微软Windows

有关在Microsoft Windows上安装MySQL的说明，请使用MySQL Installer或Zipped二进制文件，请参见第2.3节“在Microsoft Windows上安装MySQL”。

有关管理MySQL实例的信息，请参见第2.3.4节“MySQL通告程序”。

有关使用Microsoft Visual Studio从源代码构建MySQL的详细信息和说明，请参见第2.9节“从源代码安装MySQL”。

OS X.

要在OS X上安装，包括使用二进制包和本机PKG格式，请参见第2.4节“在macOS上安装MySQL”。

有关使用OS X Launch Daemon自动启动和停止MySQL的信息，请参见第2.4.3节“安装和使用MySQL启动守护程序”。

有关MySQL首选项窗格的信息，请参见第2.4.4节“安装和使用MySQL首选项窗格”。
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


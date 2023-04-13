---
title: mysql查看my_cnf位置
slug: /mysql-look-cnf-config.html
url: ''
date: 2022-05-24 14:49:54
tags:
  - mysql
  - config
  - cnf
categories:
  - 经验分享
  - 实用技巧
lastmod: ''
toc: true
keywords: mysql,config,cnf
description: mysql查看my.cnf位置。
isCJKLanguage: true
---
```bash
mysql --help | grep 'Default options' -A 1
```

mysql查看my.cnf位置

参考

[linux shell 管道命令(pipe)使用及与shell重定向区别](https://www.cnblogs.com/chengmo/archive/2010/10/21/1856577.html)
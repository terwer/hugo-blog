---
title: Oracle查看数据库版本等信息
slug: /oracle-view-the-database-version-and-other-information-z1qhr9h.html
url: ''
date: 2022-10-17 14:52:24
tags:
  - 查看
  - 数据库
  - 版本
  - 列表
  - oracle
  - version
  - info
  - 删除
categories:
  - Oracle
  - 数据库
lastmod: ''
toc: true
keywords: 查看,数据库,版本,列表,oracle,version,info,删除
description: 查看数据库版本查看oracle版本selectfromproduct_component_version_查看数据库列表查看数据库列表selectusernameasschema_namefromsysall_usersorderbyusername_删除用户及对应数据删除用户以及下面的objectsdropuserhrcascade_查询当前数据库名selectsys_context(userenvcon_name)fromdual_
isCJKLanguage: true
---
## 查看数据库版本

```sql
-- 查看oracle版本
select * from product_component_version;
```

## 查看数据库列表

```sql
-- 查看数据库列表
select username as schema_name from sys.all_users order by username;
```

## 删除用户及对应数据

```sql
-- 删除用户以及下面的objects
DROP USER hr CASCADE;
```

## 查询当前数据库名

```sql
SELECT SYS_CONTEXT('USERENV','CON_NAME') FROM dual;
```
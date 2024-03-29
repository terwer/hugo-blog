---
title: MyBatis机制介绍与原理
slug: /introduction-and-principle-of-mybatis-mechanism-2x4q8s.html
url: ''
date: 2023-02-22 20:29:49
tags:
  - 插件
  - 功能
  - 组件
  - 可以
  - 扩展
categories: []
lastmod: ''
toc: true
keywords: 插件,功能,组件,可以,扩展
description: mybatis机制介绍与原理插件简介什么是插件插件是一种软件组件可以在另一个软件程序中添加功能或特性。插件通常被设计成可以==随时添加或删除==的而不影响==主程序==的功能。插件可以==扩展==软件程序的功能这让用户可以根据自己的需求定制软件提高工作效率。常见的插件包括浏览器插件音频和视频编辑软件的特效插件图形处理软件的滤镜插件等。mybatis插件介绍mybatis作为一个通用的dao层框架也提供了插件的机制例如_我们可以用插件实现分页分表监控等功能。mybatis在四大组件（==exector===
isCJKLanguage: true
---
## 插件简介

什么是插件

插件是一种软件组件，可以在另一个软件程序中添加功能或特性。插件通常被设计成可以==随时添加或删除==的，而不影响==主程序==的功能。插件可以==扩展==软件程序的功能，这让用户可以根据自己的需求定制软件，提高工作效率。常见的插件包括浏览器插件、音频和视频编辑软件的特效插件、图形处理软件的滤镜插件等。

## MyBatis 插件介绍

MyBatis 作为一个通用的 DAO 层框架，也提供了插件的机制，例如：我们可以用插件实现分页、分表、监控等功能。

MyBatis 在四大组件（==Exector==、==StatmentHandler==、==ParameterHandler==、==ResultSetHandler==）处提供了强大的==插件扩展==机制。

MyBatis 对持久层的操作依赖于这四大核心组件对象。MyBatis 支持通过插件对四大核心组件进行拦截，对 MyBatis 来说，插件就是拦截器，用来增强和信息对象的功能。增强功能底层是借助于 ==JDK 的动态代理==来实现的，也就是说， MyBatis 的四大核心组件本质上都是代理对象。

总之，MyBatis 的四大核心组件和扩展点提供了灵活和可扩展的持久层操作方式，使得开发人员可以根据具体的应用场景来选择适合的方式来操作数据库。同时，插件机制也提供了一种简单、方便的方式来增强 MyBatis 的功能，扩展 MyBatis 的能力。

​![](https://img1.terwer.space/api/public/202303232307565.png)​

## MyBatis 允许拦截的方法

* 执行器 Executor （==update==、==query==、==commit==、==rollback== 等方法）
* Sql 语法构造器 StatementHandler（==prepare==、==parameterize==、==batch==、==updates==、==query== 等方法）
* 参数处理器 ParameterHandler（==getParameterObject==、==setParameters== 方法）
* 结果集处理器 ResultSetHandler（==handlerResultSets==、==handleOutputParameters== 方法）

## MyBatis 插件的原理

参考 [Mybatis基本流程](https://terwer.space/post/mybatis-basic-process-and-configuration-file-analysis.html)

​![image](assets/image-20230325134233-k1byy1x.png)​

​![image](assets/image-20230325154535-ejti1z2.png)​



​![这是个图片锚文本](assets/image-20230325160900-tfvy42x.png "这是个图片标题")​

​![image](assets/image-20230325173641-f9tzx1c.png)​

​![image](assets/image-20230325200855-mvbm00s.png)​
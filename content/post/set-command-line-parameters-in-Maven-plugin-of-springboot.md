---
title: 在SpringBoot的maven插件中设置命令行参数
slug: /set-command-line-parameters-in-Maven-plugin-of-springboot.html
url: ''
date: 2022-05-04 22:59:17
tags:
  - spring
  - boot
  - cli
  - cmd
  - command
categories:
  - 经验分享
  - 实用技巧
lastmod: ''
toc: true
keywords: spring,boot,cli,cmd,command
description: 怎么在SpringBoot的maven插件中设置命令行参数呢?
isCJKLanguage: true
---
怎么在SpringBoot的maven插件中设置命令行参数呢：

 `Spring Boot 2.2+` 的最新设置方式如下：

```bash
mvn spring-boot:run -Dspring-boot.run.arguments="args1 args2"
```

其他方式已经失效。
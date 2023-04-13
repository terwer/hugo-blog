---
title: openEuler2203移除旧的lernel
slug: /open-euler-remove-old-kernel.html
url: ''
date: 2022-05-27 11:11:01
tags:
  - euler
  - open-euler
categories:
  - 开发流程
  - 开发效率
  - 过程改进
lastmod: ''
toc: true
keywords: euler,open-euler
description: openEuler2203移除旧的kernel。
isCJKLanguage: true
---
方法如下：

```bash
dnf remove --oldinstallonly --setopt installonly_limit=2 kernel
```
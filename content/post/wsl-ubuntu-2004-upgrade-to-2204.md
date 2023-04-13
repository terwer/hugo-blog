---
title: 将WSL的2204版本的ununtu滚动升级版本升级到到2204
slug: /wsl-ubuntu-2004-upgrade-to-2204.html
url: ''
date: 2022-05-16 12:22:35
tags:
  - ubuntu
  - upgrade
categories:
  - 开发流程
  - 开发效率
  - 过程改进
lastmod: ''
toc: true
keywords: ubuntu,upgrade
description: 使用vagrant搭建可移植的跨平台的开发环境。
isCJKLanguage: true
---
# 将WSL的2004版本的ununtu滚动升级版本升级到到2204

## 可以直接使用

```bash
do-release-upgrade
```

## 如果没有发布，可使用

```bash
do-release-upgrade -d
```

参考：

[https://askubuntu.com/questions/1403610/22-04-is-suggested-on-ubuntus-website-but-not-in-the-repository](https://askubuntu.com/questions/1403610/22-04-is-suggested-on-ubuntus-website-but-not-in-the-repository)
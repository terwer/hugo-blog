---
title: Linux获取文件名以及后缀名
slug: /linux-gets-the-file-name-and-suffix.html
url: ''
date: 2022-05-11 23:50:25
tags:
  - linux
  - file
  - ext
categories:
  - 经验分享
  - 实用技巧
lastmod: ''
toc: true
keywords: linux,file,ext
description: Linux获取文件名以及后缀名。
isCJKLanguage: true
---
:::tip 文章更新历史

2022/05/11 feat:初稿。

:::

在 Linux 中，利用 bash 获取文件名和后缀还是很常见的。

## 获取后缀名

```bash
ext = ${file: -4}
echo $ext
```

如果文件名是 `file.zip`，运行结果如下：

```bash
.zip
```

## 获取文件名

```bash
name = $(basename "$file" .zip)
echo $name
```

如果文件名是 `file.zip`，运行结果如下：

```bash
file
```
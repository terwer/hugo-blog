---
title: NodeJS创建一个空文件
slug: /nodejs-create-an-empty-file.html
url: ''
date: 2022-04-28 21:32:35
tags:
  - node
  - nodejs
  - file
categories:
  - 经验分享
  - 实用技巧
lastmod: ''
toc: true
keywords: node,nodejs,file
isCJKLanguage: true
---
# NodeJS创建一个空文件

创建一个空文件并返回：

```javascript
var fd = fs.openSync(filepath, 'w');
```

直接创建新文件不用返回值

```javascript
fs.closeSync(fs.openSync(filepath, 'w'));
```
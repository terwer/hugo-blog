---
title: git修改提交的用户名
slug: /git-modify-the-submitted-username.html
url: ''
date: 2022-06-13 10:35:55
tags:
  - git
categories:
  - 经验分享
  - 实用技巧
lastmod: ''
toc: true
keywords: git
isCJKLanguage: true
---
## 第一步，设置新的用户名

```bash
git config user.name terwer
git config user.email youweics@163.com
```

## 第二步，修正用户名

```bash
git commit --amend --reset-author --no-edit
```
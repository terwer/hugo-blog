---
title: MacOS解决npm权限不足问题
slug: /mac-os-solves-the-problem-of-insufficient-npm-permissions-zugbum.html
url: ''
date: 2022-08-24 18:01:34
tags:
  - 错误
  - 提示
  - npm
  - permission
  - deny
categories:
  - 前端开发
lastmod: ''
toc: true
keywords: 错误,提示,npm,permission,deny
description: sudochownr`whoami`~npmsudochownr`whoami`usrlocallibnode_modules错误提示如下_permissiondeniedaccessusrlocallibnode_modules‍
isCJKLanguage: true
---
```bash
sudo chown -R `whoami` ~/.npm
sudo chown -R `whoami` /usr/local/lib/node_modules
```

错误提示如下：

```bash
permission denied, access '/usr/local/lib/node_modules/'
```

‍
---
title: 解决jenkins使用sodo出现的Authentication error in jenkins on using sudo错误
slug: /authentication-error-in-jenkins-using-sudo.html
url: ''
date: 2022-04-28 21:38:15
tags:
  - jenkisn
  - sudo
  - auth
  - error
categories:
  - 经验分享
  - 实用技巧
lastmod: ''
toc: true
keywords: jenkisn,sudo,auth,error
isCJKLanguage: true
---
# 解决jenkins使用sodo出现的Authentication error in jenkins on using sudo错误

修改suduousers，

```bash
sudo su    
visudo -f /etc/sudoers
```

运行jenkins无密码使用sudo

```bash
jenkins ALL= NOPASSWD: ALL
```
---
title: vagrant用户无法访问vboxsf的共享文件夹解决方案
slug: /vagrant-can-not-open-vboxsf-share-forder.html
url: ''
date: 2022-05-13 02:21:47
tags:
  - vagrant
  - virtualbox
categories:
  - 经验分享
  - 实用技巧
lastmod: ''
toc: true
keywords: vagrant,virtualbox
description: vagrant用户无法访问vboxsf的共享文件夹解决方案，将vagrant用户添加到vboxsf用户组即可。
isCJKLanguage: true
---
将vagrant用户添加到vboxsf用户组即可。

```bash
sudo usermod --append --groups vboxsf vagrant
```

然后就可以了，访问共享文件夹：

```bash
cd /mnt/share
ls
```

![image-20220513022415845](https://img1.terwer.space/20220513022416.png)
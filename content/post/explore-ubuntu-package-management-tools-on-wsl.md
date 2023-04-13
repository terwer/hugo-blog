---
title: 探索一下WSL上Ubuntu的包管理工具
slug: /explore-ubuntu-package-management-tools-on-wsl.html
url: ''
date: 2022-05-18 16:14:54
tags:
  - wsl
  - ubuntu
  - package
categories:
  - 开发流程
  - 开发效率
  - 过程改进
lastmod: ''
toc: true
keywords: wsl,ubuntu,package
description: 探索一下WSL上Ubuntu的包管理工具。
isCJKLanguage: true
---
:::warning

此问题尚在研究中，暂时没有完美解决办法，仅供参考。

:::

ubuntu设置某个包不更新

```bash
sudo apt-mark hold mysql-client
```

显示保持不更新的团结列表

```bash
sudo apt-mark showhold
```

取消保留旧版本

```bash
sudo apt-mark unhold htop
```

ubuntu上更好的包管理工具

[https://help.ubuntu.com/stable/ubuntu-help/addremove-install-synaptic.html.en](https://help.ubuntu.com/stable/ubuntu-help/addremove-install-synaptic.html.en)

[https://help.ubuntu.com/community/SynapticHowto](https://help.ubuntu.com/community/SynapticHowto)

```bash
sudo apt-get install synaptic
```

PS：WSL暂时不能用，报错

启动命令

```bash
synaptic-pkexec
```

错误如下：

```bash
Error getting authority: Error initializing authority: Could not connect: No such file or directory
```
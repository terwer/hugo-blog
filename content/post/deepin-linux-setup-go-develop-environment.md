---
title: Deepin搭建GO开发环境
slug: /deepin-linux-setup-go-develop-environment.html
url: ''
date: 2022-07-02 00:33:01
tags:
  - go
  - env
  - deepin
categories:
  - 经验分享
lastmod: ''
toc: true
keywords: go,env,deepin
description: Deepin搭建GO开发环境。
isCJKLanguage: true
---
# Deepin搭建GO开发环境

## 安装

下载

[https://go.dev/dl/](https://go.dev/dl/)

```bash
wget https://go.dev/dl/go1.18.3.linux-amd64.tar.gz
```

解压

```bash
sudo tar -C /usr/local -xzf go1.18.3.linux-amd64.tar.gz
```

设置环境变量

```bash
# GO
export GO_HOME=/usr/local/go
export PATH=$PATH:$GO_HOME/bin
```

验证

```go
go version
```

![image-20220702010433529](https://img1.terwer.space/20220702010522.png)

## GO 国内代理库

```go
go env -w GOPROXY=https://goproxy.cn,direct
```

## 参考

[https://segmentfault.com/a/1190000020293616](https://segmentfault.com/a/1190000020293616)
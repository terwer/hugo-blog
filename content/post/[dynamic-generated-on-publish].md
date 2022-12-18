---
title: Git应用开发详解之Git入门指引
slug: git-application-development-detailed-git-entry-guidelines-ztt2sx
url: post/git-application-development-detailed-git-entry-guidelines-ztt2sx.html
date: '2022-12-17 21:30:05'
tags:
  - 版本
  - 使用
  - 管理
  - 文件
  - 开源
categories: []
lastmod: '2022-12-18 18:24:46'
toc: true
keywords: 版本,使用,管理,文件,开源
description: >-
  git简史官方网站_https_gitscmcom​​linux内核一开始使用bitkeeper来管理和维护代码。年bitkeeper不再免费使用linux开源社区需要一套自己的版本控制系统。自年诞生以来git越来越完善及其适合管理大型项目它有着非线性分支管理系统可以应付各种复杂的项目开发需求。谁在使用git很多开源的非开源项目已经逐步由svn迁移到了git​​cvssvn与git集中式版本控制系统（cvcs）分布式版本控制系统（dvcs）git让编程更有趣gitgithub与gitlabgit是一个版本
isCJKLanguage: true
---



## Git 简史

* 官方网站：[https://git-scm.com/](https://git-scm.com/)

  ​![](https://img1.terwer.space/api/public/202212172144155.png)​

* Linux 内核一开始使用 **BitKeeper** 来管理和维护代码。2005 年，BitKeeper 不再免费使用，Linux 开源社区需要一套自己的版本控制系统。
* 自 **2005** 年诞生以来，Git 越来越完善，及其适合管理大型项目，它有着 **非线性分支管理系统** ，可以应付各种复杂的项目开发需求。

## 谁在使用 Git

* 很多开源的、非开源项目已经逐步由 **SVN** 迁移到了 Git

  ​![](https://img1.terwer.space/api/public/202212181737223.png)​

## CVS、SVN 与 Git

* **集中式** 版本控制系统（CVCS）
* **分布式** 版本控制系统（DVCS）
* **Git** 让编程更有趣

## Git、Github 与 Gitlab

* Git 是一个 **版本控制** 软件
* Github 与 Gitlab 都是用于管理版本的服务端软件
* Github 提供免费与付费服务
* Gitlab 用于 **企业内部管理** Git 版本库，功能上类似于 Github

## Git 设计目标

Git 主要为了完成以下目标而设计
1、快速
2、高效存储
3、简单
4、完全分布
5、满足大规模项目需要
​![](https://img1.terwer.space/api/public/202212181748212.png)​

## 为什么要使用 Git

* **本地** 建立版本库
* 本地版本控制
* 多主机异地协同工作
* **重写** 提交说明
* 有后悔药可以吃
* 更好用的提交列表
* 更好的差异比较
* 更完善的分支系统
* 速度极快

## Git 工作模式

* **版本库初始化**

  个人计算机从版本服务器同步
* **操作**

  * 90% 以上的操作在个人计算机上
  * 添加文件
  * 修改文件
  * 提交变更
  * 查看版本历史等
* **版本库同步**

  将本地修改推送到版本服务器

Git 工作模式图解
​![](https://img1.terwer.space/api/public/202212181810208.png)​

## Git文件存储

Git的文件存储图解  
​![](https://img1.terwer.space/api/public/202212181821096.png)​

‍

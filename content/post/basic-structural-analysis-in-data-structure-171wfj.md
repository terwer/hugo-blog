---
title: 数据结构中的基本结构分析
slug: basic-structural-analysis-in-data-structure-171wfj
url: /post/basic-structural-analysis-in-data-structure-171wfj.html
date: '2022-10-25 00:32:56'
tags:
  - 线性表
  - 元素
  - 结构
  - 存储
  - 称为
  - 数据
  - 数据结构
  - data
  - data-structure
  - structure
categories: []
lastmod: '2022-12-30 22:16:33'
toc: true
keywords: 线性表,元素,结构,存储,称为,数据,数据结构,data,data-structure,structure
description: >-
  数据结构一般将数据结构分为两大类_线性结构和非线性结构。线性数据结构有线性表栈队列串数组和文件_非线性数据结构有树和图。线性表线性表的数据结构是n个数据元素的有限序列_left({{{rm{a}}_}{a_}cdots{a_n}}right)n为线性表的长度（nge）`n=`的表称为空表。数据元素呈线性关系。必存在唯一的一个称为“第一个”的数据元素_必须在唯一的一个称为“最后一个”的元素_除第一个元素外每个元素都有唯一的一个先驱元素除最后一个元素外每个元素都有且只有一个后继元素。所有数据元素在同一个线性表
isCJKLanguage: true
---



## 数据结构

* 一般将数据结构分为两大类：线性结构 和 非线性结构 。

  线性数据结构有 线性表、栈、队列、串、数组和文件；非线性数据结构有 树和图。

### 线性表

* ![](https://img1.terwer.space/api/public/20221025010116.png)

  ```markdown
  * 线性表的数据结构是 n 个数据元素的有限序列：

    $\left( {{{\rm{a}}_1},{a_2} \cdots {a_n}} \right)$
  * n 为线性表的长度（$n \ge 0$）, `n=0` 的表称为空表。
  ```

* 数据元素呈线性关系。必存在唯一的一个称为 “第一个” 的数据元素；必须在唯一的一个称为 “最后一个” 的元素；除第一个元素外，每个元素都有唯一的一个先驱元素，除最后一个元素外，每个元素都有且只有一个后继元素。
* 所有数据元素在同一个线性表中必须是相同的数据类型。
* 线性表按照其存储结构可以分为 顺序表 和 链表 。

  用顺序存储结构存储的线性表称为​ 顺序表 。

  用链式存储结构存储的线性表称为 链表 。
* 将线性表中的数据元素依次存储在某个区域中，所形成的表称为 顺序表 。一维数组就是用顺序方式存储的线性表。

### 链表

* 单向链表

  ![](https://img1.terwer.space/api/public/20221024210834.png)​

  插入

  ![](https://img1.terwer.space/api/public/20221024211701.png)​

  删除

  ![](https://img1.terwer.space/api/public/20221024211843.png)​

* 循环链表

  ![](https://img1.terwer.space/api/public/20221024212032.png)​
* 双向循环链表

  ![](https://img1.terwer.space/api/public/20221024212143.png)​

### 栈

* 栈（Stack）也是一种特殊的线性表，是一种后进先出（LIFO）的结构。
* 栈是限定仅在表尾进行插入和删除运算的线性表，表尾成为栈顶（top），表头成为栈底（bottom）。
* 栈的物理存储可以用顺序存储结构，也可以用链式存储结构。
---
title: Java_SE_第五讲：运算符续
slug: /java_se-1iyv6l.html
url: ''
date: 2022-10-10 20:28:41
tags:
  - 逻辑
  - 结果
  - 运算符
  - 操作数
  - 运算
  - operator
  - continue
categories:
  - JavaSE
  - 后端开发
lastmod: ''
toc: true
keywords: 逻辑,结果,运算符,操作数,运算,operator,continue
description: 关系运算符_大于（=）关系运算的结果是个boolean值。逻辑运算符_重点讲解两个逻辑运算符本身也返回一个boolean值。）逻辑与_使用表示逻辑与是个双目运算符（即有两个操作数的运算符）只有当两个操作数都为真的时候结果才为真_其余情况结果均为假。逻辑与表示的并且的意思。）逻辑或_使用__表示逻辑或也是个双目运算符只有当两个操作数都为假的时候结果才为假_其余情况结果均为真。逻辑或表示或者的意思。关于逻辑运算符的短路特性。）逻辑与_如果第一个操作数为false那么结果肯定就是false所以在这种情况下将不会
isCJKLanguage: true
---
# Java_SE_第五讲：运算符续

1. 关系运算符：大于（>）、小于（<）、等于（==）、不等于（!=）、大于等于（>=）、小于等 于（<=），关系运算的结果是个 boolean 值。
2. 逻辑运算符：重点讲解两个，逻辑运算符本身也返回一个 boolean 值。   

    1） 逻辑与：使用&&表示， 逻辑与是个双目运算符（即有两个操作数的运算符），只有 当两个操作数都为真的时候，结果才为真；其余情况结果均为假。 逻辑与表示的并 且的意思。   

    2） 逻辑或：使用||表示，逻辑或也是个双目运算符，只有当两个操作数都为假的时候， 结果才为假；其余情况结果均为真。 逻辑或表示或者的意思。
3. 关于逻辑运算符的短路特性。   

    1） 逻辑与： 如果第一个操作数为 false，那么结果肯定就是 false ，所以在这种情况下， 将不会执行逻辑与后面的运算了，即发生了短路。   

    2） 逻辑或： 如果第一个操作数为 true，那么结果肯定就是 true ，所在在这种情况下， 将不会执行逻辑或后面的运算了，即发生了短路。
4. 关于变量的自增与自减运算。   

    1） 关于 int b = a++，作用是将 a 的值先赋给 b，然后再让 a  自增 1.   

    2） 关于 int b = ++a，作用是将 a 的值先自增 1，然后将自增后的结果赋给 b。

> 文章更新历史
>
> 2022/05/08 fix:修改备注。
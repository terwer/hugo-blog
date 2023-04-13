---
title: 解决css部分border被圆角切掉之后圆角的边框消失问题
slug: /solve-the-disappearance-of-the-frame-of-the-rounded-corner-after-the-css-part-of-the-border-is-cut-off-by-the-rounded-corner-z5jex4.html
url: ''
date: 2023-03-18 12:58:37
tags:
  - 圆角
  - 切掉
  - css
  - border
  - border-radius
  - overflow
categories:
  - 前端开发
lastmod: ''
toc: true
keywords: 圆角,切掉,css,border,border-radius,overflow
description: 解决css部分border被圆角切掉之后圆角的边框消失问题问题症状大概是这个样子_​​解决办法给当前设置border​和borderradius​属性的元素加_overflow_auto_‍
isCJKLanguage: true
---
## 问题

症状大概是这个样子：  
​![](https://img1.terwer.space/api/public/202303181303568.png)​

## 解决办法

给当前设置 `border`​ 和 `border-radius`​ 属性的元素加：

```css
overflow: auto;
```

‍
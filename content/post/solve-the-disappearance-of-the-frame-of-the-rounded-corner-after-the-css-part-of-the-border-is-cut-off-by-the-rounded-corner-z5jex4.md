---
title: 解决css部分border被圆角切掉之后圆角的边框消失问题
slug: >-
  solve-the-disappearance-of-the-frame-of-the-rounded-corner-after-the-css-part-of-the-border-is-cut-off-by-the-rounded-corner-z5jex4
url: >-
  /post/solve-the-disappearance-of-the-frame-of-the-rounded-corner-after-the-css-part-of-the-border-is-cut-off-by-the-rounded-corner-z5jex4.html
tags:
  - 圆角
  - 切掉
  - css
  - border
  - border-radius
  - overflow
categories: []
lastmod: '2023-03-18 13:58:35'
toc: true
keywords: 圆角,切掉,css,border,border-radius,overflow
description: 问题症状大概是这个样子_​​解决办法给当前设置border和borderradius属性的元素加_overflow_auto_‍
isCJKLanguage: true
---



## 问题

症状大概是这个样子：  
​![](https://img1.terwer.space/api/public/202303181303568.png)​

## 解决办法

给当前设置 border 和 border-[radius](https://so.csdn.net/so/search?q=radius&spm=1001.2101.3001.7020) 属性的元素加：

```css
overflow: auto;
```

‍

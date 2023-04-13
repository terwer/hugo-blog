---
title: npm切换为阿里云国内源码
slug: /npm-switch-to-local-china-source.html
url: ''
date: 2022-07-11 03:07:00
tags:
  - npm
  - pnpm
  - yarn
categories:
  - 前端开发
lastmod: ''
toc: true
keywords: npm,pnpm,yarn
description: npm切换为阿里云国内源码npmnpmconfigsetregistryhttps//registrynpmmirrorcom/pnpmnpminstallgpnpmpnpmconfigsetregistryhttps//registrynpmmirrorcom/pnpmconfigsetelectron_mirrorhttps//npmmirrorcom/mirrors/electron/yarnnpminstallgyarn
isCJKLanguage: true
---
# npm切换为阿里云国内源码

## npm

```bash
npm config set registry https://registry.npmmirror.com/
```

## pnpm

```bash
npm install -g pnpm
pnpm config set registry https://registry.npmmirror.com/
pnpm config set electron_mirror https://npmmirror.com/mirrors/electron/
```

## yarn

```bash
npm install -g yarn
```
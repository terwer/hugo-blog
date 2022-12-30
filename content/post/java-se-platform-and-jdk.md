---
title: Java_SE之Java_SE平台与JDK
slug: java-se-platform-and-jdk
url: /post/java-se-platform-and-jdk.html
date: '2022-09-05 12:20:12'
tags:
  - 平台
  - 版本
  - jdk
  - javase
  - java
  - kotlin
categories: []
lastmod: '2022-12-30 20:14:17'
toc: true
keywords: 平台,版本,jdk,javase,java,kotlin
description: >-
  java平台javase_javaplatformstandardeditionjavase是一个计算平台用于桌面和服务器环境开发和部署可移植代码。javase以前称为javaplatformstandardedition(jse)。javame_javaplatformmicroeditionjavame是一个计算平台用于嵌入式和移动设备（微控制器传感器网关移动电话个人数字助理电视机顶盒打印机）开发和部署可移植代码。javame以前称为javaplatformmicroedition或jme。截至年月日
isCJKLanguage: true
---



## Java 平台

[Java SE](https://en.wikipedia.org/wiki/Java_Platform,_Standard_Edition)：Java Platform, Standard Edition  
Java SE 是一个计算平台，用于桌面和服务器环境开发和部署可移植代码。 Java SE 以前称为 Java 2 Platform, Standard Edition (J2SE)。

[Java ME](https://en.wikipedia.org/wiki/Java_Platform,_Micro_Edition)： Java Platform, Micro Edition  
Java ME 是一个计算平台，用于嵌入式和移动设备（微控制器、传感器、网关、移动电话、个人数字助理、电视机顶盒、打印机）开发和部署可移植代码。 Java ME 以前称为 Java 2 Platform、Micro Edition 或 J2ME。 截至 2006 年 12 月 22 日，Java ME 源代码在 GNU 通用公共许可证下获得许可，并以项目名称 phoneME 发布。

[Java EE](https://zh.wikipedia.org/wiki/Jakarta_EE)：Java Platform Enterprise Edition  
JavaEE 是 Java 平台企业版，之前称为 Java 2 Platform, Enterprise Edition (J2EE)，2018 年 3 月更名为 **Jakarta EE ​**。

## Java 的历史与版本

Java 是由 Sun 公司推出的（2010 年初被 Oracle 公司收购）。

收购价格：74 亿美金

J2SE、J2ME、J2EE

JDK：Java Development Kit （Java 开发必备）

JRE：Java Runtime Environment （Java 执行环境）

JDK 包含了 JRE。

**JDK 版本历史**

Jdk 1.4

jdk 1.5(5.0)：Tiger，老虎

jdk 1.6(6.0)：Mustang，野马

jdk 1.7(7.0): Dolphin，海豚

jdk 1.8(8.0) LTS

java 11 LTS

java 17 LTS

版本历史

[https://zh.wikipedia.org/zh-cn/Java%E7%89%88%E6%9C%AC%E6%AD%B7%E5%8F%B2#JDK_Alpha_%E5%92%8C_Beta](https://zh.wikipedia.org/zh-cn/Java%E7%89%88%E6%9C%AC%E6%AD%B7%E5%8F%B2#JDK_Alpha_%E5%92%8C_Beta)

[https://www.wdbyte.com/java/java-17/](https://www.wdbyte.com/java/java-17/)

[https://www.oracle.com/java/technologies/downloads/archive/](https://www.oracle.com/java/technologies/downloads/archive/)

## Kotlin/JDK 的下载、安装与运行

### 下载 Kotlin

[https://kotlinlang.org/docs/command-line.html](https://kotlinlang.org/docs/command-line.html)

### 下载 JDK

[https://www.oracle.com/java/technologies/downloads/archive/](https://www.oracle.com/java/technologies/downloads/archive/)

目前兼容性和使用最广泛的是 JDK8：

[https://www.oracle.com/java/technologies/javase/javase8u211-later-archive-downloads.html](https://www.oracle.com/java/technologies/javase/javase8u211-later-archive-downloads.html)

### 安装 Kotlin/JDK

安装直接根据官网提示安装即可，主要是设置环境变量。

* Kotlin 环境变量

  Mac 直接用 Homebrew 安装

  ```bash
  brew update
  brew install kotlin
  ```

  安装日志如下：

  ```
  ==> Downloading https://mirrors.ustc.edu.cn/homebrew-bottles/openjdk-18.0.1.monterey.bottle.tar.gz
  ######################################################################## 100.0%
  ==> Downloading https://mirrors.ustc.edu.cn/homebrew-bottles/kotlin-1.6.21.all.bottle.tar.gz
  ######################################################################## 100.0%
  ==> Installing dependencies for kotlin: openjdk
  ==> Installing kotlin dependency: openjdk
  ==> Pouring openjdk-18.0.1.monterey.bottle.tar.gz
  🍺  /usr/local/Cellar/openjdk/18.0.1: 641 files, 307.7MB
  ==> Installing kotlin
  ==> Pouring kotlin-1.6.21.all.bottle.tar.gz
  🍺  /usr/local/Cellar/kotlin/1.6.21: 115 files, 75.9MB
  ==> Running `brew cleanup kotlin`...
  Disable this behaviour by setting HOMEBREW_NO_INSTALL_CLEANUP.
  Hide these hints with HOMEBREW_NO_ENV_HINTS (see `man brew`).
  ```

  输入 `kotlin -version` ，可以检测环境变量：

  ```bash
  ➜  ~ kotlin -version
  Kotlin version 1.6.21-release-334 (JRE 11.0.12+8-LTS-237)
  ```
* Java 环境变量

  设定环境变量（可以是用户变量，也可以是系统变量），指向 JDK 安装目录中的 bin 目录<br />通过运行，输入 cmd 打开命令行窗口，输入 `java –version` ，显示出 Java 版本信息

  ```bash
  ➜  ~ java -version
  java version "11.0.12" 2021-07-20 LTS
  Java(TM) SE Runtime Environment 18.9 (build 11.0.12+8-LTS-237)
  Java HotSpot(TM) 64-Bit Server VM 18.9 (build 11.0.12+8-LTS-237, mixed mode)
  ```

### 运行第一个 Kotlin/Java 程序

接下来就可以编写 Kotlin/Java 程序了。

可以直接使用 windows 记事本来编写 Kotlin/Java 程序，也可以使用 Editplus，UltraEdit 等高级文本编辑工具编写 Java 程序，还可以使用专业的 IDE（Integrated Development Environment）编写。

#### 使用 InteliJ IDEA IDE 实现

[https://kotlinlang.org/docs/getting-started.html](https://kotlinlang.org/docs/getting-started.html)

#### 记事本实现

使用记事本实现一个 Hello World 的 Kotlin 或者 Java 程序。

Mac 可以用以下命令创建一个 Kotlin 或者 java 文件：

<div>
<code-group>
</div>

<div>
<code-block title="Kotlin" active>
</div>

```bash
cd ~
vim hello.kt
```

<div>
</code-block>
</div>

<div>
<code-block title="Java">
</div>

```bash
cd ~
vim HelloWorld.java
```

<div>
</code-block>
</div>

<div>
</code-group>
</div>

然后写上如下代码：

<div>
<code-group>
</div>

<div>
<code-block title="Kotlin" active>
</div>

```kotlin
fun main(){
  println("Hello, World!")
}
```

<div>
</code-block>
</div>

<div>
<code-block title="Java">
</div>

```java
class HelloWorld{
  public static void main(String[] args){
    System.out.println("Hello World!");
  }
}
```

<div>
</code-block>
</div>

<div>
</code-group>
</div>

所有的 Kotlin 代码，其后缀都是以 kt 结尾；所有的 Java 代码，其后缀都是以 java 结尾。

Kotlin/Java 程序的执行过程分为两步：

编译

执行

Class 文件是字节码文件，程序最终执行的就是这个字节码（bytecode）文件。

* Kotlin 编译

  编译命令：`kotlinc hello.kt`

  执行命令：`kotlin HelloKt`

  ![image-20220509000006471](https://img1.terwer.space/20220509000006.png)​
* Java 编译

  编译命令：`javac HelloWorld.java`

  执行命令：`java HelloWorld`（注意，Test 后面没有.class）

  ![image-20220501192947243](https://img1.terwer.space/image-20220501192947243.png)​

### Java 跨平台与 Java 虚拟机

Java 是跨平台的语言，真正执行的不是二进制代码，而是字节码。

JVM（Java Virtual Machine，Java 虚拟机）

Java 是跨平台的，而 JVM 不是跨平台的（JVM 是由 C 语言编写的）

Java 之所以能够做到跨平台，本质原因在于 JVM 不是跨平台的。

> 文章更新历史
>
> 2022/05/08 feat:新增 Kotlin 语言支持。
>
> 2022/05/01 feat:添加最新 JDK 版本信息。
>
> 2011/10/22 feat:初稿。

‍

---
date: 2019-10-11
keywords: "kt,.kt,kotlin 文件格式,如何打开 kotlin 文件,如何运行 kotlin 文件,.kt 文件格式,kt 文件,kotlin 文件扩展名,.kt 扩展名,kotlin vs java"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "KT 文件格式"
linktitle: "KT"
description: "了解可创建和打开 KT 文件的 KT 文件格式和 API。"
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## 什么是一 .kt 文件？ ##

用 Kotlin 编写的源代码以 .kt 扩展名保存，通常称为 **Kotlin 文件扩展名**。 Kotlin 是由 JetBrains 开发的通用跨平台编程语言，可与 [Java](/zh/programming/java/) 完全互操作。 Kotlin 商标受 Kotlin 基金会保护。

Kotlin 于 2019 年 5 月 7 日被 Google 宣布为 Android 应用程序开发的首选编程语言。Android Studio 3.0 于 2017 年 10 月开始支持 Kotlin 作为 Android 应用程序开发的替代方案。

## Kotlin KT 文件格式简史##

Kotlin 于 2011 年 7 月由 JetBrains 推出，作为一种新的 JVM 编程语言。 JetBrains 的负责人 Dmitry Jemerov 表示，除了 Scala 之外，大多数语言都缺少他们正在寻找的功能，但 Scala 的编译速度慢是一个缺点。 Kotlin 的主要目标之一是像 Java 一样快速编译。 Kotlin 项目于 2012 年 2 月在 Apache 2 许可下开源。

Kotlin 1.0 版于 2015 年 2 月 15 日发布。Android 在 Google I/O 2017 上宣布对 Android 上的 Kotlin 提供一流的支持。Kotlin 1.2 于 2017 年 11 月 28 日发布，能够在 JVM 和 JavaScript 平台之间共享代码。 Kotlin 1.3 于 2018 年 10 月 29 日发布，支持异步编程。 Google 于 2019 年 5 月 7 日宣布 Kotlin 成为 Android 应用程序开发的首选编程语言。Kotlin 1.4 于 2020 年 8 月发布，稍作改动以支持与 Swift/Objective-C 的互操作性。

## Kotlin 语法 ##

Kotlin 被设计为比 Java 更好，但仍可与 Java 代码互操作，以允许从 Java 逐步迁移到 Kotlin。

* Kotlin 中分号是可选的。一个新行就足以表明语句的结束。
* Kotlin 支持两种类型的变量，只读的，由 *val* 关键字定义，和可变的，由 *var* 关键字定义。
* 默认情况下，类是私有的和最终的。要从类派生，必须使用 *open* 关键字声明基类。
* Kotlin 还支持过程式编程。
* Kotlin 程序的入口点是类似于 Java、C# 等的“main"函数。

### 语法示例###

以下是 Kotlin 语法的示例。

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

在上面的代码中，**fun** 关键字定义了名为 main 的函数。在函数内部，使用 **val** 关键字声明了一个只读变量“audience"。通过使用 **println** 方法，“来自 Kotlin 的 Hello World"被打印在控制台上。变量 Audience 的值被注入到带有 **$** 符号的字符串中。

## Kotlin 与 Java
Kotlin 是编写 Android 应用程序的官方语言，提供许多高级功能，但许多专业的 Java 开发人员仍然没有表现出切换到 Kotlin 的兴趣。他们认为只用 Java 就可以完成所有工作。因此，以下是可能说服 Java 开发人员切换的两种技术之间的比较：

|参数 |爪哇 |科特林 |
|--------------------|-----------|---------------- -|
|单例对象 | √ | √ |
|通配符类型 | √ | Χ |
|编译 |字节码 |虚拟机 |
| Lambda 表达式 | Χ | √ |
|不变数组 | Χ | √ |
|非私有领域 | √ | Χ |
|智能铸件 | Χ | √ |
|零安全 | Χ | √ |
|静态成员 | √ | Χ |

## 参考 ＃＃

- [Kotlin (编程语言) - 维基百科](https://en.wikipedia.org/wiki/Kotlin_(programming_language))


---
date: 2019-10-11
keywords: "java,.java,java文件格式,如何打开java文件,如何运行java文件,java文件,java示例代码"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "Java 文件格式"
linktitle: "爪哇"
description: "了解 Java 文件格式和可以创建和打开 Java 文件的 API。"
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-07
---

## 什么是 Java 文件？ ##
包含 Java 源代码并以 .java 文件扩展名保存的文件称为 Java 文件。 Java 是用于开发游戏、移动、Web 和桌面应用程序的最广泛使用的技术之一。由于 Java 独立于平台，因此可以在 Windows、Mac、Linux、Raspberry Pi 等平台上完美运行。Java 与 C# 和 C++ 非常相似，因此更容易在这些语言之间切换。

## 历史简介 ＃＃

Java 项目由 James Gosling、Mike Sheridan 和 Patrick Naughton 于 1991 年 6 月发起。 Java 最初被命名为 Oak。它后来更名为 Green，最后更名为 Java。 James Gosling 使用类似于 C/C++ 的语法设计了 Java。 Java 的第一个公共版本于 1996 年由 Sun Microsystems 发布。它可以在所有使 Java 迅速流行的流行系统上运行。随着 1998 年 12 月 Java 2 的发布，为不同类型的平台构建了多种配置。版本如下

- J2EE (Java EE)：用于企业解决方案
- J2ME (Java ME)：用于移动应用程序
- J2SE (Java SE)：用于桌面应用程序

2006 年 11 月 19 日，Java 虚拟机 (JVM) 由 Sun 作为免费和开源软件发布。在甲骨文公司于 2009 年至 2010 年收购 Sun Microsystems 后，James Gosling 于 2010 年 4 月 2 日从甲骨文辞职。

## 如何运行/执行 Java 代码##

要执行 Java 代码，首先需要对其进行编译。为此，需要 Java SDK。 Java SDK 将 Java 代码编译为字节码类文件。有像 Eclipse 和 IntelliJ Idea 这样的 IDE，它们通过提供代码完成和易于使用的界面来编译和执行 Java 代码，从而使处理 Java 文件变得更加容易。

## Java 文件格式 ##

Java 的语法深受 C 和 C++ 的影响，但与 C++ 不同的是，Java 几乎完全是作为一种面向对象的语言而构建的。在 Java 中，所有代码都写在类中，每个数据项都是一个对象。与 C++ 相比，Java 不支持运算符重载或多重继承。

### Java 示例代码###

以下是 Java 语法的示例。

```java
/*
The example code prints
Hello World from Java to the console.
*/
    public class ExampleApp {
        public static void main(String[] args) {
            System.out.println("Hello World from Java"); // Prints the string to the console.
        }
    }
```
在上面的代码中，**public** 关键字表示访问修饰符。它声明这个类可以被类层次结构之外的类访问。访问修饰符也可以是**protected**（可以在同一个包中访问）或**private**（方法只能被同一个类访问）。方法前面的**static**表示可以在没有特定类实例的情况下调用该方法。 **void** 表示该方法不会返回任何内容。将字符串打印到控制台。使用 System.out.println 命令。在这个命令中，*System* 类有一个静态字段 *out*，它是包含 *println* 方法的 *PrintStream* 类的一个实例。

Java 文件的文件名应与类名相同。因此，示例代码的 Java 文件将命名为 *ExampleApp.java*。

## 参考 ＃＃

- [Java (编程语言) - 维基百科](https://en.wikipedia.org/wiki/Java_(programming_language))


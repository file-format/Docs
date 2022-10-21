---
date: 2022-05-09
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: "PYD 文件格式 - Python 动态模块"
linktitle: "PYD"
description: "了解 PYD 文件格式和可创建和打开 PYD 文件的 API。"
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## 什么是一 .pyd 文件？

PYD 文件是用 Python 编写的动态链接库，可以在运行时由其他 Python 代码运行。它包含一个或多个 Python 模块，便于代码重用，并为编写应用程序提供模块架构。可以使用 .pyd 扩展名创建和保存 PYD 文件，例如 helloworld.pyd。应用程序开发人员可以使用 import 语句将 PYD 模块包含在他们的应用程序中。 PYD 文件可以使用适用于 Windows、Mac 和 Linux 操作系统的 Python Software Foundation Python 打开。

## PYD 文件格式 - 更多信息

PYD 文件是用 Python 编程语言编写的，是通过编译 Python 代码生成的。

## PY 和 PYD 文件格式之间的区别

[PY](/zh/programming/py/) 文件包含按原样执行的源代码，不能作为可重用代码包含在其他 Python 应用程序中。但是，PYD 文件是要在 Windows 操作系统上使用的动态链接库。

## 如何创建 PYD 文件？

可以通过创建一个名称为 exmaple.pyd 的模块来创建 PYD 文件。该模块将包含一个或多个函数形式的所有功能，例如 PyMod_example()。当程序包含这个库并调用它时，可以通过导入模块来完成，函数 PyMod_example() 将运行。

## 参考 ＃＃

* [在 C/C++ 中创建 Python 扩展](https://sebsauvage.net/python/mingw.html)
* [Python (编程语言) - 维基百科](https://en.wikipedia.org/wiki/Python_(programming_language))


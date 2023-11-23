---
date: 2022-05-09
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: "PYI 文件格式 - Python 接口定义"
linktitle: "PYI"
description: "了解 PYI 文件格式和可创建和打开 PYI 文件的 API。"
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## 什么是一 .pyi 文件？

PYI 文件是一个 Python 接口定义文件，其中包含用于实现接口的代码存根参考。每个 Python 模块都表示为一个 .pyi 存根，它是一个普通的 Python 文件，但具有空方法。 PYI 文件的语法与常规 Python 模块的语法相同。空方法的实现留给最终用户实现模块编写的特定目标。这就是 PYI 文件与包含程序完整实现的 [PY](/zh/programming/py/) 文件不同的地方。 PYI 文件可以使用 Notepad、Notepad++、Microsoft Visual Studio Code 和 JetBrains PyCharm 等文本编辑器打开。

## PYI 文件格式

PYI 文件保存为可以使用任何文本编辑器打开的纯文本文件。 Python 是一种解释器语言，在执行代码时会执行类型检查。在这种情况下，PYI 文件有助于开发人员在编写应用程序时手动定义和检查模块的类型。

## 参考 ＃＃

* [接口 - Java](https://en.wikipedia.org/wiki/Interface_(Java))
* [PYM 解释器](https://github.com/interpreters/pym)


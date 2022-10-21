---
date: 2022-05-09
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: "PYM 文件格式 - PYM 宏预处理器文件"
linktitle: "PYM"
description: "了解 PYM 文件格式和可以创建和打开 PYM 文件的 API。"
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## 什么是一 .pym 文件？

PYM 文件是基于 Python 编程语言的宏预处理器文件。它由 VRVis Research 开发并存储宏快捷方式。当 Python 解释器的预处理阶段解释 PYM 文件时，这些快捷方式被扩展为它们的全文替换。此外，可以由宏预处理器执行的第三个可选操作是文件包含。 PYM 文件可以在 Linux 上的 Notepad、Notepad++、Apple TextEdit 和 VI 等文本编辑器中打开。

## PYM 文件格式

PYM 文件以纯文本文件形式保存到光盘。 PYM 文件还可以使用 `#include` 指令包含其他文件。

### PYM 语法

PYM 语句包含在 ""#begin python 和 "#end python" 标记之间，如下所示。

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### PYM 宏扩展

PYM 宏扩展由两个序列表示，即<[ 和]>。这些是特殊的 html 标签，可以出现在一行中的任何位置。一个小 PYM 示例如下。

```
#begin python
TITLE = "My Web page"
def EXP(e): return str(e)
#end python
<head>
<title><[TITLE]></title>
</head>
<body>
<h4><[TITLE]></h4>
<p>The value of 2 raised to the 4th power is <[EXP(2**4)]>.</p>
</body>
```

通过 PYM 运行它的输出如下：

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## 参考 ＃＃

* [PYM - 基于 Python 的宏预处理器](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [PYM 解释器](https://github.com/interpreters/pym)


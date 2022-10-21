---
date: 2019-10-11
keywords: "py, python, .py, py文件格式, 如何打开py文件, 如何运行py文件, 如何运行python文件, 如何运行python"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "PY 文件格式"
linktitle: "PY"
description: "了解 PY 文件格式和可创建和打开 PY 文件的 API。"
menu:
  docs:
    parent: "programming"
lastmod: 2020-25-11
---

## 什么是一 .py 文件？ ##

扩展名为 .py 的文件包含 Python 源代码。 Python 语言如今已成为非常著名的语言。它可用于系统脚本、网络和软件开发以及数学。 Python支持跨平台兼容；意味着用 Python 开发的应用程序可以在不同的平台上运行，如 Windows、MAC、Linux、Raspberry Pi 等。Python 提供了一种类似于英语的简单易读的语法。开发者只需编写几行 Python 代码就可以编写出合理的软件应用程序。由于 Python 在解释器系统上运行，因此代码可以在编写后立即执行，这使得它非常适合原型设计。

## 历史简介 ＃＃

Python 由 Guido van Rossum 在 1980 年代后期构想为 ABC 编程语言的继承者。它的实施始于 1989 年 12 月，由 Van Rossum 作为唯一的首席开发人员。他一直致力于 Python 直到 2018 年 7 月 12 日。2019 年 1 月，活跃的 Python 核心开发人员选出了一个由 Nick Coghlan、Brett Cannon、Carol Willing、Barry Warsaw 和 Van Rossum 组成的五人“指导委员会"来领导该项目。

### 版本###

- Python 2.0 于 2000 年 10 月 16 日发布。
- Python 3.0 于 2008 年 12 月 3 日发布。

## 如何运行py文件##

要检查安装的 Python 版本，可以使用以下命令：

```cmd
python --version
```

这将在控制台上输出版本，如

```cmd
Python 3.7.4
```

如果您的机器上没有安装 Python，您可以访问 [python.org](https://www.python.org/) 并为您的相关操作系统下载并安装 Python。

要执行 Python 脚本，可以使用以下命令：

```cmd
python helloworld.py
```

*helloworld.py* 是一个脚本文件，包含以下代码

```py
print("Hello World from Python")
```

这将在控制台窗口上打印以下内容。

```cmd
Hello World from Python
```

注意：如果您使用 IDE，它们会在屏幕上提供按钮或不同的键盘快捷键来运行 Python。例如，PyCharm 中的编辑器在装订线中显示了一个播放按钮，可让您执行 Python 脚本。

## PY 文件格式##

Python 是为可读性而设计的，与英语和数学有相似之处。 Python 使用新行来指示完整的命令，而不是其他语言中使用的分号或括号。对于作用域、循环和函数，Python 依赖于缩进和空格，而不是其他语言中使用的花括号。

＃＃＃ 句法 ＃＃＃

以下是 Python 语法的示例。

```py
print("Hello World")

#Variables
name = "John"
age = 25
print(name)
print(age)

#While Loop
i = 1
while i < 3:
  print(i)
  i += 1
  
#For Loop
names = ["John", "Harry", "Tom"]
for name in names:
  print(name)
```

## 参考 ＃＃

- [Python (编程语言) - 维基百科](https://en.wikipedia.org/wiki/Python_(programming_language))


{
  "date" : "2022-03-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EX 文件格式 - Euphoria 源代码文件",
  "description":"了解 EX 文件格式和可以创建和打开 EX 文件的 API。",
  "linktitle" : "EX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-15"
}

## 什么是 .EX 文件？

EX 文件是一个源代码文件，其中包含使用 Euphoria 编程语言开发的应用程序的源代码。 Euphoria 是一种过程式编程语言，它相信编程的简单性，而不是复杂的编程语言。 Euphoria 开发的应用程序可以包含多个 EX 文件，但单个 EX 文件也可以包含程序的完整源代码。

可以**打开 EX 文件**的应用程序包括 openEuphoria Euphoria、Microsoft Notepad、Notepad++ 和 Atom。

## EX 文件格式简史

EX 文件格式的发展和存在与 Robert Craig 创建的 Euphoria 编程语言的发展息息相关。它最初是为 MS-DOS 发布的。随着版本 3 的发布，它在 2006 年成为开源软件。它的开发由管理和开发该项目的 **openEuphoria group** 接管。它的第 4 版于 2010 年 12 月发布，可用于 Windows、Linux、macOS 和三种 BSD 风格。

Euphoria 最初是用 **[C](/zh/programming/c/)** 编程语言编写的。后来，Euphoria 解释器被分成了两部分：

* `前端解析器` - 用 Euphoria 编写，与 Euphoria-to-C 转换器和 Binder 一起使用。
* `Back-end` - 用 C 编程语言编写的运行时库。

## EX 文件格式 - 更多信息

EX 文件存储为纯文本文件，并包含用 Euphoria 编程语言编写的程序的源代码。这些文件可以在任何文本编辑器中打开。

## 参考 ＃＃

* [OpenEuphoria 论坛](https://openeuphoria.org/forum/index.wc)

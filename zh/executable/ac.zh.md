{
  "date" : "2023-01-11",
  "keywords" :["ac 文件", "什么是 aci 文件", "文件", "如何打开 ac 文件", "ac 文件扩展名","扩展名"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解可以创建和打开 ACCDB 文件的 AC 文件格式和 API。”,
  "title" :"AC 文件格式 - Autoconf 脚本文件”，
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## 什么是 .ac 文件？

AC 文件是 Autoconf 脚本文件。 **Autoconf** 是一个可扩展的 M4 宏包，可生成 shell 脚本以自动配置软件源代码包。这些脚本可以使包适应多种类 UNIX 系统，而无需用户手动干预。 Autoconf 从一个模板文件中为一个包创建一个配置脚本，该模板文件以 M4 宏调用的形式列出了该包可以使用的操作系统特性。

使用 Autoconf 生成配置脚本需要 GNU M4。在配置 Autoconf 之前，你应该安装 GNU M4（至少版本 1.4.6，尽管推荐 1.4.13 或更高版本），以便 Autoconf 的配置脚本可以找到它。 Autoconf 生成的配置脚本是独立的，因此它们的用户不需要拥有 Autoconf（或 GNU M4）。

## 如何打开 .ac 文件？

AC 代表自动配置。它是由 GNU Autoconf 生成的脚本，通过测试包中的必要功能，使软件源代码能够适应各种类似 Posix 的系统。该脚本称为 AC 文件。

## 主要的 Autotools 组件

了解 GNU 自动工具（`automake`、`autoconf` 等）在使用 ebuild 时会很有用：

Autotools 是相关包的集合，当它们一起使用时，可以消除创建可移植软件所涉及的大部分困难。这些工具连同一些相对简单的上游提供的输入文件，用于为包创建构建系统。

**主要 autotools 组件如何组合在一起的基本概述。**

![A basic overview of how the main autotools components fit together](https://devmanual.gentoo.org/general-concepts/autotools/diagram.png "A basic overview of how the main autotools components fit together")

在一个简单的设置中：

- `autoconf` 程序从 `configure.in` 或 `configure.ac` 生成一个配置脚本。
- `automake` 程序从 Makefile.am 生成一个 Makefile.in。
- 运行 `configure` 脚本以从 Makefile.in 文件生成一个或多个 Makefile 文件。
- `make` 程序使用 Makefile 来编译程序。

## 参考
* [Autoconf 软件](https://www.gnu.org/software/autoconf/)
* [Autotools 基础知识](https://devmanual.gentoo.org/general-concepts/autotools/index.html)



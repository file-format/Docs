{
  "date" : "2022-04-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IN 文件格式 - Autoconf 输入文件",
  "description":"了解 IN 文件格式和可以创建和打开 IN 文件的 API。",
  "linktitle" : "IN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-26"
}

## 什么是.IN 文件？

IN 文件是 GNU Autoconf 在构建应用程序时使用的输入文件。运行配置过程时，Autoconf 脚本（.AC 文件）可能会引用一个或多个“.in"或“.h.in"文件。 IN 文件定义在程序安装期间引用的变量，例如应用程序的版本号和发布日期。 IN 文件还可用于确定特定安装中是否存在功能。 Notepad 和 Notepad++ 等应用程序可用于打开和编辑 IN 文件。

## IN 文件格式 - 更多信息

Autoconf 是 GNU 构建系统的一个组件，它为各种平台生成应用程序的自定义构建。它是几个 GNU 构建工具之一。其他工具包括 Automake、Gnulib 和 Libtool。无需手动用户干预，这些脚本可以使包适应各种类 UNIX 系统。 Autoconf 从一个模板文件生成一个包配置脚本，其中列出了包可以使用的操作系统特性，以 M4 宏调用的形式

## 参考

* [自动配置](https://www.gnu.org/software/autoconf/)


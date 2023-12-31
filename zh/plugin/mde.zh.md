{
  "date" : "2023-12-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MDE 文件 - 什么是 MDE 文件以及如何打开它?",
  "description":"了解 MDE 文件格式以及可创建和打开 MDE 文件的 API.",
  "linktitle" : "MDE",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-zh-mde"
    }
  },
  "lastmod" : "2023-12-03"
}

## 什么是 MDE 文件？

.MDE 文件是 Access 数据库（.mdb 或 .accdb）的编译版本。 当您将 Access 数据库编译为 .MDE 文件时，将无法再使用标准 Access 设计工具对其进行编辑。 创建 .MDE 文件的主要目的是在不暴露原始源代码的情况下分发数据库应用程序。

## MDE 文件格式

MDE 文件是通过编译 VBA 代码、表单、报告和其他对象创建的。 这会创建 MDE 二进制文件格式。 生成的 .MDE 文件可以分发给可以运行应用程序但无法修改设计或查看原始代码的用户。 MDE 文件实际上是[.MDA 文件](/database/mda/) 的编译版本。 分发 .MDE 文件可以防止用户访问或修改源代码，从而帮助保护知识产权。 随着代码的编译和优化，它还可以提高性能。

＃＃ 参考

* [访问规范](https://support.microsoft.com/en-us/office/access-specations-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [非官方 MDB 指南](http://jabakobob.net/mdb/)
{
  "date" : "2021-07-25",
  "keywords":["man","file", "extension", "type", "format", "Unix Manual"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAN - Unix 手册",
  "description":"了解 FODT 文件格式和可以创建和打开 MAN 文件的 API。",
  "linktitle" : "MAN",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-25"
}

## 什么是一 .man 文件？

带有 .man 扩展名的文件代表手册页，它是软件文档形式的 Unix 编程用户手册。它由 Unix 中包含的“Man"实用程序使用，用于查看文档。软件文档包含部分和页面中的信息，这些信息可以通过命令终端使用 Man 实用程序通过发出命令进行检索。作为文档的软拷贝在计算机中可用，它不需要任何打印副本或互联网连接即可访问它。

## Unix 手册 Man 文件格式 - 更多信息

手册页以纯文本格式存储，可以在任何文本编辑器中创建和打开以进行查看或编辑。在 UNIX 中，通过从终端发出命令来检索手册页中的信息，其中包括对手册中章节和页码的引用。

### 部分和页面

Unix man 是系统手册，其中命令的每个页面参数指的是程序、实用程序或函数的名称。如果提供了部分信息，该命令将在该特定部分中搜索页面。但是，默认行为是在所有部分中搜索页面并显示第一页，无论它是否存在于多个部分中。

### 部分编号

以下是有关手册章节编号的信息，然后是它们包含的页面类型。

|章节编号|页面类型|
---|---|
|1|可执行程序或 shell 命令|
|2|系统调用（内核提供的函数）|
|3|库调用（程序库中的函数）|
|4|特殊文件（通常在 /dev 中）|
|5|文件格式和约定，例如 /etc/passwd|
|6|游戏|
|7|杂项（包括宏包和约定），例如 man(7)、groff(7)|
|8|系统管理命令（通常只用于 root）|
|9|内核例程[非标准]|

## 示例 - 如何阅读 MAN 页面？

这是一个如何使用 Man 命令检索有关 MkDir 命令的信息的示例。

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## 参考

* [OpenDocument 技术规范 - 维基百科提供](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)
* [man(1) — Linux 手册页](https://man7.org/linux/man-pages/man1/man.1.html)


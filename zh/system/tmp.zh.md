{
  "date" : "2021-07-15",
  "keywords" :["TMP","扩展名","文件","格式","系统","TMP 文件","TMP 文件","TMP 文件","临时文件","应用程序","程序"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TMP - 临时文件格式",
  "description":"了解 TMP 文件格式和可以创建和打开 TMP 文件的 API。",
  "linktitle" : "TMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## 什么是一 .tmp 文件？ ##

TMP 文件是指由软件程序生成的临时备份、存储或其他文件系统。它偶尔会被创建为不可见的文件，并且在程序退出时经常被销毁。 TMP 文件还可用于在构建新文件时临时存储信息。

## TMP 文件格式##

TMP 文件通常由原始数据组成，这些原始数据用作材料从一种风格到另一种风格的转换过程中的一个阶段。 Microsoft Word 和 Apple Safari 是两个可以生成和使用 TMP 文件格式的应用程序。

理论上，生成的 TMP 文件应该在程序关闭或机器关闭时自动删除。在实践中，情况并非总是如此。因此，在浏览程序文档时，您可能会遇到系统或任何其他软件未主动使用的临时文件。

###辅助记忆###

虚拟内存用于操作系统，但是，使用大量信息的程序可能需要制作临时文档。

###进程间通信###

大多数操作系统提供在程序之间传递数据的原语，例如管道、套接字或主内存，但最简单的方法是将文件传输到临时文件并通知接收应用程序临时文件的位置。


## 技术规格##

获得独特的临时文档名称通常由操作系统和软件程序提供。
可以使用 mkstemp 或 tmpfile 库函数在 POSIX 系统上安全地生成临时文件。一些系统包括以前的 POSIX（已经消失）mktemp 应用程序。这些文件通常在 Unix 平台上的常规临时目录中的 /TMP 或 Windows 机器上的 %TEMP%（它特定于登录）中找到。

当程序停止或文档关闭时，使用 tmpfile 生成的临时文件会被自动删除。 GetTempFileName (Windows) 或 tmpnam (POSIX) 可用于创建比创建它的程序持续时间更长的临时文件名。

## 参考 ＃＃

* [TMP - Wikipedia](https://en.wikipedia.org/wiki/Temporary_file)

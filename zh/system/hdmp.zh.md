{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDMP 文件 - Windows 堆转储文件格式",
  "description":"了解 HDMP 文件格式和可以创建和打开 HDMP 文件的 API。",
  "linktitle" : "HDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## 什么是一 .hdmp 文件？

当应用程序或程序由于错误而崩溃时，HDMP 文件是未压缩的内存转储。它仅由 Windows XP/Vista 创建，包含应用程序崩溃时的状态转储。与为报告目的而压缩的 Minidump [MDMP](/zh/system/mdmp/) 文件相比，未压缩的 HDMP 文件在磁盘上占用更多空间。

可用于**打开**或分析 HDMP 文件的应用程序包括带有 Windows 调试工具的 Microsoft Visual Studio。

## HDMP 文件格式

HDMP 文件以二进制文件的形式存储到光盘中，如果在没有适当应用程序的情况下打开，则不会提供任何好处。这些包含发生错误时记录的相关系统数据。

### HDMP 和 MDMP 文件格式之间的区别

HDMP 是未压缩的内存转储文件。相比之下，MDMP 是经过压缩以减小文件大小并发送给 Microsoft 以报告问题的小型转储文件。

## 参考 ＃＃

* [DMP - 微软](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)


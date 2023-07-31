{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SY_ 文件格式 - 压缩的 SYS 文件",
  "description":"了解 SY_ 文件格式和可以创建和打开 SY_ 文件的 API。",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## 什么是 SY_ 文件？

SY_ 文件是压缩的 .sys 文件，软件安装程序使用它来减小安装程序中打包的安装文件的大小。这减小了安装程序的整体大小。 SY_ 文件可以使用扩展一个或多个压缩文件的 Microsoft Expand 命令行实用程序进行扩展。

## SY_ 文件格式 - 更多信息

SY_ 文件作为压缩的二进制文件保存到光盘中。但是，它们的内部文件格式不公开。 Microsoft Expand 命令行实用程序可以使用以下命令行之一来扩展 SY_ 文件。

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
展开后，SY_ 文件将转换为 [SYS](https://docs.fileformat.com/system/sys/) 文件。

SY_ 文件类似于 EX_ 和 DL_ 文件。

## 参考

* [StuffIt - 来自维基百科](https://en.wikipedia.org/wiki/StuffIt)
* [微软展开](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/expand)


{
  "date" : "2021-07-12",
  "keywords" :[ "cmd 文件","什么是 cmd 文件","文件","cmd 示例","cmd 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 CMD 文件格式和可以创建和打开 CMD 文件的 API。",
  "title" :"CMD - Windows 命令文件格式",
  "linktitle" : "CMD",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-07-12"
}

## 什么是一 .cmd 文件？
CMD 文件由一个脚本组成，该脚本包含一个或多个纯文本形式的命令，这些命令是为了执行各种任务而运行的。它类似于一个[BAT](/zh/executable/bat/)文件，一般也用于存储一批可执行命令。 CMD 文件广泛用于 Microsoft Windows 操作系统。这些文件几乎是在 90 年代引入的，但仍在最新的 Windows 操作系统中使用。这些文件通常被编写为在一个序列中执行多个命令。

## CMD 文件格式
CMD 是 CP/M 风格的可执行程序使用的文件格式。它通常与 CP/M-80 中的 [COM](/zh/executable/com/) 和 DOS 中的 [EXE](/zh/executable/exe/) 相当。一个 CMD 文件包含 1 到 8 组代码或数据和一个 128 字节的标头。每个组的大小最大为 1 mb。 CMD 文件还可以在其更高版本中包含重定位信息和驻留系统扩展 (RSX)。与[BAT](/zh/executable/bat/) 文件相比，CMD 是一个新人；用于 MS-DOS 之前发布的 windows 在 MS-DOS 中。尽管今天您仍然可以使用 .bat 扩展名保存文件，但许多人使用 .cmd 扩展名来保存他们的可执行脚本。

### CMD 格式规范

标题的开头包含文件中存在的组列表及其类型。每种类型最多可使用一次。这些类型是：

- 代码
- 数据
- 额外的
- 堆
- 用户 1
- 用户 2
- 用户 3
- 用户 4
- 共享代码

同样，DOS 中的程序段前缀，数据组的前 256 个字节为零。它们将由带有零页的 CP/M-86 填充。如果没有数据组，则使用代码组的前 256 个字节。
## CMD 文件示例
以下是显示系统信息的 CMD 脚本示例。
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## 参考

* [如何编写 CMD 脚本](https://smallbusiness.chron.com/write-cmd-script-53226.html)
* [CMD 文件 (CP/M) - 来自维基百科](https://en.wikipedia.org/wiki/CMD_file_(CP/M))


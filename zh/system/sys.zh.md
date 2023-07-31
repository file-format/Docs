{
  "date" : "2021-07-08",
  "keywords" :["SYS","扩展名","文件","格式","系统","驱动程序","系统文件","程序","计算机","应用程序"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SYS - 系统文件格式",
  "description":"了解 SYS 文件格式和可以创建和打开 SYS 文件的 API。",
  "linktitle" : "SYS",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## 什么是一 .sys 文件？ ##

SYS 文件是在 Windows 操作系统和 MS-DOS 应用程序中使用的“系统文件"。这些文件不能直接打开，由设备的驱动和配置组成。 SYS文件负责包含操作系统核心功能的文件。这些被认为是设备驱动程序的关键文件，也可以在要解决竞赛驱动程序的任何问题时使用。它们负责计算机系统的正常运行，并且 .sys 文件必须正确且完整。


## 技术规格##

.sys 文件实际上是 [BMP](/zh/image/bmp/) 格式的子集，因为它只允许特定的组合。这些文件的通常格式为 LOGOS.SYS、LOGOW.SYS 和 LOGO.SYS。任何其他文件都没有这种格式。

这些文件在安装时主要在 Windows 的 *C* 目录中使用。大多数与设备驱动程序相关的问题都可以通过更新 Windows 操作系统来解决。这些文件的详细信息可以通过Windows操作系统的内置程序查看。这些还包括对操作系统中不同模块的引用。
系统文件的一些示例是：

* IO.SYS（这些存储磁盘操作系统的设备驱动程序）
* MSDOS.SYS（这些包含内核或操作系统的核心代码）
* CONFIG.SYS（这些包含各种配置选项）
* KEYBOARD.SYS（这些包含键盘布局相关信息）
* COUNTRY.SYS（这些包含国家和代码页相关信息）

## SYS 文件格式##

Microsoft 开发了带有 .sys 扩展名的文件。变量和函数包含在 SYS 文件中。这些主要由 Microsoft 操作系统使用。这些文件主要位于磁盘的根目录下：

* C:\Windows\system32\驱动程序
* C:\Windows\WinSxS

关于 SYS 文件的一些常见警告如下：

* 这些文件的名称不应更改，因为这些文件负责操作系统的核心功能和变量
* 这些文件不应删除，因为缺少这些文件会导致错误
* 在您确定来源的合法性之前，不应从 Internet 下载 .sys 文件
* 不应该弄乱这些文件，因为更改它们或弄乱这些文件会导致严重的系统错误
* 如果这些文件被某些病毒或恶意软件损坏，则应重新安装这些文件

## 系统示例##

下面是一个简单的 SYS 系统配置文件的例子：

```
DEVICE=C:\Windows\HIMEM.SYS
DOS=HIGH,UMB
DEVICE=C:\Windows\EMM386.EXE NOEMS
FILES=30
STACKS=0,0
BUFFERS=20
DEVICEHIGH=C:\Windows\COMMAND\ANSI.SYS
DEVICEHIGH=C:\MTMCDAI.SYS /D:123
```

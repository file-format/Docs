{
"日期":"2023-07-20",
   "keywords":[
"垃圾桶",
"BIN 文件",
"文件",
"BIN 文件扩展名",
"扩大",
"文件"
],
   "author":{
"display_name":"沙基尔·法伊兹"
},
"draft": "false",
"toc": true,
"title":"BIN 文件格式 - Unix 可执行文件",
   "description":"了解 BIN 格式以及可以创建和打开 BIN 文件的 API。",
"linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"executable-bin",
"parent": "executable"
}
},
"lastmod": "2023-07-20"
}

## 什么是 .bin 文件？

BIN 文件是基于 Unix 的操作系统（例如 Linux 或 FreeBSD）上的可执行文件。它保存由源代码派生的二进制代码组成的编译程序，使其与底层系统架构兼容。就可执行格式的作用而言，Unix 可执行 BIN 文件可以与 Windows .EXE 文件和 macOS .APP 文件进行比较。

在Unix系统的软件开发领域，开发人员通常使用BIN文件来打包和分发程序。它们提供了一种向用户交付软件的便捷方式，从而可以轻松安装和执行。除了 BIN 文件之外，还存在其他类型的 Unix 可执行文件，包括 [.ELF](/zh/executable/elf/)、.X86、[.RUN](/zh/executable/run/) 和 .X86_64，每种都针对特定硬件或系统要求。

当谈到 BIN 文件的内部结构时，它由 Unix 操作系统用来识别、读取和执行所包含程序的编码数据组成。系统依靠特定的文件签名或标头将 BIN 文件识别为可执行文件，然后解释和执行其中包含的二进制指令。

BIN 文件通常与随附的 **INSTALL.TXT** 文件捆绑在一起，该文件提供有关如何正确安装和设置程序的详细说明。该文档可确保用户能够成功地完成安装过程并开始使用该软件，不会出现任何复杂情况。

## 如何打开 BIN 文件？

BIN 文件不适合直接打开和查看。但是，您可以执行程序或提取它们包含的数据。要访问 BIN 文件的内容，请在命令行上执行以下步骤，假设 BIN 文件的名称为“sample.bin”：

1. **确保可执行权限：**

在执行 BIN 文件之前，请确保它具有作为可执行文件运行所需的权限。使用命令：

```
$ chmod +x sample.bin
```

该命令授予文件可执行权限。

2. **执行BIN文件：**

设置可执行权限后，输入以下命令即可运行BIN文件：

```
$ ./sample.bin
```

**警告**

_处理下载或通过电子邮件发送的 BIN 文件时请务必小心，因为网络犯罪分子可能会利用它们来传播恶意软件。仅运行来自受信任来源的 BIN 文件，以降低恶意可执行攻击的风险。_

## 其他BIN文件

以下是使用 **.bin** 文件扩展名的其他文件类型。

- [BIN - MacBinary 编码文件](/zh/compression/bin/)
- [BIN - 二进制光盘映像文件](/zh/disc-and-media/bin/)
- [BIN - BlackBerry IT 策略文件](/zh/settings/bin/)
- [BIN - 世嘉创世游戏 ROM](/zh/game/bin/)
- [BIN - PSX PlayStation BIOS 映像](/zh/game/bin-pcsx/)

## 参考

* [如何在Linux中执行二进制文件](https://linuxhint.com/execute-binary-files-in-linux/)



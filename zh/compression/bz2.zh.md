{
  "date" : "2019-10-11",
  "keywords" :["bz2 文件","bz2 文件格式","什么是 bz2 文件","文件","bz2 示例","bz2 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BZ2 - 压缩文件格式",
  "description":"了解什么是 BZ2 文件以及可以创建和打开 BZ2 文件的 API。",
  "linktitle" : "BZ2",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2020-09-05"
}

## 什么是一 .bz2 文件？

BZ2 是使用 [BZIP2](http://www.bzip.org/) 开源压缩方法生成的压缩文件，主要在 UNIX 或 Linux 系统上。它用于压缩单个文件，而不是用于归档多个文件。这与同一平台上的 TAR 文件格式形成对比，后者将多个文件归档为单个文件但不进行压缩。压缩为 BZ2 的文件可以使用 [WinZip](https://www.winzip.com/win/en/) 等应用程序解压缩。 BZIP2 使用运行长度编码 (RLE) 或 [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform) 压缩算法来实现高水平的压缩。

## BZ2 文件格式

此文件格式没有可用的正式规范。然而，一个非官方的 [逆向工程规范](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) 表明 .bz2 流由一个 4 字节的标头组成，其后跟通过零个或多个压缩块。紧随其后的是一个包含 32 位 CRC 的流结束标记，用于处理纯文本整个流。压缩块之间没有填充，所有块都是位对齐的。

## 解压/解压 BZ2 文件

您可以使用 WinZip 等软件在 Windows 和 Mac OS 上解压缩 BZ2 文件。在 linux 上，终端中的以下命令。

```
bzip2 -d filename.bz2
```

## 参考

* [BZIP2 格式规范](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)


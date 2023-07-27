{
  "date" : "2019-10-11",
  "keywords" :["tbz 文件","tbz 文件格式","什么是 tbz 文件","文件","tbz 示例","tbz 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TBZ - Bzip 压缩焦油存档",
  "description":"了解 TBZ 文件格式和可以创建和打开 TBZ 文件的 API。",
  "linktitle" : "TBZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## 什么是一 .tbz 文件？

扩展名为 .tbz 的文件是一种压缩存档，它使用 BZIP 压缩来减小内容文件的大小。 TBZ 文件实际上是使用 BZIP 压缩的 UNIX [TAR](/zh/compression/tar/) 归档文件。最新的二级压缩是 [BZIP2](/zh/compression/bz2/)，它取代了 BZIP。 TBZ 文件格式适合传输大文件。可以使用 7-Zip、PeaZip 和 jZip 等软件应用程序打开/提取 TBZ 文件。 Linux 和 macOS 用户还可以从终端窗口使用 BZIP2 命令打开 TBZ。

## TBZ 文件格式

TBZ 文件实际上是使用 BZIP/[BZIP2](/zh/compression/bz2/) 压缩创建的压缩档案。此文件格式没有可用的正式规范。然而，一个非官方的 [逆向工程规范](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) 表明 .bz2 流由一个 4 字节的标头组成，其后跟通过零个或多个压缩块。

## 参考 ＃＃

* [BZIP2 格式规范](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)


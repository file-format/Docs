{
  "date" : "2021-04-08",
  "keywords" :["mst 文件","mst 文件格式","什么是 mst 文件","文件","mst 示例","mst 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
	

},
  "draft" : "false",
  "toc" : true,
  "title" :"LBR - LU 库存档文件格式",
  "description":"了解 LBR 文件格式和可以创建和打开 LBR 文件的 API。",
  "linktitle" : "LBR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## 什么是一 .lbr 文件？

扩展名为 .lbr 的文件是使用 LU 程序创建的存档文件，在 1980 年代用于 CP/M 和 DOS 操作系统。它不再被使用，并已被现代归档文件格式所取代。该格式不压缩成员文件并充当这些文件的容器存档。存档功能主要用于通过 Internet 传输存档文件。由于 LBR 不提供压缩功能，因此使用其他实用程序（例如 SQ 或 CRUNCH）来压缩预归档的成员文件或归档后生成的归档文件以减小其大小。

## LBR 文件格式

LBR 文件格式由 Gary P. Novosielski 设计，没有公开的技术细节。 LBR 文件以 0x00 字节开始，然后是 11 个空格 (0x20)，然后是两个 0x00 字节，然后是两个不是都是 0x00 的字节。作为容器文件格式，可以使用 LU.COM 和 NULU.COM 进行提取。

## 参考

* [LBR - 维基百科](https://en.wikipedia.org/wiki/LBR_(file_format))


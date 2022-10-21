{
  "date" : "2019-10-11",
  "keywords" :["b6z 文件","b6z 文件格式","什么是 b6z 文件","文件","b6z 示例","b6z 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"B6Z - B6ZIP 存档文件格式",
  "description":"了解 B6Z 文件格式和可以创建和打开 B6Z 文件的 API。",
  "linktitle" : "B6Z",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## 什么是一 .b6z 文件？

扩展名为 .b6z 的文件是由 macOS 软件应用程序 [B6Zip](http://b6zip.com) 创建的压缩存档文件，用于压缩和解压缩文件。它是相对较新的存档格式，允许更高的压缩率。 B6Z 具有开放式架构，支持的文件大小高达 900000 PB。它支持数据压缩、错误恢复和文件跨越。 B6Zip 实用软件可在 MacOS 上免费使用，用于打开不同类型的压缩文件，包括 B6Z。

## B6Z 文件格式

B6Z 文件格式基于开放式架构，并使用 AES-256 加密算法提供可靠的压缩。它使用 LZMA2 作为默认压缩方法，但也支持以下其他压缩方法。

|方法|说明|
---|---|
|LZMA |LZ77算法优化版|
|LZMA2| LZMA改进版|
|放气|常规LZ77算法|
|BZip2|标准BWT算法|
|PPMD| Dmitry Shkarin 的 PPMdH|

B6Zip 实用程序支持所有这些压缩标准，并且经过高度优化，可实现高速化。它支持使用 [ZIP](/zh/compression/zip/)、[TAR](/zh/compression/tar/) 和 [RAR](/zh/compression/rar/) 文件格式。 B6Z 文件具有 MIME 类型 application/x-b6z-compressed。

## 参考

* [B6Zip](http://b6zip.com)


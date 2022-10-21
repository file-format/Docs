{
  "date" : "2022-06-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GZIP 文件格式 - GNU 压缩存档文件",
  "description":"了解什么是 GZIP 文件以及可以创建和打开 GZIP 文件的 API。",
  "linktitle" : "GZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-26"
}

## 什么是一 .gzip 文件？

GZIP 文件是使用标准 [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip) 压缩算法创建的压缩档案。压缩档案可能包含多个文件，包括压缩文件、目录和文件存根。大多数 Unix 系统包括用于压缩/解压缩文件的开源 gzip (GNU Zip) 压缩器实用程序。 GZIP 文件可以使用 [WinZip](https://www.winzip.com/en/) 等应用程序打开。

## GZIP 文件格式 - 更多信息

GZIP 使用 [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) 算法将文件压缩为档案。两个 RFC，[RFC1952](https://tools.ietf.org/html/rfc1952) 和 [RFC 1951](https://tools.ietf.org/html/rfc1951)，定义了 gzip 包装格式的规范和 deflate 压缩数据格式，分别。

GZIP 文件通常保存为 [GZ](/zh/compression/gz/) 文件格式。

## 参考

* [gzip](http://www.gzip.org/)
* [gzip - 维基百科](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952：GZIP 文件格式规范](http://tools.ietf.org/html/rfc1952)，由 IETF
* [RFC 1951](https://tools.ietf.org/html/rfc1951)


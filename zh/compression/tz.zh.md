{
  "date" : "2022-03-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TZ - 压缩焦油存档文件格式",
  "description":"了解什么是 TZ 文件以及可以创建和打开 TZ 文件的 API。",
  "linktitle" : "TZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-24"
}

## 什么是一 .tz 文件？

TZ 文件是使用 Unix 压缩算法压缩的 TAR 归档文件。它是 [TAR](/zh/compression/tar/) 压缩文件和 [Z](/zh/compression/z/) 压缩文件的组合，是 Unix OS 的原生压缩格式。 TZ 文件可以使用 WinZIP 和 WinRAR 等标准压缩实用程序打开。

## TZ 文件格式

TZ 文件使用 UNIX 压缩算法保存为二进制文件。 Z 文件的使用使文件的格式化、运行和打开更加容易。 TZ 文件的大小更小，因为 Z 压缩实现了高压缩。生成的文件在磁盘上占用的空间更少，并且可以通过通信媒体轻松传输。

## 参考

* [TAR - 维基百科提供](https://en.wikipedia.org/wiki/Tar_(computing))
* [TAR 基本格式](https://www.gnu.org/software/tar/manual/html_node/Standard.html)


{
  "date" : "2019-12-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZIM 文件格式 - OpenZIM 存档文件",
  "description":"了解 ZIM 文件格式和可以创建和打开 ZIM 文件的 API。",
  "linktitle" : "ZIM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## 什么是一 .zim 文件？ ##

扩展名为 .zim 的文件是为离线存储 Wiki 内容而创建的档案。它被认为是最适合在 USB 上存储 Wikipedia 的开放文件格式。它以紧凑的格式存储站点内容。它的名字来源于“Zeno IMproved"，这是早期的 Zeno 文件格式。 ZIM 由维基媒体 CH 赞助的 [openZIM](https://openzim.org/) 项目维护，并得到维基媒体基金会的支持。 ZIM 文件可以通过 Kiwix 和 ZIMReader 等应用程序打开。 OpenZIM 项目在 [Github](https://github.com/openzim) 上托管了 ZIM 文件格式的实现，以供开源社区的贡献。

## ZIM 文件格式规范

ZIM 文件格式是在 [Zeno 文件格式](https://openzim.org/wiki/Zeno_file_format) 之上开发的，不向后兼容。 ZIM 文件格式的格式规范由 openZIM [可在线获取](https://openzim.org/wiki/ZIM_file_format) 供开发者参考。 OpenZIM 提供了 C++ 开源实现，[LibZim](https://openzim.org/wiki/Zimlib)，用于读写 ZIM 文件。

ZIM 文件格式使用 LZMA2 压缩来使内容紧凑。

{{< figure src="../ZIM_File_Format.jpeg" alt="ZIM 文件格式" >}}


### ZIM 标头

ZIM 文件以偏移量 0 处的标头开头。所有成分均基于 little-endian，并且所有整数都是无符号整数，即 uint_16、uint_32、uint_64。

|字段名称 |类型|偏移量|长度|说明|
---|---|---|---|---|
|幻数|整数| 0| 4|识别文件格式的幻数，必须是 72173914 (0x44D495A)|
|主要版本|整数| 4| 2| ZIM 文件格式的主要版本（5 或 6）|
|小版本|整数| 6| 2| ZIM 文件格式的次要版本|
|uuid|整数| 8| 16|此 zim 文件的唯一 ID|
|文章数|整数| 24| 4|文章总数|
|集群计数|整数| 28| 4|集群总数|
|urlPtrPos|整数| 32| 8|按 URL 排序的目录指针列表的位置|
|titlePtrPos|整数| 40| 8|按 Title| 排序的目录指针列表的位置
|clusterPtrPos|整数| 48| 8|簇指针列表的位置|
|mimeListPos|整数| 56| 8| MIME 类型列表的位置（也是标题大小）|
|主页|整数| 64| 4|主页或 0xffffffff 如果没有主页|
|布局页面|整数| 68| 4|布局页面或 0xffffffffff 如果没有布局页面|
|校验和位置|整数| 72| 8|指向此文件的 md5checksum 的指针，不包含校验和本身。这总是指向文件结尾之前的 16 个字节。|

## 参考 ＃＃

* [OpenZIM](https://openzim.org/)
* [C++ LibZim](https://openzim.org/wiki/Zimlib)


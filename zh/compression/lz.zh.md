{
  "date" : "2021-04-08",
  "keywords" :["lz 文件","lz 文件格式","什么是 lz 文件","文件","lz 示例","lz 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ - Lzip 压缩文件格式",
  "description":"了解 LZ 文件格式和可以创建和打开 LZ 文件的 API。",
  "linktitle" : "LZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## 什么是一 .lz 文件？

扩展名为 .lz 的文件是使用 Lzip 创建的压缩存档文件，Lzip 是一个免费的命令行压缩工具。它支持连接以压缩支持文件。 LZ 文件的媒体类型为 application/lzip，并且支持比 [BZ2](/zh/compression/bz2) 更高的压缩比。 LZ 基于 LZMA（Lempel-Ziv-Markov 链）算法，包括 32 位 CRC 校验和和用于检查文件完整性的 ident 字节。

## LZMA 压缩格式

LZMA 压缩格式由使用自适应二进制范围编码器编码的压缩比特流组成。流被分成数据包。每个数据包描述单个字节或 LZ77 序列。每个数据包的长度和距离都被隐式或显式编码。

七种数据包类型如下（[Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview)）

|打包代码（位序列） |包名 |包描述|
---|---|---|
|0 + 字节码|点亮|使用自适应二进制范围编码器编码的单字节。
|1+0 + 长度 + 距离 |比赛|描述序列长度和距离的典型 LZ77 序列。
|1+1+0+0|短途旅行|一个单字节 LZ77 序列。距离等于上次使用的 LZ77 距离。|
|1+1+0+1 + 长度| LONGREP[0]| LZ77 序列。距离等于上次使用的 LZ77 距离。|
|1+1+1+0 + 长度|隆瑞普[1]| LZ77 序列。距离等于最后使用的第二个 LZ77 距离。
|1+1+1+1+0 + 长度|隆瑞普[2]| LZ77 序列。距离等于最后使用的第三个 LZ77 距离。|
|1+1+1+1+1 + 长度|龙瑞普[3]| LZ77 序列。距离等于最后使用的第四个 LZ77 距离。


## 参考

* [LZMA - 维基百科](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview)
* [Lzip](https://en.wikipedia.org/wiki/Lzip)


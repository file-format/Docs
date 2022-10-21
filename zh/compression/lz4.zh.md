{
  "date" : "2021-04-08",
  "keywords" :["lz4文件","lz4文件格式","什么是lz4文件","文件","lz4示例","lz4文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ4 - LZ4 压缩文件格式",
  "description":"了解可以创建和打开 LZ4 文件的 LBR 文件格式和 API。",
  "linktitle" : "LZ4",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## 什么是一 .lz4 文件？

扩展名为 .lz4 的文件是使用支持 [LZ4](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm)) 压缩的应用程序/实用程序创建的压缩存档文件。 LZ4 算法侧重于速度和压缩比之间的权衡。可以使用 LZ4 命令行实用程序创建压缩的 LZ4 存档，也可以使用该实用程序进行解压缩。

## LZ4 文件格式

LZ4 文件格式，基于 LZ4 压缩算法，独立于 CPU 类型、操作系统、文件系统和字符集。适用于使用LZ4算法的文件压缩和流压缩。 LZ4 格式的初始实现是由 Yann Collet 于 2011 年用 [C](/zh/programming/c/) 语言进行的，可供开发者参考 [Github](https://github.com/lz4/lz4) .

### LZ4 帧格式

LZ4文件格式的一般结构如下图所示。

|MagicNb|F.描述符|块|(...)|EndMark |C。校验和|
---|---|---|---|---|---|
|4 字节| 3-15 字节||| 4字节| 0-4字节|

#### 幻数

4 字节，小端格式。值：0x184D2204

#### 帧描述符

帧描述符由 3 t0 15 个字节组成，是规范中最重要的部分。 Magic_Number 和 Frame_Descriptor 字段一起称为 LZ4 帧头，其大小在 7 到 19 个字节之间变化。如下图所示。

|FLG| BD| （内容大小）| （字典ID）|碳氢化合物|
---|---|---|---|---|
|1 字节| 1个字节| 0 - 8 个字节| 0 - 4 个字节| 1个字节|

#### 数据块

每个数据块遵循以下顺序。

|块大小|数据| （块校验和）|
---|---|---|
|4 字节| |0 - 4 字节|

#### 结束标记

当最后一个数据块后跟 32 位值 0x00000000 时，块流结束。

#### 内容校验和

Content_Checksum 验证被正确解码的内容的有效性，并使用 xxHash-32 算法的结果进行。它以正确的顺序验证所有块的成功传输结果，并且没有任何错误。

## 参考

* [LZ4 帧格式](https://github.com/lz4/lz4/blob/dev/doc/lz4_Frame_format.md)
* [LZ4 压缩算法 - 维基百科](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))


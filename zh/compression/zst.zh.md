{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZST 文件 - Zstandard 压缩文件格式",
  "description":"了解 ZST 文件格式和可以创建和打开 ZST 文件的 API。",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## 什么是 .zst 文件？

ZST 文件是使用 Zstandard (zstd) 压缩算法生成的压缩文件。它是通过算法以无损压缩方式创建的压缩文件。 ZST 文件可用于压缩不同类型的文件，例如数据库、文件系统、网络和游戏。 Zstandard 受 [RFC 8878](https://www.rfc-editor.org/rfc/rfc8878) 管辖，它描述了整体压缩机制、媒体类型和内容编码。

## ZST 文件格式

ZST 文件以压缩文件格式存储到光盘。压缩机制如废弃 RFC 8478 的 RFC 8878 所述。

## ZST 框架

ZST 文件由一个或多个帧组成。每个帧可以是 Zstandard 帧或可跳过帧。 Zstandard 帧包含压缩数据，而可跳过帧包含自定义用户元数据。

### Z标准框架

Zstandard 框架具有以下结构。

|字段|字节大小|
---|---|
|Magic_Number |4 字节|
|Frame_Header |2-14 字节|
|Data_Block |n 字节|
|[更多数据块] ||
|[Content_Checksum] |4 字节|

### 可跳过的框架

可跳过的帧允许在串联帧流中插入用户定义的元数据。可跳过帧的结构如下。

|Magic_Number |Frame_Size |User_Data|
---|---|---|
|4 字节 |4 字节 |n 字节|

## 参考 ＃＃

* [RFC 8878 Zstandard 压缩](https://www.rfc-editor.org/rfc/rfc8878)


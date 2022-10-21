{
  "date" : "2020-08-20",
  "keywords" :["woff 文件","woff 文件格式","什么是 woff 文件","文件","woff 示例","woff 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WOFF - Web 打开文件格式",
  "description":"WOFF 文件是在 Web 开放字体格式中创建的开放字体格式。",
  "linktitle" : "WOFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-30"
}

## 什么是一 .woff 文件？

带有 .woff 扩展名的文件是基于 Web 开放字体格式 (WOFF) 的 Web 字体文件。它具有基于 TrueType (.TTF) 或 OpenType (.OTT) 字体类型的特定格式压缩容器。引入 WOFF 的目的是为了将 Web 字体与桌面应用程序中使用的字体文件区分开来。此外，该格式旨在减少字体通过网络从服务器传输到客户端计算机的延迟。有几种工具可以将 WOFF 文件转换为 TTF 和其他字体文件格式。

## **WOFF 文件格式**

WOFF 字体格式压缩了 TrueType、OpenType 和 Open Font Format 等不同字体类型中使用的基于表的 sfnt 结构的字体数据表。它就像这些字体类型的容器，也有空间包含字体的元数据和要包含在容器中的私人使用数据。转换器使用 sfnt 文件转换为 WOFF 格式的文件，用户代理恢复编码文件以供 Web 文档使用。需要说明的是，恢复的字体数据从各个方面都与输入的字体格式完全匹配。

WOFF 文件实用程序通常包含附加功能，例如字形子集、验证或字体功能添加，但不是必需的。创建者和使用代理都必须确保保留底层字体数据的有效性。

### WOFF 文件结构

WOFF 文件结构类似于 sfnt 字体。它基于包含每个字体数据表的长度和偏移量的表目录。所有表格都在此初始信息之后。该文件包含与原始字体相同的字体数据库。表的顺序也相同，但每个都可以被压缩。 WOFF 表目录虽然替换了原始表目录。

WOFF 文件包含以下内容：

* WOFFHeader - 具有基本字体类型和版本的文件头，以及元数据和私有数据块的偏移量。
* TableDirectory - 字体表的目录，指示 WOFF 文件中每个表的原始大小、压缩大小和位置。
* FontTables - 来自输入 sfnt 字体的字体数据表，经过压缩以降低带宽要求。
* ExtendedMetadata - 可选的扩展元数据块，以 XML 格式表示并压缩存储在 WOFF 文件中。
* PrivateData - 供字体设计者、铸造厂或供应商使用的可选私有数据块。

### WOFF 标题
WOFF 标头包含一个标识签名，该签名指示文件中包含的数据类型。 WOFF 标头及其字段如下所示。

|类型|字段名称|描述|
---|---|---|
|UInt32|签名 |0x774F4646 'wOFF' |
|UInt32| flavor |输入字体的“sfnt 版本"。|
|UInt32|长度 |WOFF 文件的总大小。|
|UInt16| numTables |字体表目录中的条目数。|
|UInt16|保留 |保留;设置为零。|
|UInt32| totalSfntSize |未压缩字体数据所需的总大小，包括 sfnt 标头、目录和字体表（包括填充）。|
|UInt16| majorVersion |WOFF 文件的主要版本。|
|UInt16| minorVersion |WOFF 文件的次要版本。|
|UInt32| metaOffset |从 WOFF 文件开始到元数据块的偏移量。|
|UInt32| metaLength |压缩元数据块的长度。|
|UInt32| metaOrigLength |元数据块的未压缩大小。|
|UInt32| privOffset |从 WOFF 文件开始到私有数据块的偏移量。|
|UInt32| privLength |私有数据块的长度。|


## **参考**
* [w3 WOFF 文件格式](https://www.w3.org/TR/WOFF/)


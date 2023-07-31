{
  "date" : "2021-02-25",
  "keywords": [ "ttc file", "ttc file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTC - TrueType 集合文件格式",
  "description":"TrueType Collection (TTC) 文件将多种字体组合成一个文件。Apple 和 Microsoft 在 Mac 和 Windows 操作系统上都使用了 TTF。",
  "linktitle" : "TTC",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## 什么是一 .ttc 文件？
TTC 缩写为 TrueType Collection 是 True Type 格式的扩展。一个 TTC 文件可以将多个字体文件组合到其中。这些文件有利于组合共享许多共同字形的多种字体。在 Windows 2000 之前，TTC 文件用于中文、日文和韩文版本的 Windows，但后来支持所有地区。


## 字库文件的结构
一个 TTC 文件由一个 TTC Header 表、表目录和多个 OpenType 表组成。 TTC 标头必须位于文件的开头。必须存在每种字体的完整表目录。 TableDirectory 格式应该与非集合文件中的格式相似。 TTC 文件中所有目录中的表计数是从 TTC 文件的开头计算的。
TTC 文件中的表格通过其各自字体的表格目录进行引用。一些 OpenType 表必须出现多次，在 TTC 中添加的每种字体一次。而其他表可能由 TTC 文件中的多种字体共享。

### TTC 标头
到目前为止，有两个版本的 TTC Header 表可用：
- 1.0 版用于没有数字签名的 TTC 文件。
- 2.0 版可用于带有或不带有数字签名的 TTC 文件。
以下是两个版本的 TTC Header 表：

**TTC 标头版本 1.0：**

|类型|名称|描述|
---|---|---|
|TAG|ttcTag|字体集合 ID 字符串：'ttcf'（用于具有 CFF 或 CFF2 轮廓以及 TrueType 轮廓的字体）|
|uint16|majorVersion|TTC 标头的主要版本，= 1。|
|uint16|minorVersion|TTC 标头的次要版本，= 0。|
|uint32|numFonts|TTC 中的字体数量|
|Offset32|tableDirectoryOffsets[numFonts]|每个字体从文件开头到 TableDirectory 的偏移量数组|

**TTC 标头版本 2.0：**

|类型|名称|描述|
---|---|---|
|TAG|ttcTag |字体集合 ID 字符串：'ttcf'|
|uint16| majorVersion |TTC 标头的主要版本，= 2。|
|uint16| minorVersion |TTC 标头的次要版本，= 0。|
|uint32| numFonts |TTC 中的字体数量|
|偏移32| tableDirectoryOffsets[numFonts] |每个字体从文件开头到 TableDirectory 的偏移量数组|
|uint32| dsigTag |表示存在DSIG表的标签，0x44534947（'DSIG'）（如果没有签名则为null）|
|uint32| dsigLength |DSIG 表的长度（以字节为单位）（如果没有签名则为 null）|
|uint32| dsigOffset |DSIG 表从 TTC 文件开头的偏移量（以字节为单位）（如果没有签名，则为 null）|

## 参考
* [OpenType 字体文件](https://learn.microsoft.com/en-us/typography/opentype/spec/otff)
* [TrueType (维基百科)](https://en.wikipedia.org/wiki/TrueType)


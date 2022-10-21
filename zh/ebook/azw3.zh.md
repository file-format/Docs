{
  "date" : "2019-12-12",
  "keywords" :["KF8","扩展名","文件","格式","电子书","Kindle 文件格式","AZW3 文件结构"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 AZW3 文件格式和可以创建和打开 AZW3 文件的 API。",
  "title" :"什么是 AZW3 文件？",
  "linktitle" : "AZW3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-06-04"
}

## 什么是 AZW3 文件？

AZW3，也称为 Kindle Format 8 (**KF8**)，是为亚马逊 Kindle 设备开发的 [AZW](/zh/ebook/azw/) 电子书数字文件格式的修改版本。该格式是对旧 AZW 文件的增强，仅用于 Kindle Fire 设备，它向后兼容原始文件格式，即 [MOBI](/zh/ebook/mobi/) 和 AZW。亚马逊在 KF8 之后推出了 KFX（KF 版本 10）格式，用于最新的 Kindle 设备。 AZW3 文件具有互联网媒体类型 application/vnd.amazon.mobi8-ebook。 AZW3 文件可以转换为许多其他文件格式，例如 [PDF](/zh/pdf/)、[EPUB](/zh/ebook/epub/)、[AZW](/zh/ebook/azw/)、[DOCX](/zh/ word-processing/docx/) 和 [RTF](/zh/word-processing/rtf/)。

## AZ3/KF8 文件格式##

KF8 文件本质上是二进制文件，并保留 MOBI 文件格式的结构作为 PDB 文件。如前所述，KF8 文件可能包含 MOBI 以及稍后更新的 KF8 版本的 EPUB。格式的内部细节已经被 [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack) 解码，这是一个 Python 脚本，用于解析最终编译的数据库并从中提取 MOBI 或 AZW 源文件。 AZW3 (KF8) 文件以 EPUB3 版本为目标，同时也向后兼容 EPUB。 KF8 编译 EPUB 文件并生成基于 PDB 文件格式的二进制结构。

## 参考 ＃＃

* [KF8 - 维基百科](https://en.wikipedia.org/wiki/Kindle_File_Format)
* [Kindle 解包](https://github.com/kevinhendricks/KindleUnpack)


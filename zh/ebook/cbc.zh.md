{
  "date" : "2019-12-12",
  "keywords" :["CBC","扩展名","文件","格式","漫画书","漫画书文件格式","电子书"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 CBC 文件格式和可以创建和打开 CBC 文件的 API。",
  "title" :"CBC - 漫画书收藏文件格式",
  "linktitle" : "CBC",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-03"
}

## 什么是一 .CBC 文件？

扩展名为 .cbc 的文件是用于电子书的漫画书文件的压缩集合，包含 [CBZ](/zh/ebook/cbz/) 和 [CBR](/zh/ebook/cbr/) 文件。它被 [Calibre](https://calibre-ebook.com/) 使用，这是一个电子书转换应用程序，它是一个跨平台的开源电子书管理器，可让您管理您的电子书并将其转换为不同的格式. CBC 文件包含一个 .txt 文件，comics.txt，其中列出了存档中的其他文件。有几个在线应用程序可以将 CBC 文件转换为 [AZW3](/zh/ebook/azw3/)、[EPUB](/zh/ebook/epub/)、[FB2](/zh/ebook/fb2/)、[MOBI](/zh/ebook/mobi/)、[TXT](/zh/word-processing/txt/)、[PDF](/zh/pdf/) 和其他流行的文件格式。

## CBC 文件格式

CBC 文件是包含 CBZ、CBR 和用于列出内容的文本文件的压缩档案。文本文件comics.txt 采用UTF8 编码，并包含供读者用于组织其收藏的CBC 文件列表。 CBC 文件通常具有允许组织此集合的多个属性，例如 Comic、Category、Publisher、Series、Edition 和 Artist。

示例 CBC 文件的内容如下所示：

* Comics.txt - 包含 CBR 和 CBZ 文件列表的文本文件
* 1.cbz
* 2.cbz
* 3.cbz
* CBZ 文件

其中comics.txt 文件列出的内容如下：

* 1.cbz：第一章
* 2.cbz：第二章
* 3.cbz：第三章

读者处理comics.txt 文件并根据提供的数据生成目录。

## 参考

* [口径](https://calibre-ebook.com/)


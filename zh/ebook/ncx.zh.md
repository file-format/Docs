{
  "date" : "2021-03-23",
  "keywords" :["NCX","EPUB 导航控制 XML 文件","扩展","格式","电子书","TOC","DAISY 联盟"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 EPUB 导航控制 XML 文件 (NCX) 文件格式和可创建和打开 NCX 文件的 API。",
  "title" :"NCX - EPUB 导航控制 XML 文件",
  "linktitle" : "NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## 什么是一 .ncx 文件？ ##

NCX 文件缩写为 XML 的导航控制文件，通常命名为 toc.ncx。此文件由 EPUB 文件的分层目录组成。 NCX 规范是为数字有声书 (DTB) 开发的，此文件格式由 **DAISY Consortium** 维护，不是 EPUB 规范的一部分。 NCX 文件中包含一个 mime 类型的 **application/x-dtbncx+xml**。

## NCX 规范 ##

NCX 文件包含各种 XML 标签。像 `meta name="dtb:uid"` 这样的元标记用于提及 ID。 `meta name="dtb:depth"` 元素设置为等于 `navMap` 标签元素的深度。 `navPoint` 元素可以嵌套以创建分层目录。 `navLabel` 的内容是出现在使用 .ncx 的阅读系统生成的目录中的文本。 `navPoint` 元素的内容指向清单中列出的内容文档，还可以包含元素标识符

EPUB 中使用的 NCX 规范的某些例外的描述。在这里您可以查看 NCX 文件的示例：

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE ncx PUBLIC "-//NISO//DTD ncx 2005-1//EN"
"http://www.daisy.org/z3986/2005/ncx-2005-1.dtd">

<ncx version="2005-1" xml:lang="en" xmlns="http://www.daisy.org/z3986/2005/ncx/">

  <head>
<!-- The following four metadata items are required for all NCX documents,
including those that conform to the relaxed constraints of OPS 2.0 -->

    <meta name="dtb:uid" content="123456789X"/> <!-- same as in .opf -->
    <meta name="dtb:depth" content="1"/> <!-- 1 or higher -->
    <meta name="dtb:totalPageCount" content="0"/> <!-- must be 0 -->
    <meta name="dtb:maxPageNumber" content="0"/> <!-- must be 0 -->
  </head>

  <docTitle>
    <text>Pride and Prejudice</text>
  </docTitle>

  <docAuthor>
    <text>Austen, Jane</text>
  </docAuthor>

  <navMap>
    <navPoint class="chapter" id="chapter1" playOrder="1">
      <navLabel><text>Chapter 1</text></navLabel>
      <content src="chapter1.xhtml"/>
    </navPoint>
  </navMap>

</ncx>
```

## 参考 ＃＃

* [来自维基百科的 EPUB](https://en.wikipedia.org/wiki/EPUB)
* [要在 toc.ncx 中包含哪些文件](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)


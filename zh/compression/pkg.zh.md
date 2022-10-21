{
  "date" : "2021-04-08",
  "keywords" :["pkg 文件","pkg 文件格式","什么是 pkg 文件","文件","pkg 示例","pkg 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PKG - 可扩展存档文件格式",
  "description":"了解 PKG 文件格式和可以创建和打开 PKG 文件的 API。",
  "linktitle" : "PKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## 什么是一 .pkg 文件？

带有 .pkg 扩展名的文件是一个安装程序包文件，用于在 macOS 上安装软件。除了 Macintosh 计算机之外，它还用于 iPhone。内置的 Apple 安装程序应用程序可用于安装 PKG 文件的内容。 PKG 文件类似于 Windows 操作系统上用于安装软件的 MSI 文件。在安装过程中，这些包文件可以记录消息，让您了解这个包安装了哪些额外的东西。

## PKG 文件格式

PKR 是经过压缩以减小整体文件大小的二进制文件。从 OSX 10.5 开始，Apple 引入了带有单个安装程序文件的平面包。这些与早期的打包格式不同，它们以捆绑包而不是单个文件的形式出现。这些捆绑的软件包包含一个结构化的目录层次结构，该层次结构以一种便于通过某些索引文件检索文件的方式存储文件。平面 PKG 文件格式实际上是一个 [XAR](/zh/compression/xar/) 存档，其中包含：

* Header - 定义大小、校验和和版本信息
* 目录 - 一个（并且必须）编码为 UTF-8 并存储在文件开头的 XML 文档，便于扫描存档以提取单个文件
* Heap - TOC 引用的非结构化数据堆

## 参考

* [平面包文件格式](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)
* [PKG - 维基百科](https://en.wikipedia.org/wiki/.pkg)


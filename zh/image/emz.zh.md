{
  "date" : "2019-10-11",
  "keywords" :["emz 文件","emz 文件格式","什么是 emz 文件","文件","emz 示例","emz 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMZ 文件格式 - Windows 压缩增强元文件",
  "description":"了解 EMZ 文件格式和可以创建和打开 EMZ 文件的 API。",
  "linktitle" : "EMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## 什么是一 .emz 文件？

扩展名为 .emz 的文件是增强型元文件（[EMF](/zh/image/emf/) 文件）的压缩容器。这些是使用 [GZIP](/zh/compression/gz/) 压缩技术压缩的，这是 UNIX 和 LINUX 操作系统上常用的压缩方法。取消 ZIP 链接 (/zh/compression/zip/)，GZIP 将存档作为一个整体进行压缩，而不是压缩单个文件。与 EMF 文件相比，EMZ 文件的大小更小，有助于在线文件共享期间的快速传输。一些可以打开 EMZ 文件的应用程序包括 Microsoft Visio 2019、Microsoft Office 2019、XnView MP 和 File Viewer Plus。

## EMZ 文件格式

EMZ 文件经过 [Gzip](/zh/compression/gz/) 压缩，内部包含 [EMF](/zh/image/emf/)。 Gzip 使用 DEFLATE 算法来压缩存档，并且在应用压缩方面有所不同。可以使用 GZip 压缩实用程序（例如 GNU Zip）解压缩 EMZ 文件。文件格式包括：

* 文件头
* 可选标题
* 压缩数据
* 文件页脚

由 Internet 工程任务组 (IETF) 发布的 GZIP 文件格式 [规范版本 4.3](https://datatracker.ietf.org/doc/html/rfc1952) 包含有关文件格式的详细信息。

## 参考

* [RFC1952：GZIP 文件格式规范](https://datatracker.ietf.org/doc/html/rfc1952)，由 [IETF](https://www.ietf.org/)
* [Windows 元文件 - 维基百科](https://en.wikipedia.org/wiki/Windows_Metafile)


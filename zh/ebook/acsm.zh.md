{
  "date" : "2021-03-10",
  "keywords" :[ "ACSM", "Adobe Content Server Message", "extension", "format", "eBook", "file", "Adobe Digital Editions"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 Adobe 的 ACSM 文件格式以及可以创建和打开 ACSM 文件的 API。",
  "title" :"ACSM - Adobe 内容服务器消息文件格式",
  "linktitle" : "ACSM",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-05-28"
}

## 什么是一 .acsm 文件？

扩展名为 .acsm 的文件称为 Adobe Content Server 消息文件。 **Adobe Digital Editions** 使用这些文件来激活和下载受 Adobe DRM 保护的内容。实际上，ACSM 文件不是电子书文件。它不能像其他电子书（例如 PDF）一样打开和阅读；它仅包含激活和下载电子书的数据。这意味着 ACSM 文件仅包含与 Adobe 服务器通信的信息。如果 Digital Editions 用户将下载电子书，他们可以看到 ACSM 文件，但下载会因任何原因停止。用户可以通过双击 .acsm 文件来恢复下载。

## ACSM 文件如何工作？

由于 Adobe Content Server 负责保护电子书和其他数字资料。购买后，内容会自动链接到买家的 Adobe ID。该 ID 是私有的，不能转让给其他人。用户必须在购买任何具有 Adobe 版权保护的文档之前进行设置。如果不将其 Adobe ID 传递给在后台运行的 Adobe 服务器应用程序，客户将无法访问其受版权保护的文档。

当客户进行购买时，ACSM 是他们首先可以下载的唯一文件。客户必须在其系统上安装 Adobe Digital Editions 软件并将其链接到其 Adobe ID 才能打开 ACSM 文件。 Adobe Digital Editions 将验证 ID 以获取转换 ACSM 文件的授权。如果通过身份验证，用户可以下载 [EPUB](/zh/ebook/epub/) 或 [PDF](/zh/pdf/) 格式的电子书。 Adobe Digital Editions 也使用 ACSM 文件来识别下载目录。

## 参考

* [Adobe 内容服务器 - 维基百科提供](https://en.wikipedia.org/wiki/Adobe_Content_Server)



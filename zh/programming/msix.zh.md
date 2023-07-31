{
  "date" : "2021-04-22",
  "keywords": [ "msix file", "extension", "format","how to open msix file","msix file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSIX - 什么是 MSIX 文件？",
  "description":"了解 MSIX 文件和可创建和打开 MSIX 文件的 API。",
  "linktitle" : "MSIX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## 什么是 .MSIX 文件？

MSIX 文件是一种 Windows 应用程序打包格式，用于在 Windows 10 中创建和分发应用程序。与最终将逐步淘汰的 [APPX](/zh/programming/appx/) 和 MSI 相比，这是现代的打包文件格式到这种新的文件格式。它可用于部署 Win32、WPF 和 Windows 窗体应用程序。 MSIX 文件是可靠的，目标是网络和磁盘空间优化。开发人员使用它们通过 Microsoft Store（以前称为 Windows Store）向最终用户分发程序。

## MSIX 文件格式 - 更多信息

MSIX 文件经过 [ZIP](/zh/compression/zip/) 压缩，所有文件都包含在打包文件中。除了应用相关文件之外，MSIX 文件还包含 [.xml](/zh/web/xml/) 配置文件，其中包含与应用安装相关的信息。

## MSIX 包里面有什么？

MSIX 包由以下文件组成。

* `AppxBlockMap.xml` - 称为包块映射文件，它是一个 XML 文档，其中包含应用程序文件的列表，其中包含存储在包中的每个数据块的索引和加密哈希。
* `AppxManifest.xml` - 包含部署、显示和更新 MSIX 应用所需信息的 XML 文档。此信息包括包标识、包依赖项、所需功能、可视元素和可扩展点。
* `AppxSignature.p7x` - 包签名时生成的文件。所有 MSIX 包都需要在安装前进行签名。使用 AppxBlockmap.xml，平台能够安装包并进行验证。

## 参考

* [MSIX 概述](https://learn.microsoft.com/en-us/windows/msix/overview)
* [使用 Microsoft Visual Studio 创建 APPX 文件](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)


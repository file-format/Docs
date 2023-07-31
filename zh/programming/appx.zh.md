{
  "date" : "2021-04-22",
  "keywords": [ "appx file", "extension", "format","how to open appx file","appx file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPX - 什么是 APPX 文件？",
  "description":"了解可以创建和打开 APPX 文件的 APPX 文件格式和 API。",
  "linktitle" : "APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## 什么是一 .appx 文件？

APPX 文件是一种可分发的包文件格式，用于分发和安装应用程序。它是随 Windows 8 引入的，将在 Microsoft Windows Store 上发布。它包含安装 Windows 应用程序所需的所有文件。其中包括元数据、文件和凭据信息。一种更现代的打包文件格式是 MSIX，与 APPX 相比，它目前更常用。

## APPX 文件格式 - 更多信息

APPX 文件以 [ZIP](/zh/compression/zip/) 文件格式保存为压缩文件。这使得整个包作为一个存档文件，文件大小减小，易于上传到 Microsoft Store。

## 如何查看APPX文件中的文件？

为了查看 APPX 文件中的内容或文件，应遵循以下步骤。

1. 由于 APPX 文件存储为压缩的 ZIP 文件，将文件重命名为 .zip 扩展名
1.使用7-Zip、WinZip、WinRAR等任意解压工具解压APPX文件中包含的文件

## 如何创建 APPX 文件？

有两种方法可用于创建 APPX 文件。

1. 使用 MakeApp.exe - [MakeApp.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) 用于创建两者应用程序包（.msix 或 .appx）和应用程序包捆绑文件 .msixbundle 或 .appxbundle）。此外，它可以从应用程序包中提取文件。 MakeApp.exe 随 Windows 10 SDK 提供，可从命令提示符使用。
1. 使用 Microsoft Visual Studio - 开发人员通常使用 Microsoft Visual Studio [创建 APPX 文件](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)。应用程序开发完成并准备好发布应用程序后，可以通过从 Visual Studio 中发布它来创建 APPX 包文件。

## 参考

* [使用 MakeAppx.exe 创建 MSIX 包或捆绑包](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
* [使用 Microsoft Visual Studio 创建 APPX 文件](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)


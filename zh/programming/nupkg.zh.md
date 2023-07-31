{
  "date" : "2022-03-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUPKG 文件 - NuGet 包文件",
  "description":"了解 NUPKG 文件格式和可以创建和打开 NUPKG 文件的 API。",
  "linktitle" : "NUPKG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-09"
}

## 什么是一 .nupkg 文件？

NUPKG 文件是一个包文件，其中包含 NuGet 软件用于创建要在 .NET 项目中使用的包的源代码。 NuGet 包管理器组件作为 Microsoft Visual Studio 的一部分安装，用于从在线包托管存储库中获取包。 NUPKG 文件帮助开发人员使用 NuGet 包管理器从 [Nuget.org](https://nuget.org) 获取最新包，而不是手动下载和安装开发包。 NUPKG 文件是从 NUSPEC 文件构建的，并且在获取时将包安装到用户系统上。

## NUPKG 文件格式

NUPKG 文件是 [ZIP](/zh/compression/zip/) 档案，其中包含打包的库。下载后，它可以重命名为 .zip 并使用任何标准 zip 实用程序（如 WinZIP、7-Zip 和 Apple Archive Utility）解压缩。

## 参考

* [Nuget.org](https://nuget.org)
* [快速入门：在 Visual Studio 中安装和使用包（仅限 Windows）](https://learn.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual-工作室）
* [如何创建和发布 Nuget 包](https://learn.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore- cli)


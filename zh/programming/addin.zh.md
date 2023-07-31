{
  "date" : "2021-04-22",
  "keywords": [ "addin file", "visual studio addin file", "extension", "format","addin file visual studio","addin file extension","how to open addin file","addin file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADDIN - Visual Studio 加载项定义文件",
  "description":"通过示例和可以创建和打开 ADDIN 文件的 API 了解什么是 ADDIN 文件格式。",
  "linktitle" : "ADDIN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-12"
}

## 什么是 ADDIN 文件格式？

扩展名为 .addin 的文件是 Microsoft Visual Studio 为加载项项目创建的加载项定义文件。它用于在 Visual Studio IDE 的加载项管理器中注册新的加载项，以便在其他项目中使用这些加载项而无需重新创建。插件本身是小型软件应用程序，可通过访问主要程序来扩展较大程序的功能。插件文件以 [XML](/zh/web/xml/) 文件格式存储在创建插件项目的同一位置。

## ADDIN 文件格式 - 更多信息

ADDIN 文件以人类可读的 XML 文件格式保存到光盘中。它可以在流行的文本编辑器中打开，包括 Notepad、Notepad++、Microsoft Visual Studio IDE 等。 Microsoft 已定义 Office Add 的 [XML 清单文件](https://learn.microsoft.com/en-us/office/dev/add-ins/develop/add-in-manifests?tabs=tabid-1) -in 描述了在安装外接程序并与 Office 文档和应用程序一起使用后应如何激活它。

**另请参阅：** [如何使用 Visual C# .NET 构建 Office COM 加载项](https://learn.microsoft.com/en-us/previous-versions/office/troubleshoot/office-developer/office-com-add-in-using-visual-c)

## 参考

* [Office 加载项 XML 清单](https://learn.microsoft.com/en-us/office/dev/add-ins/develop/add-in-manifests?tabs=tabid-1)


{
  "date" : "2023-01-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDISCO 文件 - DISCO 动态发现文档文件格式",
  "description":"了解什么是 VDISCO 文件？",
  "linktitle" : "VDISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-01-29"
}

## 什么是 .vdisco 文件？

VDISCO 文件是 Microsoft Visual Studio 在其 Web 服务中使用的发现文件。它提供有关可用 Web 服务的信息，例如 URL、名称空间和方法。 VDISCO 文件类似于 [DISCO](/zh/web/disco/) 文件格式，但在运行时生成。它存储在 Web 服务应用程序中，并由 Visual Studio 使用来动态发现和使用项目中的 Web 服务。 VDISCO 文件与包含实际 Web 服务代码的 [.asmx](/zh/web/asmx/) 文件结合使用。

您可以在任何文本编辑器（例如 Microsoft Notepad、Github Atom 和 Apple TextEdit）中打开 VDISCO 文件。也可以使用 Microsoft Visual Studio 2012 及更高版本打开它以进行使用。

## VDISCO 文件格式

VDISCO 文件以 [XML](/zh/web/xml/) 文件格式保存和托管，该文件格式是数据组合和发布的通用格式。它包含标准 XML 标记中的服务 URL、命名空间和方法，其中每个标记都包含其信息的相应值。

## 参考

* [DISCO](https://appsource.microsoft.com/en-us/product/office/WA104381894)
* [Web 服务发现](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [DiscoveryClient 类的 C# 示例](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)


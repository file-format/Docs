{
  "date" : "2022-09-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DISCO 文件 - DISCO 发现文档文件格式",
  "description":"了解什么是 DISCO 文件以及可以创建和打开 DISCO 文件的 API。",
  "linktitle" : "DISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-17"
}

## 什么是 .DISCO 文件？

DISCO 文件是一种 Microsoft Discovery 文件格式，用于发布和发现 Web 服务。它以 XML 文件格式存储，并允许 Web 服务发现工具定位或发现一个或多个相关文档，以描述可用的 [XML](/zh/web/xml/) 服务。 DISCO 文件存储诸如发现文档、[XSD](/programming/xsd/) 架构和服务描述等信息。 XML Web services 使用此信息来访问给定 URL 处可用的 XML Web services。

## DISCO 文件格式 - 更多信息

DISCO 文件以 XML 文件格式保存。与 Microsoft ASP.NET 开发软件（如 Microsoft Studio）捆绑在一起的 Microsoft Discovery Tool (DISCO.exe) 使用 DISCO 文件来发现有关特定 URL 的 DiscoveryDocument 中列出的 XML Web 服务的详细信息。 Microsoft 提供了在 .NET 框架中读取发现文件的支持。

## 参考

* [迪斯科](https://appsource.microsoft.com/en-us/product/office/WA104381894)
* [网络服务发现](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [C# DiscoveryClient 类示例](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)


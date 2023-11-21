{
  "date" : "2023-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AXD 文件 - ASP.NET Web 处理程序文件格式",
  "description" :"了解什么是 AXD 文件以及可以创建和打开 AXD 文件的 API。",
  "linktitle" : "AXD",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-05-23"
}

## 什么是 .axd 文件？

AXD 文件是一个 Web 设置文件，用于处理和检索 ASP.NET 中的嵌入资源请求。它包含用于检索嵌入式资源的指令，例如图像、JavaScript ([.JS](/zh/web/js/)) 文件和 [.CSS](/zh/web/css/) 文件。 AXD 文件用于将资源注入客户端页面。这允许客户端页面以标准方式访问服务器上的这些资源。

## AXD 文件格式

AXD 文件在服务器端存储为二进制文件。它指的是 ASP.NET 中的 Web 处理程序文件，这些文件是针对 Web 服务器的特定请求生成响应的组件。 AXD 文件在根据客户端页面请求生成响应之前执行自定义处理。这些通常保存为 **WebResource.axd** 文件。

### WebResource.axd 文件是什么？

大多数 ASP.NET 项目将 AXD 文件保存为 WebResource.axd 文件，允许客户端页面下载嵌入程序集中的资源。如果您在调试模式下运行应用程序，由于未缓存 WebResources.axd 处理程序，您的应用程序可能会面临性能下降的问题。

## 参考

* [WebResource.axd](https://social.msdn.microsoft.com/Forums/en-US/e6559555-5723-4590-9eb6-4b2af26a54cd/what-is-webresourceaxd?forum=aspgettingstarted)


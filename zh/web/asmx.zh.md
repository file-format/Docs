{
  "date" : "2019-10-11",
  "keywords" :["asmx","asmx 文件","asmx 文件格式","asmx 文件类型","文件","类型","什么是 asmx 文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASMX - ASP.NET Web 服务文件",
  "description" :"了解什么是 ASMX 文件以及可以创建和打开 ASMX 文件的 API。",
  "linktitle" : "ASMX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## 什么是一 .asmx 文件？

具有 .asmx 扩展名的文件是一种 ASP.NET Web 服务文件，它使用简单对象访问协议 (SOAP) 在 Internet 上提供两个对象之间的通信。它作为服务部署在基于 Windows 的 Web 服务器上，用于处理传入请求并返回响应。与包含 ASP.NET 网页可视化显示代码的 [ASPX](/zh/web/aspx/) 文件不同，ASMX 文件在后台运行在服务器上，并执行不同的任务，例如连接数据库、检索数据和返回数据提出请求的格式。这些专门用于 XML Web 服务。

## ASMX 文件格式

ASMX 文件为纯文本格式，可以在 Microsoft Visual Studio 或文本编辑器等应用程序中打开或编辑。它是 Microsoft 的专有文件格式，具有用于创建 Web 服务的明确定义的语法。 SOAP XML 形式的 ASMX 文件的响应具有以下元素。

* `Envelop` - 将 XML 文档标识为 SOAP 消息的根元素。
* `Header` - 一个可选元素，包含特定于应用程序的信息，例如身份验证数据。如果 Header 元素存在，它必须是 Envelope 元素的第一个子元素。
* `Body` - 包含发送给接收者的 SOAP 消息。
* `Fault` - 用于指示错误消息的可选元素。如果存在 Fault 元素，则它必须是 Body 元素的子元素。

ASMX 文件可以用 .NET 语言编写，例如 [C#](/zh/programming/cs/)、[Visual Basic](/zh/programming/vb/) 或 JScript。

## ASMX 与 ASPX 和 ASCX 有何不同？

ASMX 文件不同于 ASPX 和 ASCX 文件。

* ASPX，Active Server Pages，文件是使用在 Web 服务器上运行的 Microsoft ASP.NET 框架生成的编程文件。当用户请求访问此类页面时，它们会在客户端的 Web 浏览器中呈现。
* ASCX，Active Server User Control，定义用于定义 ASP.NET 网页或整个网站中可重用控件的用户控件。

## 参考

* [使用 ASMX 服务](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
* [ASCX 用户控制](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)


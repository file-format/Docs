{
  "date" : "2023-06-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"浏览器文件 - ASP.NET 浏览器定义文件格式",
  "description":"了解 BROWSER 文件格式以及可以创建和打开 BROWSER 文件的 API。",
  "linktitle" : "BROWSER",
  "menu" : {
    "docs" : {
      "parent" : "web",
      "identifier": "web-browser"
}
},
  "lastmod" : "22023-06-06"
}

## 什么是浏览器文件？

ASP.NET Web 应用程序使用扩展名为 .browser 的文件来确定 Web 浏览器的功能和配置。它包含有关浏览器的功能、限制和特征的信息。这些特征有助于 ASP.NET 框架识别发出请求的浏览器并相应地将网页呈现给用户。

## 浏览器文件格式

ASP.NET 应用程序使用浏览器定义文件来确定浏览器的功能。服务器使用该文件中包含的信息来生成与请求浏览器兼容的标记和其他资源。

BROWSER 文件以纯文本文件格式保存。您可以在文本编辑器（例如记事本、Notepad++、Apple TextEdit 和 Visual Studio IDE）中打开 BROWSER 文件。

### BROWSER 文件格式的文件结构

浏览器定义文件使用分层结构。每个 .browser 文件都包含一个 XML 标记，其中包括特定浏览器或一组浏览器的功能和特性。这些详细信息包括代理字符串、版本号等特征以及对 JavaScript、CSS 或其他 HTML 元素等技术的支持。通过使用这些浏览器定义文件，ASP.NET 开发人员可以根据不同浏览器的功能自定义用户体验。

## 参考

* [在 ASP.NET 网页中处理文件](https://learn.microsoft.com/en-us/aspnet/web-pages/overview/data/working-with-files)




{
  "date" : "2021-09-16", 
  "keywords" :["hta","文件","扩展","文件格式","hta 实现","编程指南","hta 示例","HTML 应用程序","超文本标记语言应用程序","HTA 文件", "Microsoft HTML 应用程序"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTA - HTML 应用程序文件",
  "description":"了解 HTA 文件格式和可以创建和打开 HTA 文件的 API。",
  "linktitle" : "HTA",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-16"
}

## 什么是一 .hta 文件？

HTMLA 代表 **Hypertext Markup Language Application** 是与 Microsoft Windows 兼容的程序。该程序的源代码包括不止一种脚本语言，例如[HTML](/zh/web/html/) 和[JavaScript](/zh/web/js/)。对于用户界面，首选 HTML 应用程序，而使用任何其他脚本语言来满足程序逻辑的要求。

HTML 应用程序独立于 Internet 浏览器的安全模型，并作为完全受信任的应用程序运行。用于有关这些应用程序的文件的扩展名是 HTA。这些应用程序包括 HTML 的功能以及其他脚本语言的属性。


## 历史简介 ＃＃

HTA 由 Microsoft 于 1999 年随着 Internet Explorer 5 的发布而首次推出。它与 Internet Explorer 兼容，因此只能在 Windows 操作系统上执行。该技术于 2003 年获得专利。HTA 文件的执行方式与任何其他 .exe 文件类似。 HTA 文件也与今天更新的 Windows 11 版本兼容。


## 技术规格##

HTA 具有与任何其他 HTML 页面相同的格式，而某些属性用于控制程序的边框或图标的样式。此外，还为启动 HTA 提供了论据。这些应用程序可以使用名为 mshta.exe 的程序执行。只需双击文件即可访问它。这些程序会自动与 Internet Explorer 一起运行。除其他规范外，这些规范并不独立于 Trident 引擎浏览器，而是独立于 Internet Explorer。这意味着这些可以在不使用 Internet Explorer 的情况下执行。

标签用于定制这些应用程序的外观。从 Microsoft HTML 应用程序到 HTA 格式的转换更容易，即您只需要更改扩展名。正如我们所知，这些应用程序是完全受信任的，因此与简单的 HTML 文件相比，它们包含更多的功能和优势。文本编辑器可用于创建 HTA。这些编辑器可以由 Microsoft 或任何其他受信任的来源获得。


## HTA 文件格式示例 ##

```
<HTML>
<HEAD>
<HTA:APPLICATION ID="HelloExample" 
   BORDER="bold" 
   BORDERSTYLE="complex"/>
<TITLE>HTA - Hello World</TITLE>
</HEAD>
<BODY>
<H2>HTA - Hello World</H2>
</BODY>
</HTML>

```

## 参考 ＃＃

* [HTA - 维基百科](https://en.wikipedia.org/wiki/HTML_Application)




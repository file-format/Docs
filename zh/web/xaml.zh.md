{
  "date" : "2019-10-11",
  "keywords" :["xaml","xaml 文件","xaml 文件格式","xaml 文件类型","文件","类型","什么是 xaml 文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAML - 基于 XML 的标记语言",
  "description":"了解 XAML 文件格式和可以创建和打开 XAML 文件的 API。",
  "linktitle" : "XAML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是 XAML 文件？

XAML，可扩展应用程序标记语言，扩展文件描述了基于 Windows Presentation Foundation (WPF) 的软件应用程序的用户界面元素。虽然是一门语言，但它不需要编程，因为它基于 **[XML](/zh/web/xml/)** 的标准格式，易于使用和理解。 XAML（发音为“zammel"）由 Microsoft 开发，专门用于创建用户界面。它的首字母缩写词 original 代表 Extensible Avalon Markup Language，其中 Avalon 是 WPF 的代号。 XAML 文件有时也使用 XOML 扩展名保存。

## XAML 应用程序

XAML 是 .NET Framework 3.0 和 .NET Framework 4.0 技术（如 WPF、Silverlight、Windows Workflow Foundation (WF) 等）中的使用选择。 UI 元素、数据绑定、事件和其他功能由 WPF 中的 XAML 表单定义。同样，WF 中的工作流可以使用 XAML 定义。由于它是基于 XML 的，因此很容易被工具处理。由于它是一种声明性语言并且不需要编译，因此出现了许多基于基于 XAML 的应用程序的产品。在 XAML 中创建或实现的任何内容都可以使用更传统的 .NET 语言（例如 C# 或 Visual Basic .NET）来表达。

## XAML 文件格式

XAML 完全基于 XML 格式。 [XAML 对象映射](https://download.microsoft.com/download/0/A/6/0A6F7755-9AF5-448B-907D-13985ACCF53E/%5BMS-XAML%5D.pdf) 的初始规范发布于2006 年，随后发布了另一个 [版本](http://download.microsoft.com/download/0/A/6/0A6F7755-9AF5-448B-907D-13985ACCF53E/%5BMS-XAML-2009%5D.pdf) 2009. 这些规范定义了两个抽象信息模型：

* XAML 架构信息集模型
* XAML 信息集模型

Xaml 信息集（简称“Xaml Infoset"）定义了 Xaml 实例可以表示的信息结构。 Xaml 架构信息集允许定义特定的 Xaml 词汇表。该规范还定义了一组将 XML 文档转换为 Xaml 信息集的规则。 XML 是 Xaml 的常用格式。 （术语“Xaml 文档"是指表示 Xaml 信息集的 XML 文档。）但是，虽然本规范没有定义任何其他表示，但可以使用任何物理表示，只要它可以表示 Xaml 信息集中的信息.

## 参考

* [XAML - 维基百科](https://en.wikipedia.org/wiki/Extensible_Application_Markup_Language)
* [XAML 文件格式规范](http://download.microsoft.com/download/0/A/6/0A6F7755-9AF5-448B-907D-13985ACCF53E/%5BMS-XAML-2009%5D.pdf)


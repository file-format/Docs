
{
  "date" : "2022-01-28",
  "keywords": [ ".aml file", "extension", "format","Microsoft Assistance Markup Language File", "how to open .aml file","aml file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AML 文件 - Microsoft 辅助标记语言文件",
  "description":"了解什么是 AML 文件以及可以创建和打开 AML 文件的 API。",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
"identifier":"programming-aml",
      "parent" : "programming"
}
},
  "lastmod" : "2022-01-28"
}

# AML - Microsoft 协助标记语言文件

## 什么是一 .AML 文件？

AML（辅助标记语言）文件是使用 Microsoft 辅助标记语言 (MAML) 生成的 XML 文件。它由 Microsoft 开发，旨在为 Microsoft Windows 操作系统提供在线帮助。在此之前，Windows 帮助以编译后的 HTML [CHM](/zh/web/chm/) 文件格式提供。 AML 文件提供结构化文档，允许应用程序创建源代码和支持帮助页面。这允许通过其上下文定义文档及其组成元素。 AML 帮助文件在线发布，并且可以配置为从在线可用的包更新中获取更新。

## MAML 文件结构

使用 MAML 生成的 AML 文件保存为 [XML](/zh/web/xml/) 文件，可用于表达广泛的活动概念。它还可以提供引导式帮助（活动内容向导），通过分步向导使帮助文件与用户交互。

使用 MAML 生成的 AML 文件遵循其创作结构，可分为以下部分：

* 概念
* 常问问题
* 词汇表
* 程序
* 参考
* 可重复使用的内容
* 任务
* 故障排除，以及
* 教程

## 如何创建 MAML 文件？

可以使用以下方法之一创建 MAML 文件：

* 使用 Sandcastle - 利用一套模式和程序可执行文件来生成帮助文件。但是，此工具已停产。
* 使用 DocProject - 一个 Microsoft Visual Studio 插件，可以在 Microsoft Visual Studio 中执行以生成帮助内容。

可以使用 Sandcastle 创建 MAML 文件，这是一套 .XSL 模式和程序可执行文件。也可以使用 Microsoft Visual Studio 帮助创作工具插件 DocProject 创建它们。

## 参考

* [使用 PlatyPS 创建基于 XML 的帮助
]（https://docs.microsoft.com/en-us/powershell/scripting/dev-cross-plat/create-help-using-platyps?view=powershell-7.2）
* [微软协助标记语言](https://en.wikipedia.org/wiki/Microsoft_Assistance_Markup_Language)

# AML - Arc 宏语言文件

## 什么是 ARC 宏 AML 文件？

AML（ARC 宏语言）文件是使用 ArcInfo Workstation GIS 应用程序生成的脚本文件。它是用 ARC 宏语言编写的，这是一种专有的高级算法语言，用于在 ArcInfo 中创建 GIS 应用程序。 AML 由 ESRI 于 1986 年设计，用于从其命令行 ARCINFO GIS 系统创建应用程序。作为脚本文件，AML 文件可以包含脚本命令来执行许多任务，例如创建用户界面组件和操作地图数据。

## AML 文件格式 - 更多信息

AML，作为脚本文件，将信息作为纯文本文件保存到光盘。它遵循基于 PRIMOS 操作系统的 CPL shell 语言的 AML 语法。 AML 语言已被 ESRI 的地理处理框架取代，该框架是 ArcGIS 套件的一部分，并使用 ArcObjects 通过 VBA 或 Python 提供编程支持。

## 参考

* [ARC 宏语言](https://en.wikipedia.org/wiki/ARC_Macro_Language)
* [通过脚本工具使用 AML](https://desktop.arcgis.com/en/arcmap/latest/analyze/creating-tools/using-amls-with-script-tools.htm)


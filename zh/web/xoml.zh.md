{
  "date" : "2019-10-11",
  "keywords" :["xoml","文件","扩展名","文件格式","文件扩展名","可扩展对象标记语言"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XOML - Windows 工作流文件格式",
  "description":"了解 XOML 文件格式和可以创建和打开 XOML 文件的 API。",
  "linktitle" : "XOML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .xoml 文件？

XOML 是 Extensible Object Markup Language 的首字母缩写，是 Windows Workflow Foundation 的工作流对象的序列化格式。基于**[XAML](/zh/web/xaml/)**，它主要用于创建普通的用户界面**[XML](/zh/web/xml/)**。这些用于声明用户界面的工作流，并与包含实现逻辑的单独文件一起编译。它包含一个基于树的结构，该结构定义了一个根工作流节点、嵌套的子元素和嵌入的代码段。使用 Visual Studio for .NET 创建新工作流时，您可以选择是代码格式还是代码分隔格式。如果您选择后者，IDE 将为您创建两个文件；一种是 XOML 格式（由工作流布局和设置组成），另一种是编程代码所在的 [.CS](/zh/programming/cs/)/[.VB](/zh/programming/vb/) 格式。


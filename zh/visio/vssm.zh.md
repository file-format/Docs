{
  "date" : "2019-10-11",
  "keywords" :["vssm 文件","vssm 文件格式","什么是 vssm 文件","文件","vssm 示例","vssm 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSSM - Microsoft Visio 启用宏的文件格式",
  "description":"了解 VSSM 文件格式和可以创建和打开 VSSM 文件的 API。",
  "linktitle" : "VSSM",
  "menu" : {
    "docs" : {
"identifier":"visio-vssm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .VSSM 文件？

扩展名为 .vssm 的文件是 Microsoft Visio Stencil 文件，支持提供对宏的支持。 VSSM 文件在打开时允许运行宏以在图表中实现所需的格式和形状放置。一般来说，Microsoft Visio 是一种绘图软件，它允许创建文件，这些文件可以包含并以不同形状表示用户定义的信息。其中最常见的包括但不限于 UML 图、流程图、可视对象、信息流、组织结构图、软件图、网络布局、数据库模型、对象映射和其他类似信息。使用 Visio 生成的文件也可以转换为不同的文件格式，例如 [PNG](/zh/Image/PNG/)、[BMP](/zh/Image/BMP/)、[PDF](/zh/pdf/) 等。

## VSSM 文件格式

VSSM 文件格式是在基于 OpenOffice XML 规范的 Microsoft Visio 2013 中引入的。构成 Visio 2013 文件格式的某些其他文件类型包括：

* .vsdm（支持 Visio 宏的绘图）
* .vssx（Visio 模具）
* .vssm（启用 Visio 宏的模具）
* .vstx（Visio 模板）
* .vstm（Visio 启用宏的模板）

在底层，Visio 2013 文件格式使用结构化方法将应用程序数据与相关资源一起存储在存档中，例如 [ZIP](/zh/Compression/ZIP/)。 ZIP 文件可以使用任何标准提取实用程序进行提取，其中还包含其他类型的文件。

每个 Visio 文件都称为包含其他文件或部分的包。包部分可以是 XML 文件、图像甚至是 VBA 解决方案。包中的部分可以分为“文档"部分和“关系"部分。

## 参考 ＃＃

* [Visio 文件格式简介](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)


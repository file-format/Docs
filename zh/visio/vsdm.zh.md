{
  "date" : "2019-10-11",
  "keywords" :["vsdm 文件","vsdm 文件格式","什么是 vsdm 文件","文件","vsdm 示例","vsdm 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDM - Microsoft Visio 绘图文件格式",
  "description":"了解 VSDM 文件格式和可以创建和打开 VSDM 文件的 API。",
  "linktitle" : "VSDM",
  "menu" : {
    "docs" : {
"identifier":"visio-vsdm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .VSDM 文件？

带有 .vsdm 扩展名的文件是使用支持宏的 Microsoft Visio 应用程序创建的绘图文件。 VSDM 文件是类似于 VSDX 的 OPC/XML 工程图，但也提供了在打开文件时运行宏的能力。宏是在 Visual Basic for Applications (VBA) 中开发的用户定义的操作/步骤，可用于执行重复性任务。 VSDM 文件格式是随着 Microsoft Visio 2013 的推出而引入的。Visio 文件用于创建包含可视对象、流程图、UML 图、信息流、组织图、软件图、网络布局、数据库模型、对象映射等的绘图类似的信息。使用 Visio 生成的文件也可以导出为不同的文件格式，例如 [PNG](/zh/image/png/)、[BMP](/zh/image/bmp/)、[PDF](/zh/pdf/) 等。

## VSDM 文件格式

VSDM 文件基于 Open Packaging Conventions 和 XML，开发人员可以通过学习如何以编程方式使用这些文件来从这种格式中受益。该格式从 Visio XML 绘图文件格式 (.vdx) 继承了许多与其部分相同的 XML 结构。由于第三方软件可以在文件格式级别操作 Visio 文件，因此与 Visio 文件的互操作性大大提高。

每个 Visio 文件都称为包含其他文件或部分的包。包部分可以是 XML 文件、图像甚至是 VBA 解决方案。包中的部分可以分为“文档"部分和“关系"部分。

＃＃＃ 文档 ＃＃＃

文档部分包含 Visio 文件的实际内容和元数据，如文件名、第一页和它包含的所有形状，甚至是形状的数据连接。包中的图像和文本文件被视为文档部分。

### 关系###

Visio 文件的关系部分存储在“\_rels"文件夹中，并描述包中的部分如何与每个部分相关。它还提供了文件的结构。独立的 XML 文档使用元素的父/子关系来确定实体之间的关系。有效的 Visio 2013 文件格式包含正确的部件集，并且包包含部件之间的关系。

关系部分是描述包内不同文档部分之间关系的 XML 文档。它们定义了两个项目之间的关联：一个指定的源（由关系文件的名称和位置定义）和一个指定的目标文档部分。例如，关系部分用于描述哪些形状母版与文件相关联、页面如何与文件相关以及如何相互关联，或者图像和对象如何与特定页面相关。

## 参考 ＃＃

* [Visio 文件格式简介](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)


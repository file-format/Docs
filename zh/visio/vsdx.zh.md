{
  "date" : "2019-10-11",
  "keywords" :["vsdx 文件","vsdx 文件格式","什么是 vsdx 文件","文件","vsdx 示例","vsdx 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDX",
  "description":"了解 VSDX 文件格式和可以创建和打开 VSDX 文件的 API。",
  "linktitle" : "VSDX",
  "menu" : {
    "docs" : {
"identifier":"visio-vsdx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .VSDX 文件？

带有 .vsdx 扩展名的文件代表从 Microsoft Office 2013 开始引入的 Microsoft Visio 文件格式。开发它是为了替换早期版本的 Microsoft Visio 支持的二进制文件格式 [.VSD](/zh/image/vsd/)。 Microsoft SharePoint Server 2013 中的 Visio Services 也支持它，并且不需要中间文件格式即可发布到 SharePoint Server。 Visio 文件用于创建包含可视对象、流程图、UML 图、信息流、组织结构图、软件图、网络布局、数据库模型、对象映射和其他类似信息的绘图。使用 Visio 生成的文件也可以导出为不同的文件格式，例如 [PNG](/zh/image/png/)、[BMP](/zh/image/bmp/)、[PDF](/zh/pdf/) 等。

## 文件格式 ＃＃

VSDX 文件基于 Open Packaging Conventions 和 XML，开发人员可以通过学习如何以编程方式使用这些文件来从这种格式中受益。该格式从 Visio XML 绘图文件格式 (.vdx) 继承了许多与其部分相同的 XML 结构。由于第三方软件可以在文件格式级别操作 Visio 文件，因此与 Visio 文件的互操作性大大提高。

构成 Visio 2013 文件格式的某些其他文件类型包括：

* .vsdm（支持 Visio 宏的绘图）
* .vssx（Visio 模具）
* .vssm（启用 Visio 宏的模具）
* .vstx（Visio 模板）
* .vstm（Visio 启用宏的模板）

在底层，Visio 2013 文件格式使用结构化方法将应用程序数据与相关资源一起存储在存档中，例如 [ZIP](/zh/compression/zip/)。 ZIP 文件可以使用任何标准提取实用程序进行提取，其中还包含其他类型的文件。您可以在 windows explore 中将 .vsdx 文件扩展名替换为 .zip 以查看 VSDX 文件中的内容。

每个 Visio 文件都称为包含其他文件或部分的包。包部分可以是 XML 文件、图像甚至是 VBA 解决方案。包中的部分可以分为“文档"部分和“关系"部分。

＃＃＃ 文档 ＃＃＃

文档部分包含 Visio 文件的实际内容和元数据，如文件名、第一页和它包含的所有形状，甚至是形状的数据连接。包中的图像和文本文件被视为文档部分。

### 关系###

Visio 文件的关系部分存储在“\_rels"文件夹中，并描述包中的部分如何与每个部分相关。它还提供了文件的结构。独立的 XML 文档使用元素的父/子关系来确定实体之间的关系。有效的 Visio 2013 文件格式包含正确的部件集，并且包包含部件之间的关系。

关系部分是描述包内不同文档部分之间关系的 XML 文档。它们定义了两个项目之间的关联：指定的源（由关系文件的名称和位置定义）和指定的目标文档部分。例如，关系部分用于描述哪些形状母版与文件相关联，页面如何与文件相关以及如何相互关联，或者图像和对象如何与特定页面相关。

## 参考 ＃＃

* [Visio 文件格式简介](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)


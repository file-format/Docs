{
  "date" : "2019-10-11",
  "keywords" :["vssx 文件","vssx 文件格式","什么是 vssx 文件","文件","vssx 示例","vssx 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSSX - Visio 模板文件格式",
  "description":"了解 VSSX 文件格式和可以创建和打开 VSSX 文件的 API。",
  "linktitle" : "VSSX",
  "menu" : {
    "docs" : {
"identifier":"visio-vssx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .VSSX 文件？

带有 .vssx 扩展名的文件是使用 [Microsoft Visio](https://products.office.com/en/visio/flowchart-software) 2013 及更高版本创建的绘图模板。 VSSX 文件格式可以用 Visio 2013 及更高版本打开。 Visio 文件以表示各种绘图元素而闻名，例如形状、连接器、流程图、网络布局、UML 图、软件图、数据库模型、对象映射和其他类似信息的集合。 Microsoft Visio 还提供将 Visio 文件转换为不同文件格式的功能，例如 [PNG](/zh/image/png/)、[BMP](/zh/image/bmp/)、[PDF](/zh/pdf/) 等。它适用于 Windows 和 Mac OS。

## VSSX 文件格式

VSSX 文件格式基于 Microsoft 自 2007 年以来采用的 OpenOffice 格式。它基于表示基于 XML 文件格式规范的整体文件格式的 [ZIP](/zh/compression/zip/) 存档。与 VSSX 等效的二进制文件格式是直到 Visio 2007 才支持的 VSS。您可以通过将 VSSX 文件格式的扩展名替换为 .ZIP 并以任何存档文件格式（如 WinZIP）打开来查看 VSSX 文件格式的内容。

VSDX 文件基于开放打包约定和 XML，开发人员可以通过学习如何以编程方式使用这些文件来从这种格式中受益。该格式从 Visio XML 绘图文件格式 (.vdx) 继承了许多与其部分相同的 XML 结构。由于第三方软件可以在文件格式级别操作 Visio 文件，因此与 Visio 文件的互操作性大大提高。

构成 Visio 2013 文件格式的某些其他文件类型包括：

* .vsdm（支持 Visio 宏的绘图）
* .vssx（Visio 模具）
* .vssm（启用 Visio 宏的模具）
* .vstx（Visio 模板）
* .vstm（Visio 启用宏的模板）

每个 Visio 文件都称为包含其他文件或部分的包。包部分可以是 XML 文件、图像甚至是 VBA 解决方案。包中的部分可以分为“文档"部分和“关系"部分。

## 参考 ＃＃

* [Visio 文件格式简介](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)
* [架构图 - Visio XML](https://learn.microsoft.com/en-us/office/client-developer/visio/schema-mapvisio-xml)


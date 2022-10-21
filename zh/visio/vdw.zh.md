{
  "date" : "2019-10-11",
  "keywords" :["vdw","vdw文件","vdw文件格式","vdw文件类型","文件","类型","什么是vdw文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDW - Visio 图形服务文件格式",
  "description":"了解 VDW 文件格式和可以创建和打开 VDW 文件的 API。",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
"identifier":"visio-vdw",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}
## 什么是一 .vdw 文件？

VDW 是 Visio 图形服务文件格式，它指定呈现 Web 绘图所需的流和存储。 Web 绘图是绘图页面、形状、字体、图像、数据连接和图表更新信息的集合，可以呈现为矢量或光栅绘图。 VDW 文件也可以在 Microsoft Visio 中打开，但主要保存在 Web 上使用。 Microsoft Visio 提供将 Visio 文件转换为多种不同文件格式的功能，包括 [PNG](/zh/Image/PNG/)、[BMP](/zh/Image/BMP/)、[PDF](/zh/pdf/) 等。

## **VDW** 文件格式

[Microsoft](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx) 在线提供 VDW 文件格式的技术规范，开发者可以参考创建应用程序。该技术文档描述了包含在包含存储和流的复合文件中的数据。 Web 绘图的表示是通过一个名为 VisioServerData 的流，通过 ZIP 存档实现的。存档中的 ShapGraphic XML 部件描述了 Web 绘图中显示的图形元素，并以可扩展应用程序标记语言 (XAML) 表示。 ZIP 存档中的 XML 部分集合描述了 Web 绘图的数据连接、有关其形状的信息和图表更新逻辑。这些部分表示为 XML。 DataGraphic XML 部分描述了在从数据源刷新 Web 绘图中的数据后要评估的重新计算属性。 ZIP 存档中的其他项目包含 Web 绘图中使用的字体和图像的信息。

|![文件的可能实现](/zh/web/vdw.png "文件的可能实现")

## 参考

* [[MS-VGSFF]：Visio 图形服务 (.vdw) 文件格式](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)


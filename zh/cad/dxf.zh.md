{
  "date" : "2020-03-16",
  "keywords" :["DXF 文件","文件格式","CAD"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 DXF 文件格式和可以创建和打开 DXF 文件的 API。",
  "title" :"DXF 文件格式",
  "linktitle" : "DXF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .dxf 文件？

DXF，即图形交换格式，或图形交换格式，是 AutoCAD 图形文件的标记数据表示。文件中的每个元素都有一个前缀整数，称为组码。该组代码实际上表示后面的元素，并指示给定对象类型的数据元素的含义。 DXF 可以在图形文件中表示几乎所有用户指定的信息。

DXF 文件格式是 Autodesk 开发的 CAD 数据文件格式，用于 AutoCAD 和其他应用程序之间的数据互操作性。因此，可以根据 DXF 文件格式互操作性规范将数据从其他格式导入 DXF 到 AutoCAD。

## 历史简介 ＃＃


DXF 文件格式的历史可以追溯到 1982 年，当时它是作为 AutoCAD 1.0 的一部分引入的。 AutoCAD 的初始版本仅支持 DXF 的 ASCII 文件格式。随着 1988 年 AutoCAD 第 10 版（及更高版本）的发布，AutoCAD 引入了对 ASCII 和二进制 DXF 文件格式的支持。在早期阶段，Autodesk 没有共享任何文件格式规范，因此，正确导入 DXF 文件并不容易。但是，Autodesk 现在发布了 DXF 规范并可供公众使用。

## 文件格式规范##

DXF 文件格式使用组代码和值对将内容排列成部分。每个部分由记录组成，其中每个记录由组代码和数据项组成。每个组代码和值都在 DXF 文件中各自的行上。每个部分都以组代码 0 开头，后跟字符串 SECTION。后面是组代码 2 和指示节名称的字符串（例如，SECTION1）。每个部分由定义其元素的组代码和值组成。一个节以 0 结尾，后跟字符串 ENDSEC。

DXF 文件格式考虑与实体不同的对象。对象在这里没有图形表示，但实体有它。因此，DXF 中的条目被称为具有图形对象，而对象对象被称为非图形对象。 DXF 文件的 BLOCK 和 ENTITIES 部分包含实体，这两个部分中组码的使用是相同的。一个实体的结束由下一个 0 组指示，该组开始下一个实体或指示该部分的结束。

### 文件结构###

DXF 文件中的部分按以下顺序排列：

|栏目|基本说明
---|---|
|标题|此部分包含有关绘图的一般信息。这就像您手机中的设置功能，其中包含与绘图关联的不同变量及其关联值。例如，标题部分将定义 DXF 文件使用的 AutoCAD 版本（$ACADVER 变量）或文件中用于测量角度的单位（$AUNITS 变量）
|Classes|CLASSES 部分保存应用程序定义的类的信息，这些类的实例出现在数据库的 BLOCKS、ENTITIES 和 OBJECTS 部分中。
|Tables|此部分包含几个不同表的定义，每个表都包含许多不同的符号条目。例如[线型](https://knowledge.autodesk.com/support/autocad/learn-explore/caas/CloudHelp/cloudhelp/2016/ENU/AutoCAD-Core/files/GUID-20B4D4B3-1220-426A- 847B-5BBE36EC6FDF-htm.html) 表 (LTYPE) 定义了 DXF 文件中的破折号、点、文本和符号的模式以及它们的缩放方式。以下是本节中找到的表格的完整列表：<ul><li>应用程序 ID (APPID) 表</li><li>块记录 (BLOCK_RECORD) 表</li><li>尺寸样式 (DIMSTYPE) 表</li><li>层（LAYER）表</li><li>线型 (LTYPE) 表</li><li>文本样式 (STYLE) 表</li><li>用户坐标系 (UCS) 表</li><li>查看 (VIEW) 表</li><li>视口配置 (VPORT) 表</li></ul>
|块|此部分包含构成图形中每个块参考的图形对象和图形实体。
|实体|此部分包含绘图的实际对象数据和图形实体。这可以包括原始数据——例如，圆形实体由其厚度、中心点、半径和拉伸方向定义。
|对象|在这里，您将找到绘图的非图形部分。例如，AutoCAD 字典存储在此处。

## 参考 ＃＃

* [DXF 文件规格](http://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [维基百科的 AutoCAD DXF](https://en.wikipedia.org/wiki/AutoCAD_DXF)


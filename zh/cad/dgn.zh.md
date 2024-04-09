{
  "date" : "2020-01-12",
  "keywords" :["DGN","文件","格式","打开","读取","API","MicroStation","Intergraph 交互式图形设计系统"],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DGN - MicroStation CAD 设计文件格式",
  "description" :"了解 DGN 文件格式和可创建和打开 DGN 文件的 API。",
  "linktitle" : "DGN",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2020-01-12"
}

## 什么是 .dgn 文件？

扩展名为 .dgn（设计）的文件是由 CAD 应用程序（如 MicroStation 和 Intergraph Interactive Graphics Design System）创建并受其支持的绘图文件。它用于为公路、桥梁和建筑物等建设项目创建和保存设计。该格式类似于 Autodesk 的 [DWG](/zh/cad/dwg/) 文件格式，被视为其竞争对手。 DNG 文件可以保存为鹰图标准文件格式或 V8 DGN。 DGN 可以转换为其他几种格式，例如 DWG、[BMP](/zh/image/bmp/)、[JPEG](/zh/image/jpeg/)、[PDF](/zh/pdf/)、[GIF](/zh/image/gif/) 等。除了其他软件应用程序（例如 Corel PaintShop Photo Pro 和 IMSI TurboCAD Deluxe 版本）之外，它还可以使用 Autodesk AutoCAD、Bentley View 和 Bentley Systems MicroStation 打开。

## V8 DGN 文件格式

MicroStation V8 DGN 文件由一个或多个模型组成。模型是元素的容器。 V8 DGN 删除了以前版本的 MicroStation 中存在的所有基于文件格式的约束。以下是 DGN 文件格式的改进列表。

* 取消了 DGN 文件中层数的限制，每个层都被命名并存储为一个元素。
* DGN 文件的最大物理大小没有任何限制，仅受操作系统限制（如 NT 限制为 4 GB）
* 单个元素的最大大小为 128 KB。
* 单元格的最大大小没有限制。
* 单元名称限制为大约 500 个字符。
* 可以附加到 DGN 文件的参考数量没有限制。
* 线串、形状或点曲线最多可以有 5000 个顶点。
* 复杂链或复杂形状中的组件数量没有限制。
* DGN 文件中图形组的数量没有限制。
* 栅栏与放置它的视图平行。
* 单行文本可包含 65,535 个字符。
* 文本节点的最大大小没有限制。
* DGN 文件中文本节点的数量没有限制。
* 每个元素都有一个唯一的 64 位标识符，该标识符在元素的生命周期中不会改变。
* 每个元素都有一个时间戳，指示最近更改的时间。

## 参考

* [DNG - 维基百科](https://en.wikipedia.org/wiki/DGN)
* [MicroStation V8 DGN 文件格式](https://web.archive.org/web/20120713013730/http://docs.bentley.com/ko/MicroStation/ustnhelp47.html)


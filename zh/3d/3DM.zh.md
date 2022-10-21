{
  "date" : "2021-08-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3DM",
  "description":"了解 3DM 文件格式和可以打开和创建 3DM 文件的 API。",
  "linktitle" : "3DM",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-08-13"
}

## 什么是 3DM 文件？

扩展名为 .3dm 的文件是一种用于 3D 图形软件的开源文件格式。它包含 3D 模型及其相关元素，例如曲面、点和曲线信息。 3DM 文件格式由 [openNURBS](https://github.com/mcneel/opennurbs) 倡议开发，用于在应用程序之间准确传输 3-D 几何图形。可以使用 Rhinoceros、SAP VEViewer、Moment of Inspiration 和 Right Hemisphere Deep View 等应用程序打开和转换 3DM 文件。

## 3DM 文件格式

[openNURBS](https://github.com/mcneel/opennurbs) 是一个开源工具包，包含 3DM 文件格式规范、文档、C++ 源代码库和用于读取和写入文件格式的 .NET 2.0 程序集。

### 3DM 示例文件

可以从 openNURBS [examples](https://github.com/mcneel/opennurbs/tree/7.x/example_files) 部分下载一些示例 3DM 文件。这些可以使用 openNURBS 工具包加载和显示。

## 如何读取或写入 3DM 文件？

[openNURBS](https://github.com/mcneel/opennurbs) 库允许任何人在不需要 Rhino 的情况下读取和写入 3DM 文件格式。它为将使用 openNURBS 文件格式读取和写入 3D 模型的库提供 C++ 源代码。该工具包还提供 NURBS 评估工具和基本几何和 3D 视图操作工具，以及包括几个示例程序的源代码。 [Rhinoceros](https://discourse.mcneel.com/c/opennurbs/6) 支持论坛是一个内容丰富的讨论场所，可以分享3DM社区面临的问题并获得解决方案。

## 参考 ＃＃

* [犀牛](https://www.rhino3d.com/download/openNURBS)
* [犀牛 - 维基百科](https://en.wikipedia.org/wiki/Rhinoceros_3D)
* [GitHub 上的 openNURBS](https://github.com/mcneel/opennurbs)


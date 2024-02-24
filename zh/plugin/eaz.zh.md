{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "EAZ 文件 - 什么是 EAZ 文件以及如何打开它？",
  "description":"了解 EAZ 文件格式以及可创建和打开 EAZ 文件的 API。",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-ea-zhz"
}
},
  "lastmod" : "2023-12-23"
}

## 什么是 .eaz 文件？

EAZ 文件是 ArcGIS Explorer 使用的加载项文件，ArcGIS Explorer 是 ESRI 开发的用于地图探索、可视化和共享的免费应用程序。它包含一个压缩文件存档，其中包括 [XML file](/web/xml/)、已编译的代码以及加载项所需的支持文件。这些文件用于通过合并新按钮、可停靠窗口和其他扩展来扩展软件的基本功能。

## EAZ 文件格式 - 更多信息

EAZ 文件是通过使用 ArcGIS Explorer SDK 创建的，该 SDK 是一个设计用于在 ArcGIS Explorer 中创建自定义功能的开发工具包。这些文件利用 [ZIP](/compression/zip/) 压缩来有效地打包其内容。在存档的核心，**Addins.xml** 文件位于根目录中，作为一个重要组件，概述并详细介绍了 EAZ 文件中嵌入的各种自定义设置。

Addins.xml 文件本质上充当路线图，提供有关 EAZ 文件向 ArcGIS Explorer 引入的特定增强功能、修改和扩展的见解。通过这种综合结构，开发人员可以封装并无缝集成新功能、按钮和可停靠窗口，从而增强 ArcGIS Explorer 应用程序的整体功能和用户体验。

## 参考

 * [Sharing and installing add-ins](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)

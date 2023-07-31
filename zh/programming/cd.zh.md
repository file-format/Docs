{
  "date" : "2020-01-10",
  "keywords" :[ "cd", ".cd","什么是 cd 文件","如何打开 cd 文件", "扩展名", "文件", "cd 文件","cd 文件格式", "cd 文件扩展名" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CD - Visual Studio 类图文件",
  "description":"了解 CD 文件格式和可以创建和打开 CD 文件的 API。",
  "linktitle" : "CD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-24"
}

## 什么是 CD 文件？

扩展名为 .cd 的文件是一个 Visual Studio 类图文件，它提供有关当前解决方案中所有类之间的结构和关系的信息。 Visual Studio 解决方案（由 [.sln](/zh/programming/sln/) 表示）可能包含一个或多个项目，每个项目都有多个不同的类。可以通过右键单击项目并选择类图选项来生成类图文件。

## 类图 (.cd) 文件格式 - 更多信息

类图文件以标准 XML 文件格式保存，将项目中的类表示为 XML 节点。如果 Visual Studio 不可用，则可以在任何支持打开 XML 文件的应用程序中打开这些类图文件。

### 如何将类图添加到 Visual Studio 项目

在 Visual Studio 中，打开要为其添加类图的解决方案/项目。然后，右键单击项目节点，然后选择 Add > New Item。或者，按 Ctrl+Shift+A。

* 添加新项目对话框打开。

* 展开 Common Items > General，然后从模板列表中选择 Class Diagram。对于 Visual C++ 项目，在实用程序类别中查找类图模板。

### 将类图 (CD) 导出到图像

Visual Studio 允许将类图转换/导出为图像，例如 [PNG](/zh/image/png/)、[JPEG](/zh/image/jpeg/) 和 [BMP](/zh/image/bmp/)。这些导出的类图文件可用于文档和技术数据包 (TDP) 记录保存目的。要将类图转换为图像，可以在 Microsoft Visual Studio 中使用以下步骤。

1. 打开您的类图 (.cd) 文件。
1. 从类图菜单或图面快捷菜单中，选择将图导出为图像。
1. 选择一个图表。
1. 选择您想要的格式。
1. 选择导出完成导出。

## 参考

* [Visual Studio 中的设计类](https://learn.microsoft.com/en-us/visualstudio/ide/class-designer/designing-and-viewing-classes-and-types?view=vs-2019)


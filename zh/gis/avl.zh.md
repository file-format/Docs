{
  "date" : "2022-11-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AVL - ArcView 图例文件",
  "description":"了解 AVL 文件格式和可以创建和打开 AVL 文件的 API。”,
  "linktitle" : "AVL",
  "menu" : {
    "docs" : {
      "identifier":"gis-avl",
      "parent" : "gis"
}
},
  "lastmod" : "2022-11-30"
}

## 什么是 .avl 文件？

AVL 文件是一个图例文件，其中包含使用 ESRI ArcView GIS（地理信息系统）软件生成的地图的键。它包含相应地图中用于访问的参考符号系统信息。 AVL 文件可以包含更多信息，例如符号系统、显示设置（例如透明度）、比例相关显示属性、连接表/相关表信息、定义查询、要素图层的标注属性以及注释图层的注释显示属性，具体取决于类型一种层。

可以从 ArcView 项目 [.APR](/zh/gis/apr/) 文件中引用 AVL 文件。

## AVL 文件格式 - 更多信息

AVL 文件以纯文本文件格式保存。这意味着您可以在任何文本编辑器（如记事本、Notepad++ 和 Apple TextEdit）中打开 AVL 文件。打开后，您不仅可以查看文件内容，还可以修改这些内容。

### .LYR 和 .AVL 文件的区别

* **文件格式差异** - .lyr 是二进制文件，而 .avl 是文本文件
* **内容差异** - .lyr 文件比 .avl 文件包含更多信息。 AVL 文件仅存储符号系统信息，而 LYR 文件存储 ArcMap 图层属性对话框中可用的所有信息。

## 参考

* [.lyr 和 .avl 文件之间的区别](https://support.esri.com/en/technical-article/000005936)


{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RML - Elixir 报告模板文件",
  "description":"了解 RML 文件和可以创建和打开 RML 文件的 API。",
  "linktitle" : "RML",
  "menu" : {
    "docs" : {
"标识符":"misc-rml",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## 什么是一 .rml 文件？

RML 文件是带有 [Elixir Repertoire](https://elixirtech.com/repertoire-2/) 报告引擎的报告模板文件。模板文件用于生成数据源连接到 Elixir 文件系统的报告。数据在 RML 模板文件中读取和填充，并且可以导出为多种不同的文件格式，例如 [PDF](/zh/pdf/)、[RTF](/zh/word-processing/rtf/) 和电子表格 [XLS] （/电子表格/xls/）。 Elixir Repertoire 报告引擎可以连接到各种 JDBC 数据源。

## RML 文件格式

RML 文件格式的内部文件结构细节不公开。这些文件由 Elixir Repertoire 应用程序在内部生成和保存，以生成包含从连接的数据源填充的数据的报告。 RML 模板文件包含要从数据生成的最终报告的总体布局和占位符信息。

## 如何生成 RML 模板文件？

为了在 Elixir Repertoire 中生成 RML 模板，可以遵循以下步骤。

1. 将 JDBC 数据源连接到文件系统。
1. 启动报告模板向导
1.使用软件定位数据源.ds文件
1.选择表格报告作为导出的选择
1.选择要包含在报告模板中的字段
1. 最后，单击 Finish 按钮，First report.rml 添加到存储库并打开以显示 Layout 选项卡。

## 参考

* [Elixir Repertoire](https://elixirtech.com/repertoire-2/)


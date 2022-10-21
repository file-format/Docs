{
  "date" : "2022-05-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 FMPSL 文件格式和可以创建和打开 FMPSL 文件的 API。",
  "title" :"FMPSL 文件格式 - FileMaker Pro 12 快照链接文件",
  "linktitle" : "FMPSL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-25"
}

## 什么是一 .fmpsl 文件？

FMPSL 文件是使用 FileMaker Pro 12 创建的数据库快照文件。它存储来自数据库的查询结果以及其他信息，例如视觉布局和可见信息。 FMPSL 文件可用于在 FileMaker Pro 数据库的另一个实例中恢复所有这些数据。此文件格式是随着 FileMaker Pro v 12 的推出而引入的。在此版本之前，快照链接在 FileMaker Pro v 11 中以 FPSL 文件格式引入。FMPSL 文件可以使用 FileMaker Pro Advanced 软件打开。 FileMaker Pro 支持的其他文件格式包括 [FP5](/zh/database/fp5/)、[FP7](/zh/database/fp7/) 和 [FMP12](/zh/database/fmp12/)。

## FMPSL 文件格式

FMPSL 文件的内部文件格式详细信息不公开供开发人员参考。

### 如何将记录保存为 FMPSL 文件？

FileMaker Pro 数据库中的数据可以使用以下步骤保存为快照链接文件。

1. 从数据库中查找需要保存为快照链接文件的记录。
1. 使用菜单中的“将记录作为快照链接发送"选项，通过输入文件名保存文件。
1. 使用正在浏览的记录来保存整个找到的记录集。

生成的快照文件将以指定的名称保存到光盘中。

## 参考

* [将早期版本的 FileMaker Pro 文件格式转换为 FMP12 文件格式](https://fmhelp.filemaker.com/help/16/fmp/en/index.html#page/FMP_Help/converting-files.html)
* [将记录保存为快照链接文件](https://fmhelp.filemaker.com/help/12/fmp/en/html/import_export.17.5.html)


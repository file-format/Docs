{
  "date" : "2019-12-16",
  "keywords" :["NB","文件","扩展名","文件格式","Mathematica","电子表格"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解什么是可以创建和打开 NB 文件的 NB 文件 API。",
  "title" :"NB - Mathematica Notebook 文件格式",
  "linktitle" : "NB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-07-16"
}

## 什么是一 .NB 文件？

具有 .nb 扩展名的文件是 Wolfram 笔记本文件格式，它将数学指令的指令保存在文本文件中.它可以包含许多不同类型的数据，例如实时计算、任意动态接口、完整排版输入、图像输入、自动代码注释、完整的高级编程接口以及数千个精心组织的功能和选项。文本指令是 Mathematica 输入和输出，在输入语句放入文件时生成和更新。

## Wolfram Notebook NB 文件格式 - 更多信息

Wolfram Notebook NB 文件以纯文本格式保存，这是一种人类可读的文件格式。笔记本的内容以纯文本形式排列在多个部分中，其中每个部分由一组单元格表示，类似于电子表格。这些组的范围由每个单元格末尾的括号定义。分配给单元格的样式决定了它在笔记本中的角色，如下所述。

### 笔记本作为 Wolfram 语言

当打算保存由 Wolfram 语言内核执行的数学指令组成的 Notebook 时，文档中的单元格会自动分配 `Input` 文本样式.这告诉内核将这些视为在用户发出“Shift+Return"组合键时执行的指令。 Mathematica Notebook 如下例所示。

{{< figure src="../Wolfram Notebook.jpeg" alt="Wolfram 笔记本文件格式" >}}

### 笔记本作为文档

Mathematica Notebooks 可以采用文档格式，让您了解所见即所得 (WYSIWYG)。这些文档与在屏幕上或在打印纸上查看的文档相同，并且是交互式的。为此，将“文本样式"分配给单元格以显示内容，而无需执行内核的语句。

## 导出 Mathematica 笔记本

Mathematica Notebooks 可以导出为多种不同的文件格式，例如 PDF、图形、GIS、压缩和电子表格。

## 参考

* [Mathematica Notebook 基础知识](https://reference.wolfram.com/language/guide/NotebookBasics.html)


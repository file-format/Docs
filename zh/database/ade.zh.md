{
  "date" : "2021-08-29",
  "keywords" :["ade","扩展名","文件","文件格式","数据库文件类型","数据库文件格式","Microsoft Access"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 ADE 文件格式和可以创建和打开 ADE 文件的 API。",
  "title" :"ADE - 访问项目扩展文件",
  "linktitle" : "ADE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-29"
}

## 什么是一 .ade 文件？

带有 .ade 扩展名的文件是一个 Microsoft Access 项目文件，其中包含 Microsoft Access ADP 项目文件中包含的信息的编译输出。 Access 项目文件中的信息（除 Visual Basic for Applications (VBA) 外）在 ADE 文件中以编译形式提供。数据以压缩格式存储在这些文件中，以减小文件大小并提高 Access 的性能。由于 ADE 是 Access 项目文件的编译输出，因此作为项目一部分的任何 VBA 源代码都通过不允许它成为输出的一部分而受到保护。 ADE 文件可以在 Microsoft Access 365 中打开。

## ADE 文件格式 - 更多信息

ADE 是已编译的 Access 数据库文件，它们以二进制文件的形式存储到光盘中。这些文件的内部文件结构未知。

ADE 文件可能会根据用于创建这些文件的 Microsoft Access 版本在打开时产生问题。使用 64 位版本的 Microsoft Access 2010 并编译为 MDE、[ACCDE](/zh/database/accde/) 或 ADE 文件的 Access 数据库必须在 Microsoft Access 2021 Service Pack 1 (SP1) 中重新编译以与 Access 2010 SP1 一起正常工作。出现此问题的原因是 Access 2010 SP1 使用较新版本的 VBE7.dll 文件（版本 7.00.1619）。

## 参考

* [访问 ADE 文件的问题](https://learn.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)
* [使用哪种访问文件格式](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)


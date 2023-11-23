{
"日期":"2023-11-09",
   "keywords":[
"动物园",
"动物园文件",
"动物园压缩文件",
"如何打开动物园文件",
"文件",
"动物园文件扩展名",
"扩大",
"文件"
],
   "author":{
"display_name":"沙基尔·法伊兹"
},
"draft": "false",
"toc": true,
"title":"ZOO 文件 - 什么是 .zoo 文件以及如何打开它？",
   "description":"了解 ZOO 压缩文件格式以及可以创建和打开 ZOO 文件的 API。",
"linktitle":"ZOO",
   "menu":{
      "docs":{
         "identifier":"compression-zoo",
"parent": "compression"
}
},
"lastmod": "2023-11-09"
}

## 什么是 .zoo 文件？

`.zoo` 文件是一种存档格式，用于压缩和存储文件和目录；类似于其他存档格式，如“.zip”、“.tar”和“.rar”。 “.zoo”格式在计算早期很流行，但近年来已变得不那么常见。它最初由 **Rahul Dhesi** 开发，主要用于 Unix 和 DOS 系统。

“.zoo”文件通常包含一个或多个已压缩并存档为单个文件的文件和目录。您可以使用支持此格式的各种软件工具创建和提取“.zoo”文件。

ZOO 档案有一个独特的功能，允许它们存储同一文件的多个版本，前提是每个版本在不同日期进行修改。这意味着 ZOO 用户可以直接从 ZOO 存档保存和访问文件的先前版本。此功能使用户能够恢复到文件的早期版本或将旧版本与最新版本进行比较，从而提供了管理文件修订和随时间变化的便捷方法。

## ZOO文件的常用操作

以下是与“.zoo”文件相关的一些常见操作：

1. **创建`.zoo`文件：**您可以使用“zoo”等命令行实用程序来创建`.zoo`文件。例如，以下命令将从目录创建“.zoo”存档：
    








`zoo a -c archive.zoo 目录/`
    








在此命令中，“a”代表“add”，“-c”指定压缩，“archive.zoo”是输出存档的名称。
    








2. **从 `.zoo` 文件中提取文件：** 要提取 `.zoo` 存档的内容，您可以使用如下命令：
    








`动物园和档案.zoo`
    








此命令将从“archive.zoo”文件中提取文件。
    








3. **列出 `.zoo` 文件的内容：** 您可以列出 `.zoo` 存档的内容，而无需使用“l”选项提取它们：
    








    








`zoo l archive.zoo`

## 如何打开 .ZOO 文件？

打开 ZOO 文件的程序包括

- **zoo**（免费）适用于（Windows、Linux）

## 参考
* [Zoo (file format)](https://en.wikipedia.org/wiki/Zoo_(file_format))

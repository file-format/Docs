{
  "date" : "2019-10-11",
  "keywords" :["pot 文件","pot 文件格式","什么是 pot 文件","文件","pot 示例","pot 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"POT - Microsoft PowerPOint 模板文件格式",
  "description":"了解 POT 文件格式和可以创建和打开 POT 文件的 API。",
  "linktitle" : "POT",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .pot 文件？

带有 .POT 扩展名的文件代表由 PowerPoint 97-2003 版本创建的 Microsoft PowerPoint 模板文件。与使用更高版本的 PowerPoint 以 Office OpenXML 文件格式创建的文件相比，使用这些版本的 Microsoft PowerPoint 创建的文件是二进制格式。因此，生成的文件可用于创建具有相同布局和其他需要应用于新文件的设置的演示文稿。这些设置可以包括样式、背景、调色板、字体和默认值。生成此类文件是为了创建可供正式使用的即用型模板文件。

## 文件格式规范##

Microsoft 不单独提供 POT 文件格式的文件格式规范。但是，模板格式与二进制 [PPT](/zh/presentation/ppt/) 文件格式相同，可以在 MS PowerPoint 中打开进行编辑。 POT 文件由 HEX 标识符标识，如下所示：

```
D0 CF 11 E0 A1 B1 1A E1 00 00 00 00
```

与 POT 文件格式相关的 MIME 类型是：

* application/vnd.ms-powerpoint [官方]
* 应用程序/mspowerpoint
* 应用程序/x-mspowerpoint
* 应用程序/PowerPoint
* 应用程序/x-powerpoint
* 应用程序/x-dos_ms_powerpnt
* 应用程序/锅
* 应用程序/x-soffic

## 参考 ＃＃

* [PPT文件格式规范](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)
* [[MS-OSHARED]：Office 常用数据类型和对象结构](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)
* [[MS-OFFCRYPTO] - Office 文档加密结构](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)
* [PowerPoint 文件格式](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)


{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 FZP 文件格式和可以创建和打开 FZP 文件的 API。",
  "title" :"FZP 文件格式 - Fritzing XML 部件描述文件",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## 什么是一 .fzp 文件？

FZP 文件是由 [Fritzing](https://fritzing.org/) 电子电路原型设计和设计应用程序创建的 XML 文件。它以 [XML](/zh/web/xml/) 文件格式包含有关部件属性、连接器和总线的信息。 FPZ 文件不能在 Fritzing 中独立使用。相反，它们作为 FZPZ 存档文件的一部分导入。

## FZP 文件格式 - 更多信息

FZP 文件是 XML 文件，其中包含有关部件属性、连接器和总线的信息。除了这些，FZP 文件还包含有关 FZP 文件的标题、描述、作者和发布日期的信息。导出 Fritzing 零件文件时，Fritzing 应用程序会创建一个 [FZPZ](/zh/compression/fzpz/) 压缩存档，其中包含一个 FZP 文件和四个 [SVG](/zh/page-description-language/svg/) 文件。

[FZP 文件格式规范](https://github.com/fritzing/fzp/blob/master/docs/README.md) 由 Fritzing 在 Github 上提供。

## FZP 文件结构示例

典型的 FZP 文件具有以下 XML 结构。

```
<?xml version="1.0" encoding="UTF-8"?>
<module fritzingVersion="x.y.z" moduleId="mod-id-rev" referenceFile="ref.file">
  <version>x.y.z</version>
  <title>part-name</title>
  <description>some words about the part</description>
  <author>your-name</author>
  <date>yyyy-mm-dd</date>
  <url>http://part.org</url>
  <label>IC</label>
  <tags>...</tags>
  <taxonomy>...</taxonomy>
  <language>...</language>
  <family>...</family>
  <variant>...</variant>
  <properties>...</properties>
  <views>...</views>
  <connectors>...</connectors>
  <buses>...</buses>
</module>
```
## 参考

* [FZP 文件格式规范](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [带有 fzpz 扩展的新部件](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)


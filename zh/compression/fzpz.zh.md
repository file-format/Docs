{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FZPZ 文件格式 - Fritzing 零件文件",
  "description":"了解什么是 FZPZ 文件以及可以创建和打开 FZPZ 文件的 API。",
  "linktitle" : "FZPZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-20"
}

## 什么是一 .fzpz 文件？

FZPZ 文件是使用电路原型和设计应用程序**Fritzing** 创建的电子电路设计中使用的组件/零件。它是一个压缩档案，包含一个 [FZP](/zh/cad/fzp/) 文件和四个描述 Fritzing 整体部分的 [SVG](/zh/image/svg/) 图像。使用这些文件的优势在于，从可重用性的角度来看，用户可以与每个文件共享他们的 FZPZ 文件。 FZPZ 零件的共享有助于集成电路零件以快速创建更大的 PCB 设计。

## FZPZ 文件格式 - 更多信息

FZPZ 文件作为压缩的 [ZIP](/zh/compression/zip/) 档案保存到光盘。您可以将扩展名从 .fzpz 重命名为 .zip 并使用任何标准解压缩实用程序（例如 WinZIP）从存档中提取文件。

### FZPZ 文件结构信息

如前所述，FZPZ 文件是一个存档文件，其中包含用于表示印刷电路板中使用的零件的多个文件。 FZPZ 包含以下文件：

* `四个 SVG 文件` - 代表零件的面包板、原理图、PCB 和图标图像
* `FZP 文件` - 包含有关部件属性、连接器和总线信息的 XML 文件

这些文件通常命名如下。

* part.file.fzp
* svg.breadboard.file.svg
* svg.icon.file.svg
* svg.pbc.file.svg
* svg.schematic.file.svg

## 参考 ＃＃

* [带有 fzpz 扩展的新部件](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)


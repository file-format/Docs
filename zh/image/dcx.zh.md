{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DCX - Zsoft 多页画笔文件",
  "description":"了解 DCX 文件格式和可以创建和打开 DCX 文件的 API。",
  "linktitle" : "DCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## 什么是一 .dcx 文件？

DCX 文件是由用于生成数字传真文件的多页组成的图像文件。每个 DCX 文件都以一个 4 字节的标头开始，将 DCX 文件标识为签名，然后是单个图像，存储为嵌入的 [PCX](/zh/image/pcx/) 文件。 4 字节签名标识 DCX 文件，其后是最多 1023 个 4 字节文件偏移的列表。 DCX 文件格式由 Zsoft 开发。一些应用程序可以打开 DCX 文件，例如 Adobe Photoshop、Corel PaintShop Pro 和 IrfanView。

## 参考

* [PCX - 维基百科](https://en.wikipedia.org/wiki/PCX)
* [ZSoft PCX 文件格式技术参考手册](http://qzx.com/pc-gpe/pcx.txt)


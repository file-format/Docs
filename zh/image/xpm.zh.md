{
  "date" : "2019-10-11",
  "keywords" :["xpm 文件","xpm 文件格式","什么是 xpm 文件","文件","xpm 示例","xpm 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPM - X PixMap 文件格式",
  "description":"了解 XPM 文件格式和可以创建和打开 XPM 文件的 API。",
  "linktitle" : "XPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .xpm 文件？

扩展名为 .xpm 的文件是 X Windows 系统使用的一种图像文件格式。它支持透明像素，通常以创建图标像素图为目标。它支持单色、灰度和彩色像素图数据。这些被设计为可以手动编辑，并且可以包含在 [C](/zh/programming/c/) 代码中。为此，XPM 文件采用纯文本文件格式并遵循 C 编程语言语法。 XPM 文件可以使用各种图像查看应用程序打开，例如
CorelDRAW Graphics Suite 2020、Corel PaintShop Pro、IrfanView 和 Canvas X。

## XPM 文件格式

XPM 文件格式使用 C 语法以便将它们集成到 C 和 C++ 程序中。它由以下六个不同的部分组成。

* \<Values>
* \<Colors>
* \<Pixels>
* \<Extensions>

这些部分实际上是一个字符串数组，如下所示。

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
以下是每个部分的详细信息。

`<Values> ` - 此部分是一个字符串，包含四个或六个以 10 为底的整数，对应于：

* 像素图宽度和高度
* 颜色数
* 每个像素的字符数
* 可选热点坐标和 XPMEXT 标签

`<Colors> ` - 此部分包含与颜色一样多的字符串。每个字符串如下：

```
<chars>{<key><color> }+
```
`<Pixels> ` - 此部分由<height>字符串和<width>\*<chars_per_pixel>人物。每一个<chars_per_pixel>长度字符串应该是之前定义的组之一<Colors>部分。

`<Extension> ` - 扩展部分必须标记，如果它不为空，在<Values>部分。它可能由几个<Extension>可能有以下两种类型的小节：

* 一个独立的字符串组成如下：XPMEXT<extension-name><extension-data>
* 或由多个字符串组成的块：XPMEXT<extension-name><related extension-data composed of several strings>

## 参考

* [XPM - 维基百科](https://en.wikipedia.org/wiki/X_PixMap)
* [XPM 手册](http://www.xfree86.org/current/xpm.pdf)


{
  "date" : "2019-10-11",
  "keywords" :["ico文件","ico文件格式","什么是ico文件","文件","ico示例","ico文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICO - 图像文件格式",
  "description":"了解 ICO 文件格式和可以创建和打开 ICO 文件的 API。",
  "linktitle" : "ICO",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .ico 文件？

带有 ICO 扩展名的文件是图像文件类型，用作在 [Microsoft Windows](https://www.microsoft.com/en-us/windows) 上表示应用程序的图标。它们具有不同的尺寸、颜色支持和分辨率，以满足显示器的要求。 Microsoft Windows 上另一种类似的图像文件格式是 [CUR](/zh/image/cur/) 用于光标表示并在图像标题中定义一个热点。在 MacOS 上，ICNS 文件格式的用途与 ICO 文件相同。一些在线网站和应用程序提供了创建此类文件的功能，并将[BMP](/zh/image/bmp/)、[PNG](/zh/image/png/)等其他图像格式转换为图标文件格式。 ICO 文件的官方 IANA 注册 Internet 媒体类型是 image/vnd.microsoft.icon。

## 历史简介 ＃＃

图标是随着 Microsoft Windows 1.0 的推出而引入的。这些尺寸为 32x32，并且是单色的。随着 win32 的到来，引入了对真彩色图标图像的支持，最大尺寸为 256x256 像素。 Windows XP 是第一个提供对 32 位彩色图标图像的支持，允许将阴影、抗锯齿和玻璃效果等半透明区域添加到图标中。 Microsoft 仅建议 Windows XP 的图标大小最大为 48×48 像素。 Windows Vista 向 Windows 资源管理器添加了 256×256 像素的图标视图，并支持压缩的 [PNG](/zh/image/png/) 格式。对于使用更高分辨率和高 DPI 模式的用户，建议使用更大的图标格式（例如 256×256）。

## ICO 文件格式 ##

单个 ICO 文件由一个或多个具有多种尺寸和颜色深度的小图像组成。存在多种尺寸的图像是为了在不同的屏幕分辨率下进行适当的缩放。 ICO/CUR 文件中的所有值都以 [little-endian](https://en.wikipedia.org/wiki/Little-endian) 字节顺序表示。

ICO 文件由一个图标头、一个图标目录、

|字段|描述
---|---|
|图标标题|存储有关 ICO 文件的一般信息。
|Directory[1..n]|存储文件中每个图像的一般信息。
|Icon #1|旧的 AND/XOR DIB 格式或更新的 PNG 格式的第一张图像的实际“数据"
|...|
|Icon #n|最后一个图标图像的数据

### 标题###

|偏移量|大小（以字节为单位）|用途
---|---|---|
|0|2|保留。必须始终为 0。
|2|2|指定图像类型：1 代表图标 (.ICO) 图像，2 代表光标 (.CUR) 图像。其他值无效。
|4|2|指定文件中的图像数量。

＃＃＃ 目录 ＃＃＃

ICO 文件中包含的目录，表示为 ICONDIR 结构，包含文件中每个图像的 ICONDIRECTORY 结构。紧随其后的是所有图像位图数据的连续块。如下图所示。

|偏移量|尺寸|描述
---|---|---|
|0 (0)|1|宽度，如果是 256 像素，则应为 0
|1 (1)|1|高度，如果是 256 像素，则应为 0
|2 (2)|1|颜色计数，如果超过 256 种颜色，则应为 0
|3 (3)|1|保留，应为 0
|4 (4)|2|.ICO 格式时的颜色平面，应为 0 或 1，或 .CUR 格式时的 X 热点
|6 (6)|2|.ICO 格式时每像素的位数，或 .CUR 格式时的 Y 热点
|8 (8)|4|位图数据的大小，以字节为单位。
|12 (C)|4|文件中的偏移量。

## 参考 ＃＃

* [ICO - 维基百科](https://en.wikipedia.org/wiki/ICO_(file_format))
* [IANA - vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)


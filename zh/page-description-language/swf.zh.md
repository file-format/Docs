{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "keywords" :[ "SWF","文件","扩展名","格式","视频格式","什么是 SWF 文件","swf 文件格式","swf 文件播放器","如何打开 swf 文件"] ,
  "title" :"SWF 文件 - Shockwave Flash 电影文件格式",
  "description":"了解什么是 SWF 文件以及可以创建和展示如何打开 SWF 文件的 API。",
  "linktitle" : "SWF",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是 .swf 文件？

SWF 文件是使用 Adobe Flash 创建的动画文件。它可能包含不同类型的元素，例如文本、矢量图像、光栅图像、动作脚本、对象（例如圆、线、正方形和矩形）来创建动画。 SWF 文件将这些多媒体项目排列在可以以不同的每秒帧数 (fps) 播放的帧中。 SWF 表示短 Web 文件，但也称为 Shockwave 格式。

可以*打开 SWF 文件**的应用程序包括 Adobe Flash Player（现已停产）和 Eltima Elmedia Player。

## SWF 文件格式 - 更多信息

SWF 文件用于以二进制文件的形式存储到光盘中。 SWF 文件格式用于开发可以嵌入网站并独立播放的动画和游戏。它还支持视频和声音，为开发人员提供了许多创建交互式多媒体应用程序的选择。 SWF 文件可以在安装了 Adobe Shockwave 的网络浏览器中播放。 Adobe Flash 由于存在缺陷和安全问题，已于 2020 年 12 月停产。

## SWF 文件格式简史

SWF 文件格式最初由 FutureWave Software 设计，旨在显示动画，以便在任何网络连接速度较慢的系统上的播放器软件上运行，同时保持文件较小。 1996 年 12 月，Macromedia 拥有 FutureWave 并转换为 Macromedia Flash 1.0。

2005 年，Macromedia 被 Adobe 收购，后者于 2008 年宣布将 SWF 作为其开源项目的一部分。同年，Adobe 向世界流行的 Web 引擎发布代码，以允许它们对 SWF 文件进行爬取和索引。但是，由于 SWF 文件似乎已成为在 Internet 上发布 Flash 内容的标准格式，因此 SWF 已被修改为小型 Web 格式。

## SWF 文件结构

路径是 SWF 中的基本图形元素，它是一系列基本元素的片段，从简单的线条到贝塞尔曲线。这些简单的元素还有助于制作其他额外的基元，如立方体、椭圆甚至文本。 SWF 中的图形基元与 SVG 和 MPEG-4 BIFS 等其他格式的图形元素有相似之处。

该格式还允许显示列表和重用/重命名已定义的元素。 SWF 的二进制流格式可以与在标签、大小和有效负载方面相似的 QuickTime 原子进行比较。二进制流格式允许老玩家跳过不支持的内容。虽然原始版本的 SWF 仅限于提供矢量图形和图像，但新版本也允许音频和视频内容。

版本 11 中引入了名为“Stage3D"的新的 Flash Player 低级 3D API。该 API 被设想为 OpenGL 或 Direct3D 的对应物。 Stage3D 使用称为 Adobe 图形汇编语言 (AGAL) 的低级语言定义颜色。以下是 SWF 文件格式的几个基本数据类型。

### 坐标

SWF 文件格式的 XY 坐标以整数形式存储，并以缇为单位进行测量。缇由逻辑像素的 1/20 组成。当文件没有以 100% 缩放时，逻辑像素和屏幕像素是相同的。

### 整数类型和字节顺序

SWF 文件格式中允许使用 8、16、32 和 64 位的有符号和无符号整数类型。 Little-endian 字节顺序用于存储整数值。虽然在字节内，但位顺序存储在大端。所有整数值都应该是字节对齐的。有符号整数使用传统的 2 补码位模式表示。

### 定点数

SWF 文件格式支持两种类型的定点数，即 32 位和 16 位。

＃＃＃ 浮点数字

SWF 8 及更高版本使用与 IEEE 标准 754 浮点类型兼容的三种浮点数（FLOAT、FLOAT 16、DOUBLE）。

### 编码整数

SWF 9 及更高版本支持一种类型的编码整数，其字节数可变。

## 参考

* [SWF 文件格式](https://en.wikipedia.org/wiki/Swf)


{
  "date" : "2019-12-12",
  "keywords" :["EPS","文件","扩展名","文件格式","页面布局","封装 PostScript"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 EPS 文件格式和可以创建和打开 EPS 文件的 API。",
  "title" :"EPS 文件格式 - 封装的 PostScript 文件",
  "linktitle" : "EPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .eps 文件？

.eps 文件是以 Encapsulated Postscript 文件格式保存到光盘的图像文件。它可能包含文本、图形和图像的任意组合。 EPS 文件还可能包含封装在内部的位图预览图像，以供可以打开此类文件的应用程序显示。

## EPS 文件格式简史

从历史的角度快速查看 EPS 文件格式会发现以下信息：

* EPS 的第一个版本由 Adobe 于 1985 年至 1988 年之间的某个时间发布
* EPS 规范 2.0 版于 1989 年 1 月发布
* EPS 3.0 版本的规范于 1992 年作为单独的文件发布；这是最新发布的版本。

EPS 与 Adobe 的 PostScript 语言文档结构约定规范第 9 条中描述的开放结构约定扩展机制相结合，形成了早期版本的 Adobe Illustrator 图稿文件格式的基础。

## EPS 文件格式

EPS 是一种专有但公开记录的格式，EPS 文件格式规范可供开发人员参考。 EPS 是符合 [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions)（文档结构约定）的文件格式，并遵守 DSC 制定的所有规则。 DSC 是 Adobe 用于 PostScript 文档的一种特殊文件格式。任何声称能够读取 EPS 文件的应用程序都应符合 DSC。

EPS 文件由两个主要部分组成，如下所述。

### 预览图像###

一个典型的 EPS 文件包含一个预览图像，其格式旨在方便在涉及多个系统或应用程序的工作流中使用。预览的目的是获得大多数图形应用程序可以呈现的格式的图像；预览通常具有较低的分辨率、像素尺寸和/或位深度。预览文件可以是多种格式之一。 EPS_3 规范列出了三种“特定于设备"的预览格式：

* 对于 Apple Macintosh，QuickDraw 应用程序使用的 PICT 图像
* 对于 DOS 计算机，一个 TIFF 位图
* Windows 元文件。

PICT 和 Windows Metafile 可以合并位图数据和矢量图形。此外，该规范为嵌入式位图预览图像定义了一种非常简单的与设备无关的表示。这种表示称为封装 PostScript 交换格式 (EPSI)。

EPSI 预览是表示为 ASCII 十六进制的位图，包裹在几个 PostScript 注释之间以进行识别，旨在简单且易于传输。为了区分不同预览格式的 EPS 文件，EPS 规范中推荐了不同的 DOS 文件扩展名和 Macintosh 文件类型。

### PostScript 代码

EPS 文件格式至少必须包括以下内容：

* 标题注释，%!PS-Adobe-3.0 EPSF-3.0
* 和一个边界框注释 %%BoundingBox: llx lly urx ury，它描述了插图的边界。这四个参数对应于边界框的左下角 (llx, lly) 和右上角 (urx, ury)。

EPS 文件不能使用以下任何运算符：

* 带设备，
* 清除字典堆栈
* 复制页
* 擦除页
* 退出服务器
* 框架设备
* grestoreall
* 初始剪辑
* 初始图形
* 初始化矩阵
* 退出
* 渲染带
* 全局设置
* 设置页面设备
* 设置共享
* 开始工作。

## 将 EPS 转换为其他文件格式

EPS 文件可以转换为标准图像格式，例如 [JPG](/zh/image/jpeg/)、[PNG](/zh/image/png/)、[TIFF](/zh/image/tiff/) 和 [PDF](/zh/pdf /) 使用不同的应用程序，例如 Adobe Illustrator、Photoshop 和 PaintShop Pro。

由于 [安全漏洞](https://support.office.com/en-us/article/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e- a1b5-cbb0c334a840) 在 EPS 文件中，Office 2016、Office 2013、Office 2010 和 Office 365 已关闭将 EPS 文件插入 Office 文档的功能。

## 参考

* [Encapsulated PostScript - 来自维基百科](https://en.wikipedia.org/wiki/Encapsulated_PostScript)


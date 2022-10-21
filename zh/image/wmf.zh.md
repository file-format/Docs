{
  "date" : "2019-10-11",
  "keywords" :["wmf 文件","wmf 文件格式","什么是 wmf 文件","文件","wmf 示例","wmf 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMF - Microsoft Windows 元文件格式",
  "description":"了解 WMF 文件格式和可以创建和打开 WMF 文件的 API。",
  "linktitle" : "WMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .wmf 文件？

带有 WMF 扩展名的文件代表 Microsoft Windows 元文件 (WMF)，用于存储矢量以及位图格式的图像数据。更准确地说，WMF 属于与设备无关的图形文件格式的矢量文件格式类别。 Windows 图形设备接口 (GDI) 使用存储在 WMF 文件中的函数在屏幕上显示图像。后来发布了 WMF 的更增强版本，称为增强元文件 (EMF)，使该格式的功能更加丰富。实际上，WMF 类似于 SVG。

## WMF 文件格式规范 ##

WMF 文件在与 Windows 3.0 一起启动时指的是 16 位文件格式。文件格式由一系列可变长度记录组成，这些记录包含图形绘制命令、对象定义和属性。由于 WMF 文件基于渲染到 GDI 以绘制图像的命令，因此它也称为图像的数字记录，可以回放以再现该图像。 WMF 的完整文件格式规范可在线获得，应参考开发使用 WMF 文件的应用程序。 WMF 文件被组织成：

* WMF 标头记录
* WMF 记录
* WMF 文件结束记录

### WMF 标头记录###

**META_HEADER Record** 包含定义元文件特征的信息，包括：

* 图元文件的类型
* 元文件的版本
* 图元文件的大小
* 图元文件中定义的对象数量
* 图元文件中最大单条记录的大小

### WMF 可放置标题记录###

**META_PLACEABLE Record** 包含有关图像的扩展信息，包括：

* 一个边界矩形
* 逻辑单元大小，用于缩放
* 校验和，用于验证

### WMF 记录###

WMF 记录具有通用格式，在规范文档中指定。每个 WMF 记录都包含以下信息：

* 记录大小
* 记录功能
* 记录函数的参数，如果有的话

## 参考 ＃＃

* [[MS-WMF]：Windows 元文件格式](https://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [Windows 元文件 - 维基百科](https://en.wikipedia.org/wiki/Windows_Metafile)


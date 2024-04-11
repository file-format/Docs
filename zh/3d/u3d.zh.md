{
  "date" : "2019-10-11",
  "keywords" :["u3d 文件","u3d 文件格式","什么是 u3d 文件","文件","u3d 示例","u3d 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"U3D - 通用 3D 文件格式",
  "description":"了解 U3D 文件格式和可以打开和创建 U3D 文件的 API。",
  "linktitle" : "U3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .u3d 文件？

**U3D**（通用 3D）是一种用于 3D 计算机图形的压缩文件格式和数据结构。它包含 3D 模型信息，例如三角形网格、照明、阴影、运动数据、具有颜色和结构的线和点。该格式于 2005 年 8 月被接受为 [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) 标准。3D [PDF](/zh/pdf/) 文档支持 U3D对象嵌入并可在 Adobe Reader（版本 7 及更高版本）中查看。开发 U3D 格式的目的是建立一个通用的三维数据存储和交换标准。但是，该格式主要用于 3D PDF 的编码，而不是用作交换格式。 Acrobat 3D 在转换为 PDF 时将支持的 3D 文件类型转换为 U3D 或 PRC。

## U3D 文件格式

U3D 文件是二进制文件格式，如 [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) 参考文档所述，经历了四个版本，导致规范更新每个版本。 PDF 文件标准 ISO-32000 接受 U3D 作为允许的注释和多媒体类型。

U3D 的第一版侧重于 3D 图形属性的关键表示，例如几何、颜色、纹理、照明、骨骼和基于变换的动画。第二版和第三版更正了第一版的一些勘误，第三版是行业软件中最常用的类型。第四版提供了高阶图元（曲面）的定义。 [U3D 规范](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) 在 ECMA 网站上可供用户参考。

### U3D 文件中的数据类型

二进制文件将包含以下类型：U8、U16、U32、U64、I16、I32、F32、F64 和字符串。

* U8 : 无符号 8 位整数
* U16 : 无符号 16 位整数
* U32 : 无符号 32 位整数
* U64 : 无符号 64 位整数
* I16 : 有符号的 16 位整数
* F32：IEEE 单精度浮点数。
* F64：IEEE 双精度浮点数。
* 字符串：U3D 文件中的字符串以一个无符号的 16 位整数开头，该整数定义字符串中字符的总长度。字符串始终被处理为区分大小写。

## U3D 文件结构

U3D 文件包含一系列块。每个 U3D 文件中有 3 种不同类型的块。

* 文件头块
* 声明块
* 继续块

如果不需要该块中的数据或该块类型的解码器不可用，则加载程序确定该块的结尾。

{{< figure src="../u3d.png" alt="U3D 文件格式" >}}

### 文件头块
文件头块包含文件信息，加载程序使用这些信息来确定如何读取文件。

### 声明块

声明块包含有关文件中对象的信息。必须定义声明块中的对象。

### 继续块

在声明块中声明的对象的附加信息在延续块中提供。每个延续块必须与一个声明块相关联。


## 参考 ＃＃

* [U3D 文件格式 - 维基百科](https://en.wikipedia.org/wiki/Universal_3D)
* [ECMA U3D File Format Specifications](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/)


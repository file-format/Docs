{
  "date" : "2019-10-11",
  "keywords" :["gbr 文件","gbr 文件格式","什么是 gbr 文件","文件","gbr 示例","gbr 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GBR 文件格式 - PCB 的 Gerber 文件格式",
  "description":"了解 GBR 文件格式和可以创建和打开 GBR 文件的 API。",
  "linktitle" : "GBR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .gbr 文件？

扩展名为 .gbr 的文件是一种 Gerber 图像文件格式，用于交换印刷电路板 (PCB) 设计数据传输。它是由 Ucamco 开发的。 PCB设计数据是制造行业处理所需的主要组成部分。 GRB 文件包含 PCB 数据，例如铜层、阻焊层、图例以及钻孔和布线数据。它可用于以标准化格式传输诸如 PCB 制造特性（包括厚度或光洁度）之类的数据。所有 PCB 设计系统都输出可由 PCB 制造系统处理的 Gerber 文件。 GBR 文件现已成为印刷电路板 (PCB) 设计数据传输的事实标准。 Ucamco 提供了一个 [免费在线查看器](https://gerber-viewer.ucamco.com/) 来打开和查看 GBR 文件格式。

## GBR 文件格式

GBR 是一种 UTF-8 人类可读格式，仅包含 27 个命令。由于这个简短的命令列表及其紧凑性，GBR 很容易调试。 Gerber 的核心是 2D 二值图像的开放矢量格式。元信息通过属性与图像一起传输。单个 GRB 文件指定单个图像，并且不需要解释任何随附文件或外部参数。一张图片只需要一个文件。它对规范中定义的可打印的所有命令和名称使用 7 位 ASCII 字符。这完全涵盖了完整的图像生成。

### 示例 GBR 文件

以下是一个示例 Gerber 文件，它创建一个以原点为中心的直径为 1.5 毫米的圆。每行有一个命令。

```
%FSLAX26Y26*%
%MOMM*%
%ADD   100C,1.5*%
D100* X0Y0D03*
M02*
```

## 参考

* [格柏格式](https://www.ucamco.com/en/gerber)


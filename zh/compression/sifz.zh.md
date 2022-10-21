{
  "date" : "2021-04-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SIFZ 文件格式 - Synfig Studio 压缩项目文件",
  "description":"了解 SIFZ 文件格式和可以创建和打开 SIFZ 文件的 API。",
  "linktitle" : "SIFZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-30"
}

## 什么是一 .sifz 文件？

SIFZ 文件是由开源 2d 动画创建应用程序 **Synfig Studio** 创建的 gzip 压缩 SIF 文件。它包含构成动画的多个图形元素。整体动画内容是使用填充了形状、画笔或铅笔笔触和文本的画布组合而成的。所有这些都排列在它们自己的位置、半径、切线、角度、顶点和宽度手柄上。 SIFZ 文件可以用 [Synfig Studio](https://www.synfig.org/) 打开。

## SIFZ 文件格式

SIFZ 文件是使用 gzip 压缩方法打包的压缩 [ZIP](/zh/compression/zip/) 文件。 Synfig 用于使用矢量和位图艺术品创建电影质量的动画。与旧的逐帧动画创建方法不同，它可以让您以更少的资源制作更高质量的 2D 动画。

被压缩的 SIFZ 文件比未压缩的 SIF 文件小。这也使得通过低带宽互联网连接传输变得容易。

## 参考

* [Synfig 开源-Github](https://github.com/synfig/synfig/)
* [Synfig 文档](https://synfig.readthedocs.io/en/latest/index.html)


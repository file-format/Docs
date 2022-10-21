{
  "date" : "2022-07-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDR 文件格式 - 什么是 HDR 图像文件？",
  "description":"了解 HDR 文件格式和可以创建和打开 HDR 文件的 API。",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-07-21"
}

## 什么是 HDR 文件？

HDR 文件是一种高动态范围 (HDR) 光栅图像文件格式，用于存储数码相机照片。它允许照片编辑器增强动态范围有限的数字图像的颜色和亮度。这种修改可以提高角落周围的亮度，从而产生接近自然的图像。 HDR 文件通常保存为 32 位光栅图像。 Adobe Photoshop 可以创建和打开 HDR 文件。

HDR 文件也称为 HDRI。

## HDR 文件格式 - 更多信息

HDR 文件格式基于原始的 Radiance 图片 (.pic) 文件格式。 HDR 文件的像素数据通常以未压缩的形式存储，但在某些情况下，它使用简单的运行长度编码系统进行压缩。

### HDR 文件结构

一个 HDR 图像文件由以下三个部分组成：

* **标题：** HDR 文件由图像文件中的第一个字节标识，即“#?RADIANCE"。
* **Resolution String：** Header 后跟一个由 4 个值组成的分辨率行；一个 X 和 Y 标签，每个标签后跟一个数字整数值。 X 和 Y 的顺序表示旋转。 X 和 Y 与正值和负值的组合涵盖了所有可能的图像方向和旋转。
* **像素数据：** HDR 文件的像素数据未压缩或使用标准运行长度编码压缩。

## 开源 HDR/HDRI API

* **[imageinfo](https://github.com/xiaozhuai/imageinfo)** - 跨平台超快速单头 [C++](/zh/programming/cpp/) 库，无需加载/解码即可获取图像大小和格式。
* **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** - 无需加载/解码即可获取图像大小和格式的 Rust 库。支持 [.avif](/zh/image/avif/)、[.bmp](/zh/image/bmp)、[.cur](/zh/image/cur/)、[.dds](/zh/image/dds/)、[. gif](/zh/image/gif/), hdr (pic), [heic (heif)](/zh/image/heic/), [.icns](/zh/image/icns/), [.ico](/zh/image/ico /), [.jp2](/zh/image/jp2/), [jpeg (jpg)](/zh/image/jpeg/), [jpx](/zh/image/jpx/), ktx, [png](/zh/image/png /)、[psd](/zh/image/psd/)、qoi、tga、tiff (tif) 和 webp。
* **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** - HdrHistogram 的 Java 实现。

## 参考

* [光辉 HDR](http://paulbourke.net/dataformats/pic/)
* [图片信息](https://github.com/xiaozhuai/imageinfo )


{
  "date" : "2022-04-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DDS 文件格式 - DirectDraw 表面图像文件",
  "description":"了解 DDS 文件格式和可以创建和打开 DDS 文件的 API。",
  "linktitle" : "DDS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-04-02"
}

## 什么是一 .dds 文件？

DDS 文件是利用 DirectDraw Surface (DDS) 容器格式的光栅图像文件。它存储未压缩和压缩 (DXTn) 纹理，并实现不同类型来存储不同类型的数据。它还支持几种不同类型的数据，例如单层纹理、带有 mipmap 的纹理、立方体贴图、体积贴图和纹理阵列。这使得 DDS 文件除了存储数码照片和 Windows 桌面背景之外，还可以存储视频游戏纹理单元模型。 DDS 文件格式由 Microsoft 开发，用于 DirectX SDK。

## DDS 文件格式

DDS 文件保存为二进制文件，可与 DirectX SDK 一起使用。它利用 DirectX 的强大功能开发实时渲染应用程序，例如 3D 游戏。

### DDS 文件布局

[DDS 文件布局](https://docs.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) 已被 Microsoft 详细记录。二进制 DDS 文件包含以下信息。

* 包含四个字符代码值“DDS"（0x20534444）的 DWORD（幻数）。
* 文件中数据的描述。

DDS_HEADER 描述数据，DDS_PIXELFORMAT 描述像素格式。这些都替换了已弃用的 DDSURFACEDESC2、DDSCAPS2 和 DDPIXELFORMAT DirectDraw 7 结构。

```
DWORD               dwMagic;
DDS_HEADER          header;
```

[DDS文件格式的编程指南](https://docs.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide)进一步阐述了这种文件格式的技术细节。

## 参考

* [DDS - 维基百科](https://en.wikipedia.org/wiki/DirectDraw_Surface)
* [ZSoft PCX 文件格式技术参考手册](http://qzx.com/pc-gpe/pcx.txt)


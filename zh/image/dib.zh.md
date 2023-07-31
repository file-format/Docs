{
  "date" : "2020-01-10",
  "keywords" :["dib 文件","dib 文件格式","什么是 dib 文件","文件","dib 示例","dib 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DIB",
  "description":"了解 DIB 文件格式和可以创建和打开 DIB 文件的 API。",
  "linktitle" : "DIB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## 什么是一 .dib 文件？

与设备无关的位图 (DIB) 是一种光栅图像文件，其结构类似于标准位图文件 ([BMP]()/image/bmp/))。它包含一个颜色表，描述了 RGB 颜色到像素值的映射。这使 DIB 能够在任何设备上表示图像。几乎所有可以在 Windows 和 macOS 上打开标准 BMP 文件的应用程序都可以打开它。 DIB 是二进制文件，具有类似于 BMP 的复杂文件格式。 DIB 图像在颜色深度和每英寸像素方面独立于渲染设备的输出能力。

## DIB 文件格式规范 ##
DIB 包含以下颜色和尺寸信息：

* 创建矩形图像的设备的颜色格式。
* 创建矩形图像的设备的分辨率。
* 创建图像的设备的调色板。
* 将红色、绿色、蓝色 (RGB) 三元组映射到矩形图像中的像素的位数组。
* 一个数据压缩标识符，指示用于减小位数组大小的数据压缩方案（如果有）。

### DIB 数据块格式 ###

与存储在磁盘上的 .DIB 文件相比，DIB 出现在内存块的上下文中。内存块由符合 DIB 的 Windows API 规范的结构组成。实际的 DIB 包括：
* 一个标题
*调色板
* 像素数据

实际上，使用调色板、标题和图像数据就像它们是三个独立的内存块一样。这个公共内存块的句柄是使用 GlobalAlloc 分配的，称为 HDIB，用于提取和处理标题、颜色表和像素数据。

### 结构###
DIB 中包含的信息由不同的结构表示。这些包括：

BITMAPInfo - 定义 DIB 的尺寸和颜色信息
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
它由一个 BITMAPINFOHEADER 组成：

```
typedef struct tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} BITMAPINFOHEADER, *PBITMAPINFOHEADER;
```
后跟两个或多个 RGBQAD 结构。

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### 数据位###
|位|说明|
---|---|
|1 位格式（单色）|单色位图由两种颜色（黑色和白色）组成。由于颜色数量有限，这些位图在磁盘上占用的空间更少。 bitBitCount 返回真或假以表示两种颜色。如果 bitBitCount==1，大多数应用程序会完全跳过调色板。
|4 位格式（VGA 或 16 色）|图像数据的每个字节代表两个像素，bitBitCount==4。这些位按降序表示像素的颜色。
|8 位格式（256 色）|此 8 位格式最多可表示 256 种颜色。图像位图数据数组中的每个字节代表一个像素。该字节的值是 bmciColors 表示的 256 个条目中要使用的调色板条目的编号。
|24 位格式 (TrueColor)|这些位图最多可以有 2^24 种颜色 (biBitCount == 24)。位图数据数组中的每个三字节序列代表一个像素的三种主要色调的相对强度。色调被描述为范围从 0 到 255 的值，并以蓝色、绿色和红色的顺序存储在三个字节中。这是一个重要的区别，因为 Windows 中对颜色的大多数引用使用相反的顺序：红/绿/蓝，因此在使用 TrueColor 图像时考虑“BGR"而不是“RGB"。可以指定调色板来加速 Windows 的绘图过程，在这种情况下 biClrUsed 不会为 0。但正如您所见，它不是必需的，因为像素数据本身包含颜色信息。
|32 位格式|32 位图像最多有 2^24 种颜色 (biBitCount == 24)。

## 参考 ＃＃
* [与设备无关的位图 - Microsoft 提供](https://learn.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)


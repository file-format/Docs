{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PCX 文件格式 - 画笔位图图像文件",
  "description":"了解可创建和打开 PCX 文件的 PCX 文件格式和 API。",
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## 什么是一 .pcx 文件？

PCX 文件（图片交换文件）是一种光栅图像文件格式，用作 PC 画笔应用程序的本机文件格式。由美国 ZSoft 公司针对 DOS 和 Windows 平台开发，在 [BMP](/zh/image/bmp/)、[JPEG](/zh/image/jpeg/) 和 [ PNG](/zh/image/png/) 文件格式。 PCX 文件的大小更小，因为它们是使用 RLE 编码压缩的。它用于多页 [DCX](/zh/image/dcx/) 文件，该文件主要用于创建数字传真文件。

## PCX 文件格式

PCX 文件以二进制文件格式保存到光盘中。内部文件格式结构遵循 little endian 字节顺序，分为以下三个部分：

**`PCX 标头`** - PCX 标头的长度为 128 字节。它包含标识符、版本号、图像尺寸、16 种调色板颜色、颜色平面数和每个平面的位深度，以及压缩方法的值。

PCX Header 参考图形文件格式百科全书（第 2 版）如下所示。
```
typedef struct _PcxHeader
{
  BYTE	Identifier;        /* PCX Id Number (Always 0x0A) */
  BYTE	Version;           /* Version Number */
  BYTE	Encoding;          /* Encoding Format */
  BYTE	BitsPerPixel;      /* Bits per Pixel */
  WORD	XStart;            /* Left of image */
  WORD	YStart;            /* Top of Image */
  WORD	XEnd;              /* Right of Image
  WORD	YEnd;              /* Bottom of image */
  WORD	HorzRes;           /* Horizontal Resolution */
  WORD	VertRes;           /* Vertical Resolution */
  BYTE	Palette[48];       /* 16-Color EGA Palette */
  BYTE	Reserved1;         /* Reserved (Always 0) */
  BYTE	NumBitPlanes;      /* Number of Bit Planes */
  WORD	BytesPerLine;      /* Bytes per Scan-line */
  WORD	PaletteType;       /* Palette Type */
  WORD	HorzScreenSize;    /* Horizontal Screen Size */
  WORD	VertScreenSize;    /* Vertical Screen Size */
  BYTE	Reserved2[54];     /* Reserved (Always 0) */
} PCXHEAD;
```

**`图像数据`** - PCX 图像数据紧跟在标题之后。根据标题中的字段设置，可以压缩图像数据。 PCX 文件中数据的存储取决于指定颜色平面的数量。图像数据按行组织。在多个平面的情况下，这些平面按红色、绿色和蓝色数据的顺序排列在行内存储。对平面中的每条线重复此模式。

## 参考

* [PCX - 维基百科](https://en.wikipedia.org/wiki/PCX)


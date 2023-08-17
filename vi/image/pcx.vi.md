{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp PCX - Tệp hình ảnh bitmap cọ vẽ",
  "description":"Tìm hiểu về định dạng tệp PCX và API có thể tạo và mở tệp PCX.",
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## Tệp PCX là gì?

Tệp PCX, tệp Picture Exchange, là định dạng tệp hình ảnh raster được sử dụng làm định dạng tệp gốc cho ứng dụng PC Paintbrush. Nó được phát triển bởi ZSoft Corporation, Hoa Kỳ cho các nền tảng DOS và Windows và được sử dụng làm định dạng tệp hình ảnh chính trước khi [BMP](/vi/image/bmp/), [JPEG](/vi/image/jpeg/), và [ Định dạng tệp PNG](/vi/image/png/). Các tệp PCX có kích thước nhỏ hơn vì chúng được nén bằng mã hóa RLE. Nó được sử dụng trong tệp [DCX](/vi/image/dcx/) nhiều trang, tệp này chủ yếu được sử dụng để tạo tệp fax kỹ thuật số.

## Định dạng tệp PCX

Các tệp PCX được lưu vào đĩa ở định dạng tệp nhị phân. Cấu trúc định dạng tệp bên trong tuân theo thứ tự byte cuối nhỏ và có ba phần sau:

**`Tiêu đề PCX`** - Tiêu đề PCX dài 128 byte. Nó chứa mã định danh, số phiên bản, kích thước hình ảnh, 16 bảng màu, số mặt phẳng màu và độ sâu bit của mỗi mặt phẳng và giá trị cho phương pháp nén.

PCX Header được hiển thị bên dưới với tham chiếu từ Bách khoa toàn thư về các định dạng tệp đồ họa (tái bản lần 2).
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

**`Dữ liệu hình ảnh`** - Dữ liệu hình ảnh PCX ngay sau tiêu đề. Dữ liệu hình ảnh có thể được nén tùy thuộc vào cài đặt trường trong tiêu đề. Việc lưu trữ dữ liệu trong tệp PCX phụ thuộc vào số lượng mặt phẳng màu được chỉ định. Dữ liệu hình ảnh được sắp xếp theo hàng. Trong trường hợp có nhiều mặt phẳng, chúng được lưu trữ theo mặt phẳng trong hàng theo thứ tự sắp xếp dữ liệu màu đỏ, xanh lá cây và xanh dương. Mô hình này được lặp lại cho mỗi dòng trong mặt phẳng.

## Người giới thiệu

* [PCX - Theo Wikipedia](https://en.wikipedia.org/wiki/PCX)


{
  "date" : "2020-08-20",
  "keywords" :["fnt 文件","fnt 文件格式","什么是 fnt 文件","文件","fnt 示例","fnt 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FNT - Windows 字体文件",
  "description":"了解 FNT 文件格式和可以创建和打开 FNT 文件的 API。",
  "linktitle" : "FNT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## 什么是一 .fnt 文件？

具有 .fnt 扩展名的文件是一种字体文件，用于存储 Windows 操作系统上的通用字体信息。 FNT 文件大部分已被 TrueType (.TTF) 和 OpenType (.OTF) 文件格式取代，并且是目前已过时的字体文件格式。这些文件可以存储单个评估者或矢量字体。所有设备驱动程序都支持 Windows 2.x 字体。但是，并非所有设备驱动程序
支持Windows 3.0版本。

## FNT 文件格式

FNT 文件能够存储单个光栅或矢量字体。与使用小位图定义每个章程的字形的栅格相比，GDI 更频繁地使用矢量格式。将 .fnt 替换为 .ttf 和 .otf 的明显原因是其光栅格式。

### 字体文件头
光栅和矢量字体文件的开头很常见，然后是每种文件类型的不同信息。 Windows 3.0 的字体文件头包括以下六个新字段，这些字段设置为零以确保与未来版本的 windows 兼容。

* dFlags
* df空间
* dfB空间
* dfC空间
* dfColorPointer
* dfReserved1

有关 Windows 3.0 和 2.0 标头的详细信息，请访问 [Microsoft 知识库存档](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)。

## 参考
* [字体文件格式](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
* [如何在 Windows 中安装或删除字体](https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8-7613-c76f-88d043b334b8)


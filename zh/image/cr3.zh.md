{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CR3 文件格式 - Canon Raw 3 图像文件",
  "description":"了解 CR3 文件格式和可以创建和打开 CR3 文件的 API。",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## 什么是一 .cr3 文件？

CR3 文件是由选定的佳能数码相机创建的佳能 RAW 图像文件格式。它由佳能引入以取代 CR2 文件格式，并被一些佳能数码设备使用。 CR3 文件存储相机拍摄的原始未处理的无损图像数据。这些原始图像的使用提供了高质量的图像，并为摄影师提供了足够的编辑空间。除了主图像数据，CR3 文件还存储有关图像的元数据信息。

## CR3 文件格式

CR3 文件以 ISO 基本媒体文件格式 (ISO/IEC 14496-12) 的二进制文件形式存储到光盘中，还包括自定义 [佳能标签](https://exiftool.org/TagNames/Canon.html#uuid)。它还包括混合了 JPEG-LS（Rice-Golomb + RLE编码）和 JPEG-2000（LeGall 5/3 DWT + 量化）。

## CR3 自定义标签

CR3 文件包含用于不同目的的自定义标签。其中一些标签如下。

|标签ID|标签名称|可写|值/注释|
---|---|---|---|
|'CCTP' |佳能CCTP| - |--> 佳能 CCTP 标签|
|'CMT1' |IFD0| - |--> EXIF 标签|
|'CMT2' |ExifIFD| - |--> EXIF 标签|
|'CMT3' |MakerNoteCanon| - |--> 佳能标签|
|'CMT4' |GPS信息| - |--> GPS 标签|
|'CNCV' |压缩机版本|没有| |
|'CNOP' |佳能CNOP| - |--> 佳能 CNOP 标签|
|'CNTH' |佳能CNTH| - |--> 佳能 CNTH 标签|
|'THMB' |缩略图图片|没有| |

## 参考

* [CR2 文件格式](http://lclevy.free.fr/cr2/)
* [佳能标签](https://exiftool.org/TagNames/Canon.html#uuid)


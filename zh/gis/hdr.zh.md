{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDR 文件 - ESRI BIL 头文件格式",
  "description":"什么是 HDR 文件？",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## 什么是 HDR 文件？

HDR 文件是一个 GIS 头文件，其中包含按行交错的 Band (.BIL) 文件的头信息。它描述图像数据并与图像文件同名。 HDR 文件由一组条目组成，每个条目描述图像的特定属性。 HDR 文件描述了 BIL 文件的布局和格式，以便与单独的地理配准文件结合转换为现实世界坐标。

## HDR 文件格式

HDR 文件以 ASCII 文本文件格式保存。它包含一组条目，其中每个条目描述图像的特定属性。每个 HDR 文件都具有以下格式：

```
<keyword> <value>
```

`<keyword> ` - 表示正在设置的特定属性
`<value> ` - 这是属性被设置的值

标头中条目的顺序没有限制。但是，每个条目必须位于单独的行上，以符合 HDR 阅读器使用的解析方法。

## HDR 文件中使用的关键字总结

|关键字|可接受值|默认|
---|---|---|
|nrows |任何大于 0 的整数|没有任何
|ncols |任何大于 0 的整数|没有任何
|nbands |任何大于 0 的整数| 1
|n 位 |1、4、8、16、32| 8
|字节顺序| I = Intel;M = Motorola |与主机相同|
|布局| bil、bip、bsq|比尔|
|跳过字节|任意整数 ≥ 0| 0
|ulxmap |任何实数| 0|
|ulymap |任意实数 |nrows - 1|
|xdim |任意实数| 1
|ydim |任意实数| 1
|bandrowbytes |任何大于 0 的整数|最小整数 ≥ (ncols x nbits) / 8|
|totalrowbytes |任意整数 > 0|对于 bil：nbands x bandrowbytes；对于 bip：最小整数 ≥ (ncols x nbands x nbits) / 8|
|bandgapbytes |任意整数 ≥ 0| 0|

## 参考

* [HRD 文件格式 - ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)


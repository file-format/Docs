{
  "date" : "2021-07-28",
  "keywords" :["ntf 文件","ntf 文件格式","什么是 ntf 文件","文件","ntf 示例","ntf 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NTF - 国家传输格式文件",
  "description":"了解 NTF 文件格式和可以创建和打开 NTF 文件的 API。",
  "linktitle" : "NTF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-28"
}

## 什么是一 .ntf 文件？
扩展名为 .ntf 的文件称为 **National Transfer Format (NTF)** 文件；主要由英国军械调查局 (OS) 使用；专门用于地理空间数据的传输。它由英国标准协会管理。它已成为军械测量数字数据的标准传输格式。英国的国家网格投影是一种横向墨卡托投影，包含 NTF 文件的所有地理参考信息。

## NTF 文件格式
NTF 文件格式归英国军械测量局所有； GDB 库支持导入。 NTF 文件格式的当前版本是 2.0。引入此文件格式是为了解决 **PCIDSK** 矢量段的限制，每个结构只有一个属性字段，但是可以使用矢量数据提取多种属性。为了绕过 NTF 文件格式，它具有两个段。每个段由相同的向量组成，但具有不同的属性。 NTF 矢量文件的第一段包含以特征代码编号为属性的矢量。第二段包含以值作为属性的向量。

###坐标参考系
GDB 库表示具有适当 TM 投影特征的栅格和矢量数据：

- 参考经度：49.0
- 参考纬度：2.0
- 假东：400000
- 伪北：-100000
- 规模：0.9996012717
- 椭球体：艾里 1830 (E009)
不支持更新或写入 NTF 文件，也不能链接到 DTM 文件。

### Ogrinfo 示例
以下示例在 NTF 文件上使用 **ogrinfo** 来检索层号：
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## 参考

* [英国国家传输格式 (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)
* [Web 制图 - Tyler Mitchell 插图](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)


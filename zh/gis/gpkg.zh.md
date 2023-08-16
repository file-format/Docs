{
  "date" : "2021-07-29",
  "keywords" :["gpkg 文件","gpkg 文件格式","什么是 gpkg 文件","文件","gpkg 示例","gpkg 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPKG - GeoPackage 格式文件",
  "description":"了解 GPKG 文件格式和可以创建和打开 GPKG 文件的 API。",
  "linktitle" : "GPKG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## 什么是一 .gpkg 文件？
具有 .gpkg 扩展名的文件由一个地理信息系统组成，该系统实现为 SQLite 数据库容器，其中包含具有典型定义、格式限制、完整性断言和内容约束的数据和元数据表。它于2014年出版；由 OGC（开放地理空间联盟）代表美国军方定义。各种政府、商业和开源组织广泛支持 GeoPackage。

## GPKG 文件格式
GeoPackage 由扩展的 SQLite 3 数据库文件组成；标准定义了一组规则（必需的约定），用于：
- 存储图像的平铺矩阵集
- 矢量特征
- 各种比例的栅格地图
- 元数据和架构

您可以使用标准第 2.3 条中定义的扩展规则来扩展 GeoPackage。设计 GeoPackage 的目的是尽可能地制作轻量级数据库并将其包含在一个随时可用的单个文件中。这使得它非常适合离线模式下的移动应用程序以及在云存储或 USB 存储设备上的快速共享等。

### GPKG 内容
GeoPackages 包含许多表，就像其他关系数据库一样。这些表可以是用户定义的表或元数据表。 GeoPackages 包含两个必需的元数据表：

#### gpkg_contents
GeoPackage 的目录。此表中的必填列是：

- **table_name**：用户自定义数据表的实际名称；
- **data_type**：数据类型，例如标题、特征和属性；
- **标识符和描述**：人类可读的文本；
- **last_change**：上次更改的信息日期，采用 ISO 8601 格式；
- **min_x、min_y、max_x 和 max_y**：内容的空间范围。 ;
- **srs_id**：空间参考系统。

#### gpkg_spatial_ref_sys
对于空间参考内容；包括但不限于图块和特征，内容中的每一行都必须引用一个坐标参考系；存储在 **gpkg_spatial_ref_sys** 表中。此表中的必填列是：

- **srs_name, description**：SRS 的人类可读名称和描述；
- **srs_id**：SRS 的唯一标识符；也是表的主键；
- **组织**：定义组织的不区分大小写的名称。
- **organization_coordsys_id**：组织分配的SRS的数字ID；
- **定义**：SRS 的众所周知的文本定义。


## 参考

* [GeoPackage - 由维基百科提供）](https://en.wikipedia.org/wiki/GeoPackage)
* [GeoPackage 入门](http://www.geopackage.org/guidance/getting-started.html)


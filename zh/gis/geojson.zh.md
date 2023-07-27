{
  "date" : "2019-10-11",
  "keywords" :  ["geojson 文件","什么是 geojson 文件","文件","geojson 示例","geojson 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GeoJSON - 基于 JSON 的地理文件格式",
  "description":"了解 GeoJSON 文件格式和可以创建和打开 GeoJSON 文件的 API。",
  "linktitle" : "GEOJSON",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是 GeoJSON 文件？

GeoJSON 是一种基于 JSON 的格式，旨在表示具有非空间属性的地理特征。这种格式定义了不同的 JSON（JavaScript Object Notation）对象及其连接方式。 JSON 格式表示有关地理特征、它们的空间范围和属性的集体信息。该文件的一个对象可以表示一个几何体（点、线串、多边形）、一个特征或特征集合。这些要素将地址和地点反映为点的街道，将主要道路和边界反映为线串，将国家、省和土地区域反映为多边形。使用 GeoJSON，不同的移动路由和导航应用程序可以指示其服务的覆盖范围。 GeoJSON 的一个扩展是 TopoJSON，它的尺寸更小，可以对地理空间拓扑进行编码。

## 历史简介 ＃＃

互联网工程任务组 (IETF) 与格式作者合作，形成了一个 [GeoJSON WG](https://datatracker.ietf.org/wg/geojson/charter/) 以在 2015 年 4 月发布 GeoJSON。取代 2008 GeoJSON 规范，[RFC 7946](https://tools.ietf.org/html/rfc7946)，2016 年 8 月发布的 GeoJSON 格式的新标准规范。

## GeoJSON 文件格式 ##

＃＃＃ 协调 ＃＃＃

坐标是任何地理数据的基本元素。这是表示单个数字（十进制格式）的单个维度（经度、纬度），有时也记录高程坐标。时间也是一个维度，但它的复杂性使得很难将其记录为坐标。两种 JSON GeoJSON 中的坐标都采用数字格式。

＃＃＃ 位置 ＃＃＃

有序的坐标数组表示 [位置](https://geojson.org/geojson-spec.html#positions)。这是可以指示地球上一个点的最小单位。

`[经度、纬度、海拔]`

在当前规范发布之前，GeoJSON 允许每个位置记录三个坐标，但新规范不允许。

＃＃＃ 几何学 ＃＃＃

几何是 GeoJSON 中的简单形状（点、曲线和曲面），由类型和坐标集合组成。点是表示单个位置的最简单几何图形

`{“类型"：“点"，“坐标"：[0, 0] }`

### 线串###

至少使用两个相连的地方来表示一条线。

`{ "type": "LineString", "coordinates": [[10, 30], [10, 10]] }`

点串和线串是几何的两个最简单的类别。两种类型的几何都不会打扰许多几何规则。一个点可以在任何地方表示，一条线可以有多个点，即使这些点是自交叉的。

### 多边形###

GeoJSON 几何图形在 Polygons 中似乎要复杂得多。多边形具有内部和外部区域，并且可以在内部具有孔。

```
{
  "type": "Polygon",
  "Coordinates": [
    [
      [30, 10], [10, 10], [10, 0], [20, 40]
    ]
  ]
}
```

与 LineStrings 相比，在多边形中，坐标列表是嵌套的一层，并且可以像甜甜圈一样有切口。

### 坐标级别###

在 GeoJSON 格式中，对于坐标属性，有四个级别的深度。

＃＃＃ 特征 ＃＃＃

几何图形是 GeoJSON 的核心部分，因此，真实世界的数据不仅仅是这些具有身份和属性的简单形状。特征记录几何及其属性。

```
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [20, 10]
},
  "properties": {
    "name": "fortune island"
  }
}

```

特性属性可以是一种包含单深度键值映射的 [JSON](http://json.org/) 对象。

### 功能集合###

在 GeoJSON 文件的顶层，FeatureCollection 是最常见的东西，看起来像：

```
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [20, 10]
    },
      "properties": {
        "name": "null island"
  }
}
  ]
}
```

很多地图和 GIS 软件包都支持 GeoJSON，包括 GeoDjango、OpenLayers 和 Geoforge 软件。它还与 PostGIS 和 Mapnik 兼容。 Google、yahoo 和 Bing 地图的 API 服务也支持 GeoJSON。

## 参考 ＃＃

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)
* [GeoJSON - 来自维基百科](https://en.wikipedia.org/wiki/GeoJSON)


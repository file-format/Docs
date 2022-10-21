{
  "date" : "2019-10-11",
  "keywords" :["gml 文件","什么是 gml 文件","文件","gml 示例","gml 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GML - 地理标记语言文件格式",
  "description":"了解 GML 文件格式和可以创建和打开 GML 文件的 API。",
  "linktitle" : "GML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .gml 文件？

GML 代表地理标记语言，它基于开放地理空间联盟 (OGC) 开发的 XML 规范。该格式用于存储地理数据特征，以便在不同文件格式之间进行交换。它用作地理系统的建模语言以及互联网上地理交易的开放交换格式。

## GML 文件格式##

与大多数基于 XML 的语法一样，语法有两个部分——描述文档的模式和包含实际数据的实例文档。使用 GML Schema 描述 GML 文档。这允许用户和开发人员描述包含点、线和多边形的通用地理数据集。使用应用程序模式，用户可以参考道路、高速公路和桥梁，而不是点、线和多边形。

值得注意的是，不应将 GML 解释为地图上空间数据的表示。 GML 内容的表示不同于创建 GML 的目的。简而言之，GML 与 XML 的相似之处在于它仅用于保存可供地图应用程序用于显示目的的空间内容。

### GML 中的内容形成###

GML 使用特征表示空间数据，特征是属性和几何的列表。属性具有名称、类型和值描述。几何由基本几何构建块组成，例如：

* 点
* 行
* 曲线
* 表面和
* 多边形

GML 的未来版本计划支持 3D 几何以及特征之间的拓扑关系。

GML 编码已经允许相当复杂的特性。例如，一个特征可以由其他特征组成。因此，像机场这样的单一要素可能由其他要素组成，例如滑行道、跑道、衣架和航站楼。地理特征的几何也可以由许多几何元素组成。因此，一个几何复杂的特征可以由多种几何类型组成，包括点、线串和多边形。

＃＃＃ 例子 ＃＃＃

GML 1.0 和 2.0 对 Polygons、Points 和 LineString 对象进行如下编码：

```
<gml:Polygon>
         <gml:outerBoundaryIs>
                 <gml:LinearRing>
                         <gml:coordinates>0,0 100,0 100,100 0,100 0,0</gml:coordinates>
                 </gml:LinearRing>
        </gml:outerBoundaryIs>
     </gml:Polygon>
     <gml:Point>
        <gml:coordinates>100,200</gml:coordinates>
     </gml:Point>
     <gml:LineString>
        <gml:coordinates>100,200 150,300</gml:coordinates>
     </gml:LineString>
```

## 参考 ＃＃

* [GML 规范](http://www.opengeospatial.org/standards/gml)
* [GML - 维基百科](https://en.wikipedia.org/wiki/Geography_Markup_Language)


{
  "date" : "2021-07-18",
  "keywords" :["LOC","文件","扩展名","文件格式","GPS 位置","航点"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOC - GPS 位置文件格式",
  "description":"了解 LOC 文件格式和可以创建和打开 LOC 文件的 API。",
  "linktitle" : "LOC",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-18"
}

## 什么是一 .loc 文件？

带有 .loc 扩展名的文件是一个 GPS 位置文件，其中包含作为航点的地理空间位置。航路点是一对经纬度值，指的是地理信息系统 (GIS) 应用程序使用的位置。 GPS 测绘程序，如 DeLorme Topo，使用 LOC 文件来读取和显示这些 LOC 文件中包含的信息，作为最终用户的可选层。此外，这些用于在应用程序之间交换 GPS 数据。 LOC 文件可以使用诸如 [TopoGrafix EasyGPS](https://www.easygps.com/) 之类的应用程序打开，该应用程序将此类文件的内容显示为在相应地理位置的地图上绘制的图层和数据。

## LOC 文件格式 - 更多信息

LOC 文件与 [GPX](/zh/gis/gpx/) 文件有相似之处，但以不同的格式保存。这些保存为 [XML](/zh/web/xml/) 文件，其中航点的内容和相关信息包含在结构化标签中。由于 XML 是用于在不同应用程序之间交换数据的通用语言，因此这有助于与其他应用程序交换 LOC 数据。

## LOC 文件格式 - 示例

以下是 LOC 文件中一个航路点的标题和文本。可以看出，标头信息包含数据的位置来源。航路点包含诸如“ID"之类的信息以及与该航路点相关联的相关内容数据。最后，航点是纬度和经度值的集合，以及与该特定航点关联的文本。

```
<?xml version="1.0" encoding="UTF-8"?>

<loc version="1.0" src="Groundspeak">

<waypoint>

<name id="GCGFTA"><![CDATA[The Volunteer Cache or Find The Bridge by Eagle Son]]></name>

<coord lat="41.6965166666667" lon="-88.1080166666667"/>

<type>Geocache</type>
<link text="Cache Details">http://www.geocaching.com/seek/cache_details.aspx?wp=GCGFTA</link>

</waypoint>
```

## 参考

* [TopGraphic EasyGPS](https://www.easygps.com/)


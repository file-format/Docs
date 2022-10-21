{
  "date" : "2019-10-11",
  "keywords" :["kml 文件","什么是 kml 文件","文件","kml 示例","kml 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KML - 钥匙孔标记语言",
  "description":"了解 KML 文件格式和可以创建和打开 KML 文件的 API。",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .kml 文件？

KML，Keyhole 标记语言）包含 XML 表示法的地理空间信息。保存为 KML 的文件可以在地理信息系统 (GIS) 应用程序中打开，前提是它们支持它。许多应用程序在 KML 文件格式被采纳为国际标准后开始提供对它的支持。 KML 使用带有嵌套元素和属性的基于标签的结构。所有标签都区分大小写，并且按照 [KML](https://developers.google.com/kml/documentation/kmlreference) 参考，这些标签的顺序非常重要。

## 历史简介 ＃＃

KML 最初是为与最初称为 Keyhole Earth Viewer 的 Google 地球一起使用而开发的。 KLM 于 2008 年被 Open Geospatial Consortium 于 2008 年采用为国际标准。由于该格式是为与 Google 地球一起使用而开发的，因此它具有成为第一个查看和编辑 KML 文件的区别。随着时间的推移，现在有越来越多的项目支持 KML 文件格式，包括多种不同语言的 API。

## KML 文件格式规范 ##

KML 参考是一个完整的参考指南，以便获得完整的文件格式规范。标准 KML 文件包括：

* 地标
* 地标中的描述性 HTML
*地面覆盖
* 路径
*多边形

除此之外，KML 文件的高级版本还可以具有：

* 几何样式
* 突出显示图标的样式
*屏幕覆盖
* 网络链接

每个 KML 元素都有经纬度信息，用于对文件中存在的信息进行地理定位。但是，可能还有其他参数，例如航向、高度和倾斜度。

### 地标###

它用于表示地球表面上的一个位置，并由<Point>元素。以下是如何在 KML 文件中表示地标的示例。

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Placemark>
    <name>Simple placemark</name>
    <description>Attached to the ground. Intelligently places itself
       at the height of the underlying terrain.</description>
    <Point>
      <coordinates>-122.0822035425683,37.42228990140251,0</coordinates>
    </Point>
  </Placemark>
</kml>
```

### 地标中的描述性 HTML ###

附加信息可以与进一步增强地标表示的地标相关联。此类信息包括链接、字体大小、样式和颜色。此外，它还包括作为地标一部分的文本对齐和表格。

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <Placemark>
      <name>CDATA example</name>
      <description>
        <![CDATA[
          <h1>CDATA Tags are useful!</h1>
          <p><font color#"red">Text is <i>more readable</i> and
          <b>easier to write</b> when you can avoid using entity
          references.</font></p>
        ]]>
      </description>
      <Point>
        <coordinates>102.595626,14.996729</coordinates>
      </Point>
    </Placemark>
  </Document>
</kml>
```

###地面覆盖层###

这些代表图像在地球表面的分层。这<icon>elment 包含到覆盖图像文件的链接。

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Folder>
    <name>Ground Overlays</name>
    <description>Examples of ground overlays</description>
    <GroundOverlay>
      <name>Large-scale overlay on terrain</name>
      <description>Overlay shows Mount Etna erupting
          on July 13th, 2001.</description>
      <Icon>
        <href>https://developers.google.com/kml/documentation/images/etna.jpg</href>
      </Icon>
      <LatLonBox>
        <north>37.91904192681665</north>
        <south>37.46543388598137</south>
        <east>15.35832653742206</east>
        <west>14.60128369746704</west>
        <rotation>-0.1556640799496235</rotation>
      </LatLonBox>
    </GroundOverlay>
  </Folder>
</kml>
```

### 路径###

路径由<LineString>元素是 lat-long 对的集合。使用这些，可以在 Google 地球中创建许多不同类型的路径。

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <name>Paths</name>
    <description>Examples of paths. Note that the tessellate tag is by default
      set to 0. If you want to create tessellated lines, they must be authored
      (or edited) directly in KML.</description>
    <Style id#"yellowLineGreenPoly">
      <LineStyle>
        <color>7f00ffff</color>
        <width>4</width>
      </LineStyle>
      <PolyStyle>
        <color>7f00ff00</color>
      </PolyStyle>
    </Style>
    <Placemark>
      <name>Absolute Extruded</name>
      <description>Transparent green wall with yellow outlines</description>
      <styleUrl>#yellowLineGreenPoly</styleUrl>
      <LineString>
        <extrude>1</extrude>
        <tessellate>1</tessellate>
        <altitudeMode>absolute</altitudeMode>
        <coordinates> -112.2550785337791,36.07954952145647,2357
          -112.2549277039738,36.08117083492122,2357
          -112.2552505069063,36.08260761307279,2357
          -112.2564540158376,36.08395660588506,2357
          -112.2580238976449,36.08511401044813,2357
          -112.2595218489022,36.08584355239394,2357
          -112.2608216347552,36.08612634548589,2357
          -112.262073428656,36.08626019085147,2357
          -112.2633204928495,36.08621519860091,2357
          -112.2644963846444,36.08627897945274,2357
          -112.2656969554589,36.08649599090644,2357
        </coordinates>
      </LineString>
    </Placemark>
  </Document>
</kml>
```

## KML 文件中的空间参考 ##

任何地理空间文件中包含的有关地理位置的信息在没有空间参考信息的情况下可能具有不同的含义。默认情况下，KML 文件的空间参考由 1984 年世界大地测量系统 WGS84 定义。

## 参考 ＃＃

* [KML 参考](https://developers.google.com/kml/documentation/kmlreference)
* [KML 谷歌开发者教程](https://developers.google.com/kml/documentation/kml_tut)
* [KML 文件格式](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)


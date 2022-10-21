{
  "date" : "2019-10-11",
  "keywords" :["gpx 文件","什么是 gpx 文件","文件","gpx 示例","gpx 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPX - GPX 交换文件格式",
  "description":"了解 GPX 文件格式和可以创建和打开 GPX 文件的 API。",
  "linktitle" : "GPX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .gpx 文件？

带有 GPX 扩展名的文件代表 GPS 交换格式，用于在 Internet 上的应用程序和 Web 服务之间交换 GPS 数据。它是一种轻量级的 XML 文件格式，包含 GPS 数据，即要由多个程序导入和红色的航路点、路线和轨迹。 GPX 文件格式是开放的，并受到各种应用程序和 GPS 设备的支持。可以加载来自此类文件的 GPS 数据，以在地图应用程序上显示以用于地理空间目的。

## GPX 文件格式 ##

GPX 文件由纬度和经度位置数据、海拔值和其他可能的其他描述性信息组成。位置数据以十进制度表示，海拔以米表示。 GPX 文件中的时间采用 ISO 8601 格式的协调世界时 (UTC)。使用 GPX 文件的好处如下：

* GPX 允许您与越来越多的 Windows、MacOS、Linux、Palm 和 PocketPC 程序列表交换数据。
* GPX 可以使用简单的网页或转换器程序转换为其他文件格式。
* GPX 基于 XML 标准，因此您使用的许多新程序（例如 Microsoft Excel）都可以读取 GPX 文件。
* GPX 使网络上的任何人都可以轻松开发新功能，这些新功能将立即与您喜爱的程序一起使用。

[GPX Schema](https://www.topografix.com/GPX/1/1/gpx.xsd) 显示了 GPX 文件格式的表示形式以供参考。

### 基本数据###

以下是作为 GPS 数据表示的 GPX 文件的一部分的基本数据。

* **航点**：航点是一个点的 WGS84 (GPS) 坐标，表示 OGR 类型 wkbPoint 的特征层
* **Routes**：表示OGR类型wkbLineString的一层特征。它包括一个跟踪点列表，这些点是显示通往目的地的转弯或阶段点的航点
* **Tracks**：Tracks 表示 OGR 类型 wkbMultiLineString 的特征层。它由至少一个段组成，该段包含描述路径的点的有序列表中的航路点。它由代表连续 GPS 轨迹的轨迹点列表组成。

### GPX 示例文件###

以下 GPX 文件显示了 GPX 文件中 GPS 数据的组织结构，可以很好地了解 GPX 文件的内容。

```
<gpx xmlns#"http://www.topografix.com/GPX/1/1" xmlns:gpxx#"http://www.garmin.com/xmlschemas/GpxExtensions/v3" xmlns:gpxtpx#"http://www.garmin.com/xmlschemas/TrackPointExtension/v1" creator#"Oregon 400t" version#"1.1" xmlns:xsi#"http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation#"http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd http://www.garmin.com/xmlschemas/GpxExtensions/v3 http://www.garmin.com/xmlschemas/GpxExtensionsv3.xsd http://www.garmin.com/xmlschemas/TrackPointExtension/v1 http://www.garmin.com/xmlschemas/TrackPointExtensionv1.xsd">
  <metadata>
    <link href#"http://www.garmin.com">
      <text>Garmin International</text>
    </link>
    <time>2009-10-17T22:58:43Z</time>
  </metadata>
  <trk>
    <name>Example GPX Document</name>
    <trkseg>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.46</ele>
        <time>2009-10-17T18:37:26Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.94</ele>
        <time>2009-10-17T18:37:31Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>6.87</ele>
        <time>2009-10-17T18:37:34Z</time>
      </trkpt>
    </trkseg>
  </trk>
</gpx>
```

## 参考 ＃＃

* [GPX 文件格式](http://www.topografix.com/gpx.asp)
* [GPX - 维基百科](https://en.wikipedia.org/wiki/GPS_Exchange_Format)


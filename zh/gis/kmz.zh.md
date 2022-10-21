{
  "date" : "2019-10-11",
  "keywords" :["kmz 文件","什么是 kmz 文件","文件","kmz 示例","kmz 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KMZ - KML 压缩文件格式",
  "description":"了解 KMZ 文件格式和可以创建和打开 KMZ 文件的 API。",
  "linktitle" : "KMZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .kmz 文件？

KMZ（KML 压缩）文件是压缩 [KML](/zh/gis/kml/) 文件的表示形式，其中包含可在 GIS 应用程序（如 Google 地球）中查看的地理空间信息。有关地标的信息在文件中表示为纬度和经度以及自定义名称。单个打包的 KMZ 文件可以轻松地与其他用户共享。 KMZ 文件可以包含 3D 模型数据以及模型的地理表示。通过将文件保存到在线位置，然后在 Google 地图搜索框中键入 URL，可以在 Google 地图中打开 KMZ 文件。

## 文件结构##

MKZ 文件的内容由一个主 KML 文件和零个或多个关联文件组成。可以使用 WinZIP 等标准解压缩实用程序提取它。 KMZ 文件格式也被压缩为压缩比为 10:1 的存档。您可以将数据从 Google 地球（如应用程序）直接导出为 KMZ 文件格式。主 KML 文件名为 **doc.kml**。打包 KMZ 文件时，可以向其中添加多个 KML 文件，但这没有任何好处，因为 Google 地球在打开 KMZ 文件并读取它时会搜索第一个 KML 文件。它会忽略存档中找到的任何其他 KML 文件。为了确保 Google 地球能够读取所需的 KML 文件，建议在 KMZ 文件中只放置一个 KML 文件。

doc.kml 文件中引用的图像、模型、纹理、声音文件和其他资源位于主文件夹内的另一个子文件夹中。这也可能涉及一些复杂性，具体取决于支持文件的数量。到这些组成资源的链接可以是相对引用或通过绝对引用。

### 相对引用###

当资源放在主文件夹内的子文件夹内的主 doc.kml 旁边时，相对引用可以指向这些支持文件，如下例所示（仅用于图标）。

```
<IconStyle>
  <scale>1.1</scale>
  <Icon>
    <href>files/icon_surfing.png</href>
  </Icon>
</IconStyle>
```

### 绝对引用###

资源也可以绝对引用。绝对引用包含链接文件的完整 URL。当文件发布在中央服务器上时，与相对引用相比，绝对引用确保这些文件保持明确。不建议绝对引用本地文件，因为当文件移动到新系统时，这些链接会中断。绝对引用的示例如下：

```
<Icon>
  <href>http://maps.google.com/mapfiles/kml/pushpin/ylw-pushpin.png</href>
</Icon>
```

## 也可以看看 ＃＃

* [GeoJSON](/zh/gis/geojson/)

## 参考 ＃＃

* [Google 地球和 KMZ 文件](https://developers.google.com/kml/documentation/kmzarchives#google-earth-and-kmz-archives)


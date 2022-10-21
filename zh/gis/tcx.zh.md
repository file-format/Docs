{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TCX 文件格式- 培训中心 XML 文件",
  "description":"了解 TCX 文件格式和可以创建和打开 TCX 文件的 API。",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## 什么是一 .tcx 文件？

TCX（Training Center XML）文件是一种数据交换格式，用于在健身设备之间共享数据。它于 2008 年与 Garmin 的培训中心产品一起推出。心率、跑步节奏、自行车节奏、卡路里和单圈时间等锻炼数据以 [XML](/zh/web/xml/) 格式存储在 TCX 文件中。此外，有关锻炼轨迹的摘要数据也包含在 TCX 文件中。 TCX 文件类似于使用 Garmin 运动可穿戴设备创建的 [FIT](/zh/gis/fit/) 文件。

## TCX 文件格式 - 更多信息

TCX 文件作为 XML 文件保存到磁盘，每条记录都保存为一个活动。活动包含锻炼的所有数据，例如时间、单圈时间、Id、心率、强度、节奏和跟踪信息，其中包含位置对以及类似于 [GPX] 的经纬度位置的时间戳(/zh/gis/gpx/) 文件。

### TCX 文件格式版本

这种格式有两个版本，它们都有自己的由 Garmin 托管的 XML 模式。以下是其中的几个：

* https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
* https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
* https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## TCX 数据协议

TCX XML 格式的 swift 版本在 Github 上作为 [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol) 可用。

## 参考 ＃＃

* [培训中心 XML](https://en.wikipedia.org/wiki/Training_Center_XML)
* [TCX 查看器](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)


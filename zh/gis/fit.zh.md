{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FIT 文件格式 - Garmin 活动文件",
  "description":"了解 FIT 文件格式和可以创建和打开 FIT 文件的 API。",
  "linktitle" : "FIT",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## 什么是 .fit 文件？

FIT 文件是由 Garmin 运动可穿戴设备创建的 GIS 文件。它用于记录当他/她穿着这些设备移动时的活动。活动数据包括 GPS 设备记录的位置和时间。 FIT 文件还用于使用 Web API 传输记录的活动数据。这就是 FIT 文件是与其他健身平台共享健身数据最常用的文件格式的原因。其他常见的文件格式包括 [GPX](/zh/gis/gpx/)、TCX 和 [KML](/zh/gis/kml/)。

## FIT 文件格式 - 更多信息

FIT 文件以二进制文件的形式保存到光盘，其中包含 Garmin 设备为活动记录的信息。存储在 FIT 文件中的信息包括：

* 约会时间
* 运动类型
*圈和分裂数据
* GPS轨迹
* 传感器数据
*活动会话的事件

活动数据可以实时记录在文件中，也可以在活动记录完成后导出。

### FIT 活动消息

FIT 活动文件可能包含一些必需的消息类型。以下是活动文件所需的消息。

|留言|宗旨|
---|---|
|文件编号|所有 FIT 文件类型都需要文件 ID 消息，并且应该是文件中的第一条消息。对于 Activity 文件，Type 属性应设置为 4。|
|活动| FIT 活动文件中需要单个活动消息。活动消息中包括本地时间戳和会话计数属性。本地时间戳用于确定可应用于文件中所有时间戳的时区偏移量。大多数设备实时记录 FIT 文件，并且在记录结束之前会话计数将是未知的。因此，活动消息通常是文件中的最后一条消息。|
|会话|活动文件将包含一个或多个会话消息。会话消息是摘要消息类型。 Start Time、Total Elapsed Time、Total Timer Time 和 Timestamp 是所有摘要消息的必填字段。|
|圈|圈数消息表示会话中的圈数或间隔。 Lap 消息是一种摘要消息类型。 Start Time、Total Elapsed Time、Total Timer Time 和 Timestamp 是所有摘要消息的必填字段。|
|记录|记录信息包括GPS坐标、速度、距离、心率、功率等|

## FIT 文件有用资源

* [解码 FIT 活动文件](https://developer.garmin.com/fit/cookbook/decoding-activity-files/)
* [编码 FIT 活动文件](https://developer.garmin.com/fit/cookbook/encoding-activity-files/)
 

## 参考 ＃＃

* [FIT 活动文件](https://developer.garmin.com/fit/file-types/activity/)


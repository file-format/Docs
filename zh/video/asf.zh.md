{
  "date" : "2021-02-15",
  "keywords" :["asf 文件","asf 文件格式","什么是 asf 文件","文件","asf 示例","asf 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASF - 高级系统文件格式",
  "description":"了解 ASF 文件格式和可以创建和打开 ASF 文件的 API。",
  "linktitle" : "ASF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## 什么是一 .asf 文件？

扩展名为 .asf 的文件是一种多媒体文件格式，用于通过网络存储和播放数字媒体流。它是一种容器文件格式，可以同时包含用于在线流式传输的视频和音频内容。您很少会找到 ASF 文件，更有可能会遇到都指定 ASF 文件的 Windows Media Audio ([WMA](/zh/audio/wma/)) 和 Windows Media Video ([WMV](/zh/video/wmv/)) 文件具有使用各自编解码器编码的内容。可以使用 Windows Media Format SDK 创建和读取 Windows 媒体文件。

## ASF 文件格式

一个 ASF 文件可以包含多个独立或依赖的流。这可以包括用于多声道音频的多个音频流或多个比特率视频流。多个比特率使流适合在不同带宽上传输。此外，ASF 文件中的流可以是压缩或未压缩格式。使用 Microsoft Windows Media 音频和视频 9 系列编解码器可实现最佳压缩。 [Microsoft 网站](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc) 上提供了 ASF 文件格式的完整规范。

### ASF 顶级文件结构

ASF 文件在逻辑上包含三种顶级对象：

* `Header Object` - 强制，必须放在每个 ASF 文件的开头
* `Data Object` - 强制并且必须跟在头对象之后
* `Index Object(s)` - 可选，但在提供对 ASF 文件的基于时间的随机访问时很有用

下图显示了 ASF 文件的顶级文件结构。

![ASF File Structure](../asf.png "ASF File Structure")

#### ASF 顶级标题对象

Header 对象在 ASF 文件的开头提供众所周知的字节序列，并且可以选择包含元数据，例如书目信息。它包含正确解释数据对象中的信息所需的所有信息。标头对象可能包括几个标准对象，包括但不限于：

* 文件属性对象 - 包含全局文件属性。
* 流属性对象 - 定义数字媒体流及其特征。
* 标头扩展对象 - 允许向 ASF 文件添加附加功能，同时保持向后兼容性。
* 内容描述对象 - 包含书目信息。
* 脚本命令对象 - 包含可以在播放时间线上执行的命令。
* 标记对象 - 在文件中提供命名的跳转点。

标头对象使用以下结构表示：

|字段名称 |字段类型 |大小（位）|
---|---|---|
|对象 ID|图形用户界面| 128|
|对象大小| QWORD| 64|
|标题对象的数量|双字| 32|
|保留1|字节| 8|
|保留2|字节| 8|

#### ASF 顶级数据对象

ASF 文件的所有数字媒体数据都包含在数据对象中，并以 ASF 数据包的形式存储。每个数据包具有固定长度，并包含一个或多个数字媒体流的数据。

#### ASF 顶级索引对象

ASF 顶级索引对象有以下两种类型：

* `Simple Index Object` - 包含 ASF 文件中视频数据的基于时间的索引。索引条目之间的时间间隔是恒定的，并且存储在简单索引对象中。
* `Index Object` - 指Index Object、Media Object Index Object、Timecode Index Object，格式类似。与简单索引对象一样，索引对象以固定时间间隔按时间索引，但不限于视频流。

## 参考

* [ASF 文件格式 - Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)
* [QuickTime 文件格式 - 维基百科](https://en.wikipedia.org/wiki/QuickTime_File_Format)


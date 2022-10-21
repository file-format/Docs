{
  "date" : "2022-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4S 文件 - 什么是 M4S 文件？",
  "description":"了解 M4S 文件格式和可以创建和打开 M4S 文件的 API。",
  "linktitle" : "M4S",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-18"
}

## 什么是一 .m4s 文件？

M4S 文件是使用 **MPEG-DASH** 流技术通过 Internet 流式传输的一小段视频。它包含二进制数据形式的视频片段。接收应用程序（通常是网络浏览器或媒体播放器）按接收顺序播放这些片段。第一个 M4S 段由它包含的初始化数据标识。在 **summary** 中，M4S 文件是完整文件的单个小媒体片段。

## M4S 文件格式

M4S 文件基于 [ISO 基础媒体文件 (ISOBMFF) 格式](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)。大文件的这些小片段可以通过 HTTP 独立下载。因此，如果您有一个大的 [MP4](/zh/video/mp4/) 电影文件，则可以使用 MPEG-DASH（HTTP 上的动态自适应流式传输）技术将其分段为 M4S 分段文件，从而对其进行流式传输。如果将此大型电影文件作为 M4S 下载到光盘，则会下载多个 M4S 文件。如果将所有这些 .m4s 段连接起来，就会生成一个完整的可播放文件。除非文件的第一个初始化段也可用，否则媒体播放器无法播放文件。

## 关于 MPEG-DASH 流媒体

MPEG-DASH 使用自适应比特率流技术，可以通过 Internet 流式传输高质量的媒体内容。这是通过将内容分成一系列通过 HTTP 流式传输的小段来完成的。可以通过这种方式流式传输大型媒体文件，例如电影、播客或体育赛事的现场直播。这些段以不同的比特率编码。启用 MPEG-DASH 的媒体播放器使用比特率自适应算法自动选择具有最高比特率的片段。这避免了回放中的停顿或重新缓冲事件。

### M4S 文件的开源 API

有可用的开源 API 可用于读取和转换 M4S 文件。

* [libdash](https://github.com/bitmovin/libdash) - M4S 文件的 .NET API
* [dash.js](https://github.com/Dash-Industry-Forum/dash.js) - M4S 文件的 Javascript 客户端
* [创建 Dash 文件的 Go 库](https://github.com/zencoder/go-dash)

### 将 M4S 转换为 MP4 的开源 API

* [MFourStoMp4](https://github.com/muri11o/mfourstomp4)

## 参考 ＃＃＃

* [ISO 基础媒体文件 (ISOBMFF) 格式](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)
* [基于 HTTP 的动态自适应流 - MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)


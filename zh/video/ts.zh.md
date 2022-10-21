{
  "date" : "2021-12-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TS 文件格式 - 视频传输流文件",
  "keywords" :["ts","flie","扩展","扩展",".ts","格式"],
  "description":"了解什么是 TS 文件以及可以创建和打开 TS 文件的 API。",
  "linktitle" : "TS",
  "menu" : {
    "docs" : {
      "identifier":"video-ts",
      "parent" : "video"
}
},
  "lastmod" : "2021-12-16"
}

## 什么是一 .ts 文件？

扩展名为 .ts 的文件是将数据存储在 DVD 上的视频流。它使用 MPEG-2 ([.mpeg](/zh/video/mpg/)) 压缩算法来实现跨不同媒体类型（如互联网流媒体和广播）的最大效率和兼容性。创建了 TS 文件格式，以便它可以在互联网连接不佳的设备上播放，例如智能电视。

## TS 文件格式 - 更多信息

TS 文件中的数据类似于 [MP4](/zh/video/mp4/) 文件，但它被分成小块。每个块由一小段视频组成，然后是一段音频，以及一个可选的标题。一个 TS 文件由许多这样的块组成。除了视频、音频和字幕之外，每个块还包含一些额外的数据，用于检测块中的错误。因此，TS 文件的大小会稍大一些。

### 为什么要使用 TS 文件格式？

那么，如果 TS 文件的大小有点大，那么使用它们而不是其他文件格式有什么好处呢？好吧，在广播中，可以通过通信媒体（有线或无线电）实时发送微小的视频和音频块。接收方使用块中的额外数据来跳过容易出错的块。

此外，使用 TS 文件是因为广播系统不需要整个流来播放它。传输可以被拾取，并且可以通过组装音频和视频来实时使用。

## 如何播放 TS 文件？

好吧，TS 文件可以在流行的 [VideoLAN VLC 媒体播放器](https://www.videolan.org/vlc/features.html) 中打开和播放，免费提供下载。

## 参考 ＃＃

* [MPEG 传输流 - 维基百科](https://en.wikipedia.org/wiki/MPEG_transport_stream)


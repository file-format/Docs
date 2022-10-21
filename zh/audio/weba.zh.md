{
  "date" : "2022-07-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 WEBA 文件格式和可以创建和打开 WEBA 文件的 API。",
  "title" :"WEBA - 什么是 WebA 文件？",
  "linktitle" : "WEBA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2022-07-13"
}

## 什么是一 .WEBA 文件？

WEBA 是一种音频文件格式，仅包含从 [WEBM](/zh/video/webm/) 视频文件中提取的音频。它使用 OGG Vorbis 压缩编解码器进行压缩，从而减小了文件大小。这使得通过 Internet 传输 WEBA 文件变得更加容易。使用 [OGG](https://en.wikipedia.org/wiki/Ogg) Vorbis 压缩让大多数媒体播放器都支持 WEBA 文件。

**你可知道？**
您可以成为 FileFormat.com 的贡献者，让文件格式社区及时了解您的发现。如果您必须分享有关 WAV 或音频文件格式的任何内容，您可以在 [音频文件格式新闻](https://news.fileformat.com/t/audio) 部分发布您的发现，以便人们保持最新状态。

## WEBA 文件格式 - 更多信息

WEBA 文件使用 OGG Vorbis 压缩进行压缩，并以二进制文件的形式保存到光盘中。 OGG 是一种免费的开源容器文件格式，可提供高质量数字多媒体的高效流式传输和管理。由于它可以多路复用多个独立的音频、视频、文本和元数据流，它为存储从 WEBM 文件中提取的音频提供了理想的方法。

WEBA 文件格式位于 WEBM 文件格式规范的仅音频部分，如下所示。

|字段|说明|
---|---|
|MIME 类型 |video/webm|
|纯音频 MIME 类型 |audio/webm|
|统一类型标识符| org.webmproject.webm|
|视频编解码器名称| VP8 或 VP9|
|音频编解码器名称| Vorbis 或 Opus|

## 如何将 WEBA 文件转换为 SubRip SRT 文件？

WEBA 是音频文件，因此无法转换为字幕文件。但是，有免费的语音到文本转换器可以将 WEBA 文件作为输入并将其转换为 SubRip SRT 文件。一种这样的工具是基于 AI 的工具 Sonix，它可以在线将 WEBA 文件转换为 SRT。

## 如何将 WEBA 转换为其他音频格式？

WEBA 文件可以转换为其他音频文件格式。由于它基于免费和开源的 OGG 容器文件格式，许多 API 和应用程序可以读取 WEBA 并将其转换为其他文件格式，例如 [MP3](/zh/audio/mp3/)、[MP4](/zh/audio/ mp4/)、[FLAC](/zh/audio/flac/) 等等。 FFmpeg 就是这样一款可以将 WEBA 转换为 MP3 文件的软件。

## 参考

* [OGG 文件格式](https://en.wikipedia.org/wiki/Ogg)


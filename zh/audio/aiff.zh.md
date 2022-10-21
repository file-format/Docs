{
  "date" : "2021-04-26",
  "keywords" :["aiff","文件","扩展名","格式","音频交换文件格式","音乐","aiff 文件格式","aiff 到 mp3","aiff 与 wav","将 aiff 转换为mp3"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 AIFF 文件格式和可以创建、转换和打开 AIFF 文件的 API。",
  "title" :"AIFF - 音频交换文件格式",
  "linktitle" : "AIFF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## 什么是 .aiff 文件？
AIFF（音频交换文件格式）是 Apple 于 1998 年开发的一种未压缩音频文件格式，但基于 **EA IFF 85**（Electronic Arts 开发的交换格式文件标准），一种用于 Amiga 系统的包装格式.这种文件格式提供了存储采样声音的标准。该格式具有足够的灵活性，并且能够以各种采样率和采样宽度存储单声道或多声道采样声音。由于 AIFF 文件是未压缩的，这使得它们的大小比其他有损格式（例如 [MP3]（https://docs.fileformat.com/audio/mp3/））更大。这些文件由 2 个未压缩立体声音频通道组成，样本大小为 16 位，以 44.1 khz 录制。由于音频质量高，5 分钟的音频最多可占用 50MB 磁盘空间，类似于 [WAV](https://docs.fileformat.com/audio/wav/) 文件格式。

## AIFF 与 WAV
AIFF 和 WAV 在质量方面几乎相同。它们都使用相同的 PCM（脉冲编码调制）编码，这使得它们与其他有损格式相比更大，例如 [MP3](https://docs.fileformat.com/audio/mp3/)， [M4A]()。下表列出了一些一般差异：

|AIFF|WAV|
---|---|
|主要用于MAC|主要用于PC|
|允许元数据|不允许元数据|

## 文件结构
**EA IFF 85** 列出了在文件中存储数据的总体结构。 **EA IFF 85** 文件由许多数据块组成。一个块是 AIFF 文件的构建块，由一些头信息和数据组成：
{{< figure src="../chunk.png" alt="AIFF 块" >}}

AIFF 文件是许多不同类型的块的集合。有两种一般类型的块对于形成 AIFF 文件块很重要：
- **Common Chunk**：包含描述采样声音的重要参数，例如它的长度和采样率。
- **声音数据块**：包含实际的音频样本。
还有许多其他可选块列出仪器参数、定义标记、存储应用程序特定信息等。
 

### 本地块类型

下表给出了形成 AIFF 的块类型：

|块类型|说明|
---|---|
|Common Chunk|Common Chunk 描述了采样声音的基本参数|
|声音数据块|声音数据块包含实际的样本帧|
|标记块|标记块包含指向声音数据中位置的标记|
|Instrument Chunk|Instrument Chunk 定义了乐器（例如采样器）可以用来播放声音数据的基本参数|
|MIDI 数据块|MIDI 数据块可用于存储 MIDI 数据|
|音频记录块|音频记录块包含与音频记录设备相关的信息|
|应用程序特定块|应用程序制造商可以将应用程序特定块用于任何目的|
|Comments Chunk|Comments Chunk 用于在 FORM AIFF 中存储评论|
|文本块 - 名称、作者、版权、注释|都是文本块|

## 参考 ＃＃

* [音频交换文件格式 - 维基百科](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format)


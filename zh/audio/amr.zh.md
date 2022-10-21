{
  "date" : "2021-04-29",
  "keywords" :[ "amr", ".amr", "file", "extension", "format", "什么是 amr 文件", "music", "amr 文件格式", "amr 文件","将 amr 文件转换为mp3", "播放 amr 文件"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 AMR 文件格式和可以创建、转换和打开 AMR 文件的 API。",
  "title" :"AMR - 自适应多速率编解码器文件",
  "linktitle" : "AMR",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-29"
}

## 什么是一 .amr 文件？
扩展名为 .amr 的文件是与 **Adaptive Multi-Rate** 音频编解码器相关的音频数据格式；由一个多速率窄带语音编解码器组成，它以 4.75-12.2 kbit/s 的比特率对窄带信号进行编码，长途质量语音从 7.4 kbit/s 开始；使用链路自适应从基于八种不同比特率的一种中进行选择。

## AMR 文件格式
AMR 文件格式使用了许多编码技术，其中 ACELP（代数代码激励线性预测）算法是最好的技术之一；旨在以更有效的方式压缩人类语音音频。 AMR 于 1999 年被 3GPP 设定为标准语音或语音编解码器。AMR 文件格式也用于存储语音音频，使用许多智能手机使用的 **Adaptive Multi-Rate** 音频编解码器来存储录制的演讲。

### 文件格式结构
AMR（自适应多速率）是一种音频格式；广泛用于各种移动应用程序和设备，通常用于音频播放器/录音机或 VoIP 类应用程序。 AMR可以进一步分类为：

1. AMR-NB（窄带）
2. AMR-WB（宽带）

通常，AMR 是指 AMR-NB。 AMR 文件格式具有以下结构：

每个 AMR 文件都包含一个 6 字节的标头，可将文件识别为 AMR 音频。此标头始终设置为：
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

这通常适用于所有 AMR-NB 文件。如果标头遵循标准，则文件很可能已损坏，不应使用。 AMR 文件由大量打包的音频帧组成。这些帧每个组成 20 毫秒的音频。每个帧都可以使用任何有效的 AMR-NB 模式（0-7，DTX 模式中的 8 SID）进行编码。由于可以以不同的比特率对帧进行编码，因此这种典型的方法称为自适应多速率 (AMR)。
#### AMR 模式
以下是不同的 AMR 模式及其对应的比特率：

|模式|比特率|
---|---|
|0| AMR 4.75 - 以 4.75kbit/s 编码|
|1 | AMR 5.15 - 以 5.15kbit/s 编码|
|2 | AMR 5.9 - 以 5.9kbit/s 编码|
|3 | AMR 6.7 - 以 6.7kbit/s 编码|
|4 | AMR 7.4 - 以 7.4kbit/s 编码|
|5 | AMR 7.95 - 以 7.95kbit/s 编码|
|6 | AMR 10.2 - 以 10.2kbit/s 编码|
|7 | AMR 12.2 - 以 12.2kbit/s 编码|

AMR 模式的帧大小（包括头字节）如下所示：

|CMR |模式 |帧大小（以字节为单位）|
---|---|---|
|0 |AMR 4.75 |13|
|1 |AMR 5.15 |14|
|2 |AMR 5.9 |16|
|3 |AMR 6.7 |18|
|4 |AMR 7.4 |20|
|5 |AMR 7.95 |21|

## 参考 ＃＃

* [自适应多速率音频编解码器 - 维基百科提供](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)
* [AMR 和 AMR-WB 音频编解码器的 RTP 有效负载格式和文件存储格式](https://tools.ietf.org/html/rfc4867#page-35)


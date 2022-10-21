{
  "date" : "2021-08-09",
  "keywords" :["mmf","文件","扩展名","格式","音频","smaf","mmf 扩展名","mmf 文件","手机音乐文件","yamaha"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 MMF 文件格式和可以创建和打开 MMF 文件的 API。",
  "title" :"MMF - 移动音乐文件格式",
  "linktitle" : "MMF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-09"
}

## 什么是一 .mmf 文件？ ##

MMF 是与 SMAF 文件关联的文件扩展名。 MMF 代表移动音乐文件，而 SMAF 代表合成音乐移动应用程序格式。智能手机中的 MMF 文件包含系统铃声、声音，还可以包含图形和文本显示。 MMF 进一步包含三种类型的仪器参数，包括 FM、PCM 和 Stream PCM。这些文件格式与 Windows 系统平台兼容。 MMF 文件被归类为数据文件。通常，Microsoft Mail 支持 MMF 文件。带有 MMF 后缀的文件可以复制到任何移动设备或系统平台。
此外，与标准 MIDI 格式文件相比，这些文件的大小要小得多。 [WAV](/zh/audio/wav/) 和 [MID](/zh/audio/mid/) 文件可以转换为 MMF 格式，然后可以作为音频内容共享和分发。这些文件可以通过电子邮件直接接收到手机和 PC。


## 历史简介 ＃＃

Yamaha 开发了 SMAF 工具作为声音文件，以便智能手机可以存储更多独特的铃声。 Yamaha 介绍了 SMAF 并生产了他们的 MA-1、MA-2、MA-3、MA-5 和 MA-7 LSI 声音芯片。所有这些格式在 2000 年初在东亚市场的手机中变得非常熟悉。

在国际层面，MMF 格式得到了三星的授权。在 MMF 格式的帮助下，三星能够设计用于三星智能手机的各种和弦铃声。

雅马哈希望使该格式更加流行等官方雅马哈 SMAF 文件，它发布了更多与此格式兼容的工具。有了这个用户现在可以轻松地在他们的计算机上播放 MMF 文件。


## MMF 文件格式规范 ##

MMF 文件分为数据部分。围绕 8 字节的前缀结构用于描述每个段。
4 字节标签包括 CNTI、OPDA、MSTR、MTR 和 ATR。数据大小加上 8 个字节就是块大小；整个文件大小是通过将所有块大小相加来计算的。如果文件没有损坏，则总文件大小应与主标题大小相同。

### 标题###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

以下是 MMF 文件的示例：

![](../mmf.png)

## 参考 ＃＃

* [MMF - 维基百科提供](https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)


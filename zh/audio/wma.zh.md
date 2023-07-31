{
  "date" : "2021-02-20",
  "keywords" :["WMA","文件","扩展名","格式","音频交换文件格式","音乐"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 WMA 文件格式和可以创建和打开 WMA 文件的 API。",
  "title" :"WMA - Windows 媒体音频文件",
  "linktitle" : "WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-20"
}

## 什么是一 .wma 文件？

扩展名为 .wma 的文件表示以高级系统格式 (ASF) 格式保存的音频文件。 ASF 是 Microsoft 的专有格式，包含由 Windows Media Audio 9 编码的比特流。除了音频内容之外，WMA 文件还包含元数据对象，例如曲目的标题、专辑、艺术家和流派。 WMA 文件主要用于类似于 [.mp3](/zh/audio/mp3/) 文件的网络流式传输。

## WMA 文件格式

WMA 文件是二进制文件格式，包含在 ASF 文件格式中。它指定有关文件的元数据的编码，类似于 MP3 文件使用的 ID3 标记。 WMA 编解码器自 2008 年以来一直被 Microsoft 在其受保护的可互操作文件格式 (PIFF) 中使用。但是，DECE UltraViolet 和 MPEG-DASH 等相关行业标准并未将其声明为标准化音频编解码器。

### WMA 类型特定数据

Windows Media Audio 编解码器的类型特定信息以以下格式存储，作为流属性对象的类型特定数据的一部分。

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## 参考

* [ASF 概述 - 微软](https://learn.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format)


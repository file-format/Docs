{
  "date" : "2021-08-05",
  "keywords" :[ "gsm", "file", "extension", "format", "Audio", "Global System for Mobile Audio", "gsm extension", "gsm files"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 GSM 文件格式和可以创建和打开 GSM 文件的 API。",
  "title" :"GSM - 全球移动音频文件格式系统",
  "linktitle" : "GSM",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-05"
}

## 什么是一 .gm 文件？ ##

GSM 是与全球移动音频格式文件系统相关联的文件扩展名。可以在 Linux、Windows 和 Mac OS 平台上打开包含 GSM 扩展名的文件。 GSM 文件格式属于音频文件类别。

GSM 文件使用有损 CBR（恒定比特率）声音压缩编解码器进行编码。 GSM 音频文件中的采样率为 8000 个样本/秒，而数据速率约为 13 kbps。 GSM 文件中的比特率可确保录音过程中的质量。此外，GSM 文件格式也被称为手机中使用的全球标准格式，WAV 文件也可以使用 GSM 文件格式轻松编码。 GSM 文件的任何问题都可以由用户自己轻松解决，而无需求助专家。用户还可以将 GSM 文件转换为 [MP3](/zh/audio/mp3/) 和 [MP4](/zh/video/mp4/) 格式。

## 历史简介 ＃＃

GSM 是一种为欧洲互联网电话创建的音频文件格式。它由欧洲电信标准协会 (ETSI) 开发，用作移动电话和平板电脑中使用的 2G 数字蜂窝。今天，它用于存储电话交谈和语音信息的录音。

## GSM 文件格式规范 ##

GSM 在一个结构化的网络上工作，该网络由以下部分组成：

- **调制**：将输入数据转换为易于传输的格式的过程。传输的数据在接收端解调
- **传输速率**：GSM 是一种数字系统，比特率超过 270 kbps
- **上行频率范围**：933-960 MHz
- **下行频率范围**：890 – 915 MHz
- **Channel Spacing** ：表示相邻屏障之间的间距，应为 200 kHz 左右
- **双工距离**：它是上行链路和下行链路频率之间的空间，应为 80 MHz
- **语音编码**：GSM 使用线性预测编码 (LPC)。 LPC 压缩比特率。当音频信号通过滤波器并模仿声道时。 GSM 以 13kbps 编码语音

|音频压缩格式 |算法 |采样率 |比特率变换 |延迟 |社区康复 |视频广播 |立体声 |多通道 |
| ------------------------------------ | --------- | ------------ | ------------------ | -------- | --- | --- | ------ | ------------ |
| |
| GSM-HR | VSELP | 8 kHz | 5.6 kbit/s | 25 毫秒 |是 |没有 |没有 |没有 |
| GSM-FR | RPE-LTP | 8 kHz | 13 kbit/s | 20–30 毫秒 |是 |没有 |没有 |没有 |
| GSM-EFR | ACELP | 8 kHz | 12.2 kbit/s | 20–30 毫秒 |是 |没有 |没有 |没有 |


## 参考 ＃＃

* [GSM - 维基百科](https://en.wikipedia.org/wiki/Comparison_of_audio_coding_formats)


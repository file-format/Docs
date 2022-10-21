{
  "date" : "2019-12-13",
  "keywords" :["AAC","文件","扩展名","格式","音频编码","MPEG"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 AAC 文件格式和可以创建和打开 AAC 文件的 API。",
  "title" :"AAC - 高级音频编码文件",
  "linktitle" : "AAC",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-03-03"
}

## 什么是一 .aac 文件？

AAC（高级音频编码）是指基于有损音频压缩表示音频文件的数字音频编码标准。它是作为**[MP3](/zh/audio/mp3/)** 文件格式的继任者推出的，考虑到基于数据压缩方法的开发，在编码过程中实施新思想所面临的横向问题。在相同的比特率下，AAC 的音质比 MP3 更好。它在 MPEG-2 第 7 部分 (ISO/IEC 13818-7) 中定义，并在 MPEG-4 第 3 部分 (ISO/IEC 14496-3) 中以更新形式定义。该格式被 YouTube、iPhone、iPod、iPad、Apple iTunes 和其他几个平台采用为默认媒体格式。一些应用程序和 API 可用于将 AAC 文件格式转换为其他格式，例如 MP3、WMA、M4A、**[WAV](/zh/audio/wav/)** 等。

## 历史简介 ＃＃

AAC 文件格式是 MP3 的增强版本，有一些改进。该格式由包括弗劳恩霍夫研究所（Fraunhofer IIS - MP3 的开发商）、诺基亚、杜比、AT&T 和索尼在内的多家公司提供，于 1997 年 4 月被运动图像专家组 (MPEG) 宣布为国际标准。1999 年晚些时候， MPEG-2 Part 7 已更新并包含在 MPEG-4 系列标准中。它被称为 MPEG-4 Part 3，标识为 ISO/IEC 14496-3: 1999 或 MPEG-4 Audio。

## AAC 文件格式规范 ##

AAC 文件格式规范允许比 MP3 更灵活地设计编解码器，从而产生更多并发编码策略和有效压缩。该格式已成为许多硬件平台的选择，因为它在提供对更多选项的支持方面比 MP3 进行了改进，即使比特率较低。 AAC 文件格式规范可作为 [MPEG-2 Part 7](https://www.iso.org/standard/43345.html) 和 [MPEG-4 Part 3](https://www.iso.org /standard/53943.html)（不可免费下载）。该格式使用以下媒体类型：

* 音频/aac
* 音频/aacp
* 音频/3gpp
* 音频/3gpp2
* 音频/mp4
* 音频/mp4a-latm
* 音频/mpeg4-通用

## AAC 与 MP3 - 改进 ##

AAC和MP3在改进方面的主要区别如下：

* AAC 支持更广泛的通道（最多 48 个）和采样率（从 8 kHz 到 96 kHz）
* AAC 在 16 kHz 以上有更好的编码频率
* AAC 对一组滤波器的频率-时间分辨率的变化有更广泛的限制，从而改进了音频信号的瞬态和静止部分的编码
* 更高效、更简单的滤波器组：混合滤波器组已被标准 MDCT（改进的离散余弦变换）取代
* 使用时间噪声整形 (TNS)、MDCT 时间的预测系数（长期预测）、参数立体声、感知噪声替换、频谱带复制 (SBR) 支持增强的压缩效果。
* 更灵活的联合立体声（不同的频率范围可以使用不同的方法）；

## 参考 ＃＃

* [AAC - 维基百科提供](https://en.wikipedia.org/wiki/Advanced_Audio_Coding)


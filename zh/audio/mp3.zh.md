{
  "date" : "2019-12-13",
  "keywords" :["MP3","文件","扩展名","格式","音频","MPEG"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 MP3 文件格式和可以打开和创建 MP3 文件的 API。",
  "title" :"MP3 - 音频文件格式",
  "linktitle" : "MP3",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2020-09-04"
}

## 什么是 MP3 文件？

扩展名为 .mp3 的文件是音频文件的数字编码文件格式，正式基于 MPEG-1 音频层 III 或 MPEG-2 音频层 III。它由使用第 3 层音频压缩的运动图像专家组 (MPEG) 开发。 MP3 文件格式实现的压缩是 .WAV 或 .AIF 文件大小的 1/10。该格式提供了通过 Internet 流式传输此类音频文件以在线收听的优势，这在以前是不可能的，因为音频文件的文件大小很大。 MP3 音频文件的音质可以通过比特率、采样率、联合或普通立体声等参数设置来控制。

## MP3简史##

MP3 格式是由一家德国公司 Fraunhofer-Gesellshart 发明和开发的。该算法已获得其使用的压缩技术的许可专利。这是一个方便的 MP3 时间表：

• **1987** - 德国的弗劳恩霍夫研究所开始研究高质量的低比特率音频编码。它被称为 EUREKA 项目 EU147，数字音频广播。

• **1988 年 1 月** - 运动图像专家组 (MPEG) 成立。

• ** 1989 年 4 月** - Fraunhofer 在德国获得了 MP3 专利。

• **1992** - 帮助 Fraunhofer 进行研究的 Dieter Seitzer 将他的音频编码与 MPEG-1 集成在一起。

• **1993** - MPEG-1 标准发布。

• **1994** - MPEG-2 标准被开发并在一年后发布。

• **十一月1996 年 2 月 26 日** - 发布了 MP3 的美国专利。

• **1998 年9 月** - 弗劳恩霍夫开始执行专利权。使用 MP3 音频编码的人向弗劳恩霍夫支付了许可费。

• **1999 年2 月** - SubPop，一家唱片公司，以MP3 格式发行音乐，这是第一家这样做的公司。

• **1999** - 第一台便携式 MP3 播放器出现。

## MP3 文件格式##

MP3 文件由 MP3 帧组成，其中每个帧由一个标题和一个数据块组成。帧不是独立的，通常不能在任意帧边界处提取。文件的数据块包含有关音频的频率和幅度信息。标头中的同步字标识有效帧的开始。接下来是 3 位，其中第 1 位表示它是 MPEG 标准，其余 2 位表示使用了第 3 层；因此 MPEG-1 Audio Layer 3 或 MP3。在此之后，值会有所不同，具体取决于 MP3 文件。[ISO](https://en.wikipedia.org/wiki/International_Organization_for_Standardization)/[IEC](https://en.wikipedia.org/wiki/International_Electrotechnical_Commission ) 11172-3 定义了标题的每个部分的值范围以及标题的规范。今天大多数 MP3 文件包含 [ID3](https://en.wikipedia.org/wiki/ID3) [元数据](https://en.wikipedia.org/wiki/Metadata)，它位于 MP3 帧之前或之后，如图所示。数据流可以包含一个可选的校验和。

## 参考 ＃＃

* [MP3 - 维基百科提供](https://en.wikipedia.org/wiki/MP3)


{
  "date" : "2021-06-09",
  "keywords" :["m4p","mp3","文件","扩展名","格式","什么是 m4p 文件格式","音乐","m4p 文件格式","M4b vs MP3","m4p 文件格式规范" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 M4P 文件格式和可以创建、转换和打开 M4P 文件的 API。",
  "title" :"M4P - MPEG-4 有声读物文件格式",
  "linktitle" : "M4P",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## 什么是一 .m4p 文件？
扩展名为 .m4p 的文件是一个音频文件，通常可以在 Apple iTunes 商店下载。换句话说，我们可以说 M4P 是一个 AAC 文件，但使用数字版权管理 (DRM) 进行了版权保护。这意味着 M4P 文件只能在授权的系统或设备上播放。通常 M4P 文件特定于 Apple 多媒体设备。所以这些文件只能在 Apple macbooks、播客、iPhone 6 或 iPhone 7 等智能手机上播放。

## M4P 文件格式
M4P 代表 MPEG 4 Protected（音频），它使用高级音频编解码器 (AAC) 对音频进行编码，并保护文件免遭未经授权的使用。这种文件格式通常被认为是 iTunes Music Store 的音频文件格式。 Apple 使用其 FairPlay 数字版权管理 (DRM) 系统来保护 M4P 文件。 FairPlay DRM 基于 Veridisc 开发的技术。其保护机制通过使用 AES 加密对 AAC 音频流进行加密来工作。用户收到分配给他的帐户用于解密的主密钥。这种文件格式是作为 MP3 文件格式的替代品而引入的，因为 MP3 最初并不是作为音频文件，而是作为 MPEG 1 或 2 视频文件中的第三层。


## M4P 文件格式规范

与 [M4A](/zh/audio/m4a/) 类似，M4P 文件也由连续的块组成。每个块有 8 个字节的头，并细分为：
- 4字节块大小（大端，高字节优先）
- 4 字节块类型 - 预定义签名之一：“mdat"、“moov"、“pnot"、“moof"、“udta"、“uuid"、“free"、“skip"、“ftyp"、 “jP2"、“wide"、“load"、“imap"、“matt"、“chap"、“kmat"、“clip"、“crgn"、“sync"、“tmcd"、“PICT"、“scpt" "、"ctab"、"ssrc"。

与 M4A 类似，M4P 中的第一个块的类型为“ftype"，并且在偏移量 8 处有一个子类型。由子类型定义的 M4P 必须是“M4P_"。

迭代块，直到检测到未知类型的块，它将组成 M4P（MPEG-4 音频）文件。

## 参考 ＃＃

* [MPEG-4 第 14 部分 - 维基百科提供](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 音频 (M4A,M4B,M4P) 格式和恢复示例](https://www.file-recovery.com/m4a-signature-format.htm)


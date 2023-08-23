{
  "date" : "2021-06-09",
  "keywords" :[ "m4b","mp3","文件","扩展名","格式","什么是 m4b 文件格式","音乐","m4b 文件格式","M4b vs MP3","m4b 文件格式规范" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 M4B 文件格式和可以创建、转换和打开 M4B 文件的 API。",
  "title" :"M4B - MPEG-4 有声读物文件格式",
  "linktitle" : "M4B",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## 什么是一 .m4b 文件？
扩展名为 .m4b 的文件是 Apple 图书和 iTunes 普遍使用的有声读物。此格式中使用的音频以 MPEG-4 格式存储，并使用 AAC 编码进行压缩。 M4B 文件与 M4A 非常相似，但支持有声读物相关功能，例如书签和分节。 M4B 文件在启用 DRM 和无 DRM 版本中均可用。 DRM 加密有声读物通常是来自 iTunes Store 的付费有声读物。然而，可以通过互联网轻松找到免费的 DRM。

## M4B 文件格式
包含元数据、图像、书签和超链接的有声读物文件可以使用 .m4a 扩展名保存，但通常在保存时使用 .m4b 扩展名，只是为了指定文件具有有声读物文件格式。 Fairplay DRM（数字版权管理）被 apply 用来保护他们的 M4B 文件。因此，从 iTunes 下载的文件只能在授权设备或计算机上播放。


## M4B 与 M4A

M4B 和 [MP3](/audio/mp3/) 都是纯音频文件格式。

**M4B**：如果以相同的比特率进行编码，则在质量方面优于 MP3。 M4B 是使用 AAC 编码压缩的有声读物文件。它基本上与“MPEG-4 音频层"相关联，扩展名为 .m4b 的文件是 MPEG-4 电影的音频层，但具有额外的有声读物相关功能。它的目标是超越 MP3，成为音频压缩的新标准。它在许多方面都非常接近 MP3，但在相同甚至更小的文件大小下具有更好的质量。 M4B 格式最早由 Apple 引入。格式类型也实现为 Apple 无损编码器 (ALE)。

因此，目前M4B无法获得MP3的主流成功，因为音频格式还不能普遍播放。

**Mp3**：一种大家都很熟悉的数字音频格式。现场第一种压缩格式，并在音乐听众中非常有名。它的主流成功是如此迅速，以至于该文件类型能够被普遍播放并与几乎任何硬件或软件兼容。一般来说，M4A会产生更好的音质，但很多人会认为，无论是真是假，声音差异都没有可比性，将MP3文件转换为M4A文件是浪费时间。最后，转换只会让你失去原来的音质。

## M4B 文件格式规范

与 [M4A](/zh/audio/m4a/) 类似，M4B 文件也由连续的块组成。每个块有 8 个字节的头，并细分为：
- 4字节块大小（大端，高字节优先）
- 4 字节块类型 - 预定义签名之一：“ftyp"、“mdat"、“moov"、“pnot"、“moof"、“udta"、“uuid"、“free"、“ctab"、 “skip"、“jP2"、“wide"、“load"、“imap"、“matt"、“chap"、“kmat"、“clip"、“crgn"、“sync"、“tmcd"、“PICT" "、"scpt"、"ssrc"。

与 M4A 类似，M4B 中的第一个块的类型为“ftype"，并且在偏移量 8 处有一个子类型。由子类型定义的 M4B 必须是“M4B_"。

迭代块，直到检测到未知类型的块，它将组成 M4B（MPEG-4 音频）文件。

## 参考 ＃＃

* [MPEG-4 第 14 部分 - 维基百科提供](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 音频 (M4A,M4B,M4P) 格式和恢复示例](https://www.file-recovery.com/m4a-signature-format.htm)


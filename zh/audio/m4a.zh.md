{
  "date" : "2021-04-26",
  "keywords" :["m4a","mp3","文件","扩展名","格式","什么是 m4a 文件格式","音乐","m4a 文件格式","M4A vs MP3","m4a 文件格式规范" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 M4A 文件格式和可以创建、转换和打开 M4A 文件的 API。",
  "title" :"M4A - MPEG-4 音频文件",
  "linktitle" : "M4A",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## 什么是一 .m4a 文件？
**M4A 文件格式** 是使用称为有损压缩的 AAC（高级音频编码）创建的音频文件。 M4A 一词缩写为 MPEG 4 音频。这些音频文件通常具有 .m4a 文件扩展名。对于未受保护的内容尤其如此。它可以存储各种类型的音频内容，例如有声读物、歌曲和播客。 M4A 通常被认为是比 MP3 更高级的格式，而 MP3 通常不是为音频而设计的。它只是 MPEG 1 或 2 视频文件中的音频层。 M4A 格式由 FairPlay 数字版权管理加密，通过 iTunes Store 出售时使用 .m4p 扩展名。 Apple iPhone 使用 MPEG-4 音频作为铃声，但这些音频文件使用 .m4r 扩展名。


## M4A 与 MP3

M4A 和 [MP3](https://docs.fileformat.com/audio/mp3/) 都是纯音频文件格式。

**M4A**：以相同比特率编码时，在质量和大小方面优于 MP3。 .m4a 文件扩展名非常常见，因为它们已被 Apple 用于 iTunes Music Store。 M4A 是使用 MPEG-4 技术压缩的音频文件；一种有损压缩算法。它基本上与“MPEG-4音频层"相关联，扩展名为.m4a的文件是MPEG-4电影的音频层。它旨在超越 MP3 并成为音频压缩的新标准。它在许多方面都非常接近 MP3，但引入它以在相同甚至更小的文件大小中具有更好的质量。 M4A 格式最早由 Apple 引入。格式类型也实现为 Apple 无损编码器 (ALE)。

因此，目前M4A无法获得MP3主流的成功，因为音频格式还不能普遍播放。它在某种程度上仅限于 MacOS、iPod 和其他 Apple 产品。

**Mp3**：最著名的数字音频格式。它也是现场最早的压缩格式之一，并在音乐爱好者中非常流行。它的主流成功是如此之快，以至于该文件类型能够被普遍播放，几乎可以用任何硬件或软件播放。一般来说，M4A会产生更好的音质，但很多人会认为，无论是真是假，声音的差异是无法区分的，将MP3文件转换为M4A文件是浪费时间。最终，转换只会让你失去原来的音质。

## M4A 文件格式规范

M4A 文件由连续的块组成。每个块有 8 个字节的头，并细分为：
- 4字节块大小（大端，高字节优先）
- 4 字节块类型 - 预定义签名之一：“ftyp"、“mdat"、“moov"、“pnot"、“udta"、“uuid"、“moof"、“free"、“skip"、 “jP2"、“wide"、“load"、“ctab"、“imap"、“matt"、“kmat"、“clip"、“crgn"、“sync"、“chap"、“tmcd"、“scpt" "、“ssrc"、“PICT"。

第一个块的类型为“ftype"，在偏移量 8 处有一个子类型。子类型定义的 M4A 必须是“M4A_"，对于 M4B 子类型必须是“M4B_"，对于 M4P 子类型必须是“M4P_"。

迭代块，直到检测到未知类型的块，它将组成 M4A（MPEG-4 音频）文件。

## 参考 ＃＃

* [MPEG-4 第 14 部分 - 维基百科提供](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 音频 (M4A,M4B,M4P) 格式和恢复示例](https://www.file-recovery.com/m4a-signature-format.htm)


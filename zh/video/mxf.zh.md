{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MXF - 材料交换格式",
  "keywords" :["MXF","matroska 视频","mkv 格式","如何播放 MXF 文件","SMPTE","多媒体","视频"],
  "description":"了解 MXF 文件格式和可以创建和打开 MXF 文件的 API。",
  "linktitle" : "MXF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-01"
}

## 什么是 MXF 文件？

扩展名为 .mxf 的文件是一种多媒体容器格式，其中包含数字视频和音频媒体以及有关文件的元数据信息。它遵循 SMPTE（电影和电视工程师协会）标准，该标准是一个由工程、技术和媒体和娱乐行业高管组成的全球专业人士协会。 MXF 文件可以转换为其他文件格式，例如 [AVI](/zh/video/avi/) 或 [MOV](/zh/video/mov/)。

## MXF 文件格式

MXF 文件实际上是由一定格式的字节序列组成的二进制文件。解码应用程序必须符合这种格式才能理解它并从中提取信息。该格式允许使用下面描述的 KLV 编码添加新项目而不会破坏向后兼容性。

* Key – 元素的标识符，一个 SMPTE 通用标签 (UL)
* 长度 – 数据的长度，它是用于减少此项所需空间量的可变长度编码
* Value – 元素的实际值。

### SMPTE 格式规范

MXF 文件格式已由以下 SMPTE 规范定义。

* SMPTE ST 377-1:2011。电视 — 材料交换格式 (MXF) — 文件格式规范
* SMPTE ST 377-2（截至 2012 年 1 月的工作正在进行中）。 MXF 的 KLV 编码扩展语法。
* SMPTE ST 378:2004（2010 年存档）。电视 — 材料交换格式 (MXF) — 操作模式 1a（单项、单包）
* SMPTE ST 379-1:2009。材料交换格式 (MXF) — MXF 通用容器
* SMPTE ST 379-2:2010。材料交换格式 (MXF) -- MXF 约束通用容器
* SMPTE ST 380:2004。电视 — 材料交换格式 (MXF) — 描述性元数据方案 1（标准、动态）
* SMPTE ST 381-1:2005。电视 — 材料交换格式 (MXF) — 将 MPEG 流映射到 MXF 通用容器（动态）
* SMPTE ST 381-2:2011。材料交换格式 (MXF) — 将 MPEG 流映射到受 MXF 约束的通用容器中
* SMPTE ST 382:2007。材料交换格式 (MXF) — 将 AES3 流和广播波音频映射到 MXF 通用容器
* SMPTE ST 383:2008。电视 — 材料交换格式 (MXF) — 将 DV-DIF 数据映射到 MXF 通用容器
* SMPTE ST 384:2005。电视 — 素材交换格式 (MXF) — 将未压缩图片映射到 MXF 通用容器
* SMPTE ST 385:2004。电视 — 材料交换格式 (MXF) — 将 SDTI-CP 本质和元数据映射到 MXF 通用容器中
* SMPTE ST 386:2004（2010 年存档）。电视 — 材料交换格式 (MXF) — 将 D-10 型本质数据映射到 MXF 通用容器
* SMPTE ST 387:2004（2010 年存档）。电视 — 材料交换格式 (MXF) — 将 D-11 型本质数据映射到 MXF 通用容器
* SMPTE ST 388:2004（2010 年存档）。电视 — 材料交换格式 (MXF) — 将 A-law 编码音频映射到 MXF 通用容器
* SMPTE ST 389:2005。电视 — 材料交换格式 (MXF) — MXF 通用容器反向播放系统元素
* SMPTE ST 390:2011。电视 — 材料交换格式 (MXF) — 专用操作模式“原子"（单个项目的简化表示）
* SMPTE ST 391:2004（2010 年存档）。电视 — 材料交换格式 (MXF) — 操作模式 1b（单项、组合包）
* SMPTE ST 392:2004。电视 — 材料交换格式 (MXF) — 操作模式 2a（播放列表项，单个包）
* SMPTE ST 393:2004。电视 — 材料交换格式 (MXF) — 操作模式 2b（播放列表项、组合包）
* SMPTE ST 394:2006。电视 — 材料交换格式 (MXF) — MXF 通用容器的系统方案 1
* SMPTE ST 405:2006。电视 — 材料交换格式 (MXF) — MXF 通用容器系统方案 1 的元素和单个数据项
* SMPTE ST 407:2006。电视 — MXF — 操作模式 3a 和 3b
* SMPTE ST 408:2006。电视 — MXF — 操作模式 1c、2c 和 3c
* SMPTE ST 410: 2008。材料交换格式 - 通用流分区。
* SMPTE ST 422:2006。材料交换格式 - 将 JPEG2000 码流映射到 MXF 通用容器
* SMPTE ST 429.4:2006。 D-Cinema 包装 — MXF JPEG 2000 应用程序
* SMPTE ST 429.5:2006。 D-Cinema Packaging - 定时文本轨道文件
* SMPTE ST 429.6:2006。 D-Cinema Packaging — MXF 轨道文件本质加密
* SMPTE ST 434:2006。材料交换格式——元数据和文件结构信息的 XML 编码
* SMPTE ST 436:2006。电视 — VBI 线路和辅助数据包的 MXF 映射
* SMPTE ST 2019-4:2009。将 VC-3 编码单元映射到 MXF 通用容器
* SMPTE ST 2037:2009。将 VC-1 映射到 MXF 通用容器
* SMPTE RP 2008:2008。材料交换格式 - 将 AVC 流映射到 MXF 通用容器
* SMPTE RP 2057:2011。 MXF 中基于文本的元数据载体
* SMPTE EG 41:2004。材料交换格式 (MXF) — 工程指南。注意：在 2012 年 1 月查阅时，该文档不再列在 SMPTE 网站上。
* SMPTE EG 42:2004。材料交换格式 (MXF) — MXF 描述性元数据
* SMPTE RDD 3:2008。 e-VTR MXF 互操作性规范
* SMPTE RDD 9-2009。 Sony MPEG Long GOP 产品的 MXF 互操作性规范
* SMPTE 元数据注册表电子表格菜单。

### MXF 结构元数据

结构元数据是 MXF 文件的基础，因为它包含有关文件内容的有用信息。 MXF 元数据包含帧速率、帧大小、文件创建日期和自定义修改日期等信息。结构元数据描述了 MXF 文件的结构和功能，包括从技术上描述各种基本组件并传达输出时间线的组成方式。

## 参考

* [MXF - 维基百科](https://en.wikipedia.org/wiki/Material_Exchange_Format)
* [MXF - 进度报告](http://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
* [用于 MXF 的开源 C++ 库](http://www.freemxf.org/)


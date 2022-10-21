{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MKV 文件格式",
  "keywords" :["mkv","matroska 视频","mkv 格式","如何播放 mkv 文件","视频","文件","格式"],
  "description":"了解 MKV 文件格式和可以创建和打开 MKV 文件的 API。",
  "linktitle" : "MKV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2020-17-11"
}


## 什么是 MKV 文件？ ##

MKV (Matroska Video) 是一种类似于 [MOV](/zh/video/mov/) 和 [AVI](/zh/video/avi/) 格式的多媒体容器，但它在同一文件中支持多个音频和字幕轨道。 MKV 文件是用于视频的 Matroska 多媒体容器格式。 MKV 基于可扩展二进制元语言，它支持多种视频和音频压缩格式。 MKV 和其他视频格式的主要区别在于 MKV 是一个容器而不是编解码器。 MKV 文件以 .mkv 文件扩展名保存。 MKV 可以将音频、视频和字幕合并到一个文件中，即使这些元素使用不同类型的编码。例如，您可以拥有一个包含 H.264 视频和 MP3 或 AAC 音频的 MKV 文件。 MKV 还支持描述、评级、封面艺术，甚至章节点。 MKV 有几个关键特性是面向未来的。这些功能包括：

- 支持快速搜索。
- 能够选择不同的音频和视频流。
- 支持字幕（硬编码和软编码）。
- 支持元数据、章节和菜单。
- 在线流式传输的能力。
- 能够恢复提供播放损坏文件的能力的错误文件。

## 历史简介 ＃＃

MKV 文件起源于 2002 年的俄罗斯。首席开发人员是 Lasse Kärkkäinen，他与 Matroska 的创始人 Steve Lhomme 和一个程序员团队一起工作。 MKV 是作为一个开放标准项目开发的，这意味着它是开源的并且可以免费使用。随着时间的推移，该格式得到改进，并在 2010 年成为 WebM 多媒体格式的基础。

## Matroska 设计##

Matroska 在 EBML 规范中添加了以下约束。

- **EBML Header** 的 **docType** 必须是 'matroska'。
- **EBML Header** 的 **EBMLMaxIDLength** 必须为 4。
- **EBML Header** 的 **EBMLMaxSizeLength** 必须介于 1 和 8（含）之间。

所有顶级元素都以 4 个八位字节编码。

- 语言代码：Matroska（版本 1 到 3）使用的语言代码可以是 3 个字母的书目 ISO-639-2 形式（如法语的“fre"），或者可以使用额外的国家代码，如“fre-ca" " 代表加拿大法语。从 Matroska 版本 4 开始，ISO 639-2 或 BCP 47 可以用于语言代码，但建议使用 BCP 47。
- 物理类型：这些对于音频和视频文件具有不同的含义。例如，ChapterPhysicalEquiv = 60 表示 (CD / 12" / 10" / 7" / TAPE / MINIDISC / DAT) 表示音频和 (DVD / VHS / LASERDISC) 表示视频。
- 块结构 - 块头：块头包含有关轨道号、时间戳、系带类型等的信息。
- Lacing：这是一种在存储数据时节省空间的机制，通常用于小数据块（帧）。有 3 种类型的系带：
  - Xiph: Frame with a size multiple of 255 coded with a 0 at the end of the size. For example, The code for 765 is 255;255;255;0.
  - EBML: The frame size is coded as a difference between the previous size and this size. The first size in the lace is unsigned but others use a range shift to get a sign on each value.
  - fixed-size: The size remains the same.
- SimpleBlock 结构：它受到 **Block 结构** 的启发，主要区别在于添加了 **Keyframe** 和 **Discardable** 标志。除此之外，一切都一样。

## Matroska 结构##

Matroska 文档必须由至少一个使用**Matroska Document Type** 的**EBML 文档** 组成。每个**EBML 文档** 必须以**EBML 标题** 开头，后跟定义为段的**EBML 根元素**。 Matroska 定义了几个可能出现在 **Segment** 中的顶级元素。

EBML 使用元素系统组成 EBML 文档，以下是 Matroska 文件中的顶级元素列表：

- **EBML 文档**：整个文件的包装器。
- **EBML Header**：它包含文件的标题信息，如 DocType。
- **Segment**：包含所有其他顶级元素的顶级元素。
- **SeekHead**：它包含其他顶级元素的段的位置。
- **信息**：它包含有关该段的一般信息。
- **曲目**：描述了许多曲目的顶级信息元素。
- **章节**：用于定义基本菜单和分区数据。
- **Cluster**：包含块结构的顶级元素。
- **Cues**：一个顶级元素，其中包含加速寻求访问的 Segment 本地的所有条目。
- **附件**：这包含附件。
- **标签**：此元素包含描述曲目、版本、章节、附件或整个片段的元数据。

下表显示了 Matroska 文档的结构，其中大部分元素以层次结构显示：

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| EBML 标题 | | | |
|细分 |寻头|寻求 |搜索ID |
| | | |寻找位置 |
| |信息 |段UID | |
| | |段文件名 | |
| | |上一页UID | |
| | |上一个文件名 | |
| | |下一个UID | |
| | |下一个文件名 | |
| | |细分家庭 | |
| | |章节翻译 | |
| | |时间戳刻度 | |
| | |持续时间 | |
| | |日期UTC | |
| | |标题 | |
| | |沐星App | |
| | |写作应用 | |
| |曲目 |跟踪条目 |轨道号 |
| | | | TrackUID |
| | | |轨道类型 |
| | | |姓名 |
| | | |语言 |
| | | |编解码器ID |
| | | |编解码器私人 |
| | | |编解码器名称 |
| | | |视频 |标志交错 |
| | | | |现场订单 |
| | | | |立体模式 |
| | | | |阿尔法模式 |
| | | | |像素宽度 |
| | | | |像素高度 |
| | | | |显示宽度 |
| | | | |显示高度 |
| | | | |纵横比类型 |
| | | | |颜色 |
| | | |音频 |采样频率 |
| | | | |频道 |
| | | | |位深度 |
| |章节 |版本条目 |版本UID |
| | | |版旗隐藏 |
| | | |版本标志默认 |
| | | | EditionFlagOrdered |
| | | |章原子 | ChapterUID |
| | | | | ChapterStringUID |
| | | | |章节时间开始 |
| | | | |章节时间结束 |
| | | | | ChapterFlagHidden |
| | | | |章节显示 |章节字符串 |
| | | | | |章节语言 |
| |集群 |时间戳 |
| | |无声曲目 |
| | |职位 |
| | |上一页尺寸 |
| | |简单块 |
| | |块组 |
| | |加密块 |
| |提示 |提示点 |提示时间 |
| | | |提示跟踪位置 |
| |附件 |附件 |文件描述 |
| | | |文件名 |
| | | |文件MimeType |
| | | |文件 UID |
| | | |文件推荐 |
| | | |文件使用开始时间 |
| | | |文件使用结束时间 |
| |标签 |标签 |目标 |目标类型值 |
| | | | |目标类型 |
| | | | |标签跟踪UID |
| | | | | TagEditionUID |
| | | | | TagChapterUID |
| | | | |标签附件UID |
| | | |简单标签 |标记名 |
| | | | |标记语言 |
| | | | |标签默认 |
| | | | |标签字符串 |
| | | | |标签二进制 |
| | | | |简单标签 |


### 使用编解码器###

如果您不想要新的媒体播放器并且更喜欢使用现有的播放器，则需要安装一些编解码器（压缩/解压缩的简写）。即使下载编解码器是一个有效的选项，您也应该小心来源，这些可能包含恶意软件。

## 参考 ＃＃

- [维基百科的 Matroska](https://en.wikipedia.org/wiki/Matroska)


{
  "date" : "2021-06-08",
  "keywords" :["AAX","文件","扩展名","格式","AAX 文件","音频","AAX 文件格式","什么是 aax 文件","AAX 文件格式规范"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 AAX 文件格式和可以创建和打开 AAX 文件的 API。",
  "title" :"AAX - 高级音频编码文件",
  "linktitle" : "AAX",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-08"
}

## 什么是一 .aax 文件？
带有.aax扩展名的文件是由[Audible]（https://www.audible.com/）开发的有声读物； Amazon.com Inc. 拥有的美国在线播客服务和有声读物。Audiblekids、Audible.com 和 iTune 商店可能会使用这些文件。 AAX 文件是数字多媒体有声读物，可能包括图形、视频、书签和视频时间线等功能；使它们成为儿童的**图画书**和**图画小说**的更有用和更合适的选择。 AAX 文件被视为 AA 文件的增强版本。


## AAX 文件格式
AAX 是一种有声读物文件格式，由于其可变比特率并使用 DRM（数字版权管理）加密算法加密，因此它是一种高质量的 M4B 文件。大多数电子书以 64 kbit/s、22.050 kHz、立体声编码，有些低至 32k，单声道和广播剧通常以 128kbit/s 和 44.1 kHz 编码。 AAX 文件格式的音频以 AAC 格式（可变质量）编码。

### AAX 文件格式规范
Audible 提供的有关 AAX 文件格式质量规范的详细信息如下所示：

- **比特率：** 32 - 128 kbit/s
- **采样率：** 22.050 - 44.10 kHz
- **位深度：** 未知
- **频道：** 单声道或立体声
- **MBytes/小时：** 28.8
- **容器：** MPEG-4 Part 14
- **质量描述：** AAC 声音

### 数字版权管理 (DRM)
Audible 文件格式封装了编码的声音，但它们还包括通过 Audible 用户名和密码防止未经授权的播放，默认情况下一次最多可在四台计算机和三部智能手机上使用。学校和图书馆可能会获得不同类型的许可证。 DRM 负责控制：
- 未经授权的用户访问
- 刻录有限数量的 CD 以不受限制地播放
- 为有限数量的设备启用有声内容
但是您仍然可以找到许多其他可以轻松绕过 Audible 的 DRM 控制的软件工具。 Audible 现在为内容作者提供无 DRM 的标题。 FFmpeg 2.8.1 或更高版本可以原生播放 .aax 文件格式。


## 参考 ＃＃

* [Audible (service) - By Wikipedia](https://en.wikipedia.org/wiki/Audible_(service))
* [音频文件格式 - 维基百科提供](https://en.wikipedia.org/wiki/Audio_file_format)


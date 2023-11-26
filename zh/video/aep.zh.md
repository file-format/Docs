{
  "date" : "2023-02-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AEP 文件 - After Effects 项目文件格式",
  "description":"了解 AEP 文件格式以及如何打开 AEP 文件。",
  "linktitle" : "AEP",
  "menu" : {
    "docs" : {
      "identifier":"video-aep",
      "parent" : "video"
}
},
  "lastmod" : "2023-02-21"
}

## 什么是 .aep 文件？

AEP 文件是保存 After Effects 项目时由 Adobe After Effects 创建的项目文件。它是 After Effects 用来保存与项目相关的所有设置和数据的主要文件类型，例如视频素材、静态图像、音频文件和任何其他效果。 AEP 文件包含有关合成、图层、关键帧、效果以及属于 After Effects 项目的其他元素的信息。

您可以使用 Adobe After Effects 软件打开 AEP 文件。

## AEP 文件格式 - 更多信息

Adobe After Effect 以二进制文件格式存储 AEP 文件。 AEP 文件的内部文件结构不公开供开发人员参考，因此只能在 Adobe After Effect 中打开。 AEP 文件存储对属于项目一部分的元素的引用，但实际上并不包含这些集合和元素。如果您在创建项目后移动参考文件，After Effects 将无法找到这些文件，并且您将无法使用这些媒体文件。

### After Effects 项目文件的类型

After Effects 将项目文件保存在：

* `AEP 文件` - 以二进制格式存储并且尺寸较小。二进制文件加载速度更快，并且可以轻松与其他用户共享。
* `AEPX 文件` - 这是基于 XML 的 After Effects 项目文件格式，以文本格式存储数据。 AEPX 文件通常比 AEP 文件格式更大且加载速度更慢。

## 如何转换 AEP 文件

AEP 文件可以转换为其他流行的文件格式，例如：

* [.MOV](/zh/video/mov/) - Apple QuickTime 电影
* [.AVI](/zh/video/avi/) - 音频视频交错
* [.JPG](/zh/image/jpeg/) - JPEG 图像
* [.PNG](/zh/image/png/) - 便携式网络图形
* .DPX - 数字图片交换
* .EXR - OpenEXR 图像
* .M4A - MPEG-4 音频
* [.MP3](/zh/音频/mp3/) - MP3 音频
* [.WAV](/zh/audio/wav/) - WAVE 音频
* .AEPX - After Effects XML 项目
* .AET - After Effects 模板
* .PRPROJ - Adobe Premiere Pro

## 参考

- [After Effects 项目类型](https://helpx.adobe.com/after-effects/using/projects.html)


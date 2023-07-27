{
  "date" : "2021-23-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MK3D 文件格式",
  "keywords" :["mk3d","matroska 视频","mkv 格式","立体 3d","StereoMode","视频","文件","格式"],
  "description":"了解 Matroska 创建的立体 3D 视频的 MK3D 文件格式以及可以创建和打开 MK3D 文件的 API。",
  "linktitle" : "MK3D",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-23-02"
}

## 什么是 MK3D 文件？ ##

MK3D 文件属于 Matroska 视频格式系列。这些文件实际上是使用 Matroska 3D 格式创建的 **立体 3d** 视频。 MKV 文件容器使用 StereoMode 字段的值来定义立体 3D 视频素材的类型。 StereoMode 值也可用于通过分离青色和红色 (AnaGlyph) 来显示旧的立体 3D 视频

## 技术细节 ＃＃
可以通过以下两种方式压缩 3D 视频：

- 每只眼睛的单独轨道。
- 将每个眼动追踪合并为一条轨道。

MKV 文件容器支持这两者。

对于其中包含 3D 素材的单轨视频，您必须设置 **StereoMode** 字段，该字段决定飞机是组装在单声道还是左右组合轨道中。您可以使用以下 StereoMode 字段值之一：

|价值 |说明 |
|---|---|
|0|单声道|
|1|并排（左眼在前）|
|2|自上而下（右眼在前）|
|3|自上而下（左眼在前）|
|4|棋盘（右为第一）|
|5|棋盘（左为第一）|
|6|行交错（右边是第一个）|
|7|行交错（左边是第一）|
|8|列交错（右边是第一个）|
|9|列交错（左为第一）|
|10|浮雕（青色/红色）|
|11|并排（右眼在前）|
|12|浮雕（绿色/洋红色）|
|13|双眼在一个块中（左眼在前）（场序模式）|
|14|双眼合一（右眼在前）（场序模式）|

对于多个轨道，MKV 容器需要分别决定每个轨道的功能。带有 **TrackCombinePlanes** 的 **TrackOperation** 用于完成这项工作。


## 参考 ＃＃

- [Matroska 规范说明](https://www.matroska.org/technical/notes.html)
- [对立体 3D 视频和 MK3D 文件的 MKV 文件容器支持](https://3dvision-blog.com/5520-mkv-file-container-support-for-stereo-3d-video-and-the-mk3d-files/)


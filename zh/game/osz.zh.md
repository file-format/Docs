{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 OSZ 文件格式和可以创建和打开 OSZ 文件的 API。",
  "title" :"OSZ 文件 - osu! Beatmap 文件格式",
  "linktitle" : "OSZ",
  "menu" : {
    "docs" : {
      "identifier":"game-osz",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## 什么是 .osz 文件？

OSZ 文件是节奏游戏 osu! 使用的压缩文件格式。存储谱面数据。 Beatmaps 本质上是游戏的关卡，它们包括歌曲、节拍时间和游戏屏幕上击中对象的位置等信息。 OSZ 文件允许轻松分发谱面图，通常从互联网下载并导入到游戏中。俄勒冈州立大学！也有 [OSR](/zh/game/osr/) 文件格式，是游戏回放文件，可供游戏玩家回放。

**OSR 文件格式的 MIME 类型：** x-osu-replay

## OSZ 文件格式

OSZ 文件类型的内部文件格式详细信息不公开。它包含 [ZIP](/zh/compression/zip/)-压缩数据，其中包含播放音乐、显示图形以及在玩家必须与游戏交互时显示有关事件的信息。

## 如何创建 OSZ 文件？

俄勒冈州立大学！有关于[创建 OSZ](https://osu.ppy.sh/wiki/en/Client/File_formats#creating-.osz-and-.osk-files) 的详细说明
 和 OSK 文件。以下步骤可用于使用 OSU! 创建 OSZ 文件。

1. 通过编辑器打开谱面。
1. 从顶部菜单中，选择文件 > 导出包...。
1. .osz 存档将放置在 osu! 内的 Exports 文件夹中文件夹。

## 参考

* [俄勒冈州立大学！节奏游戏](https://osu.ppy.sh/home)

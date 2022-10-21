{
  "date" : "2022-03-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"了解 WUD 文件格式和可以创建和打开 WUD 文件的 API。",
  "title" :"WUD 文件格式 - Wii U 盘映像文件",
  "linktitle" : "WUD",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-03-13"
}

## 什么是一 .wud 文件？

带有 .wud 扩展名的文件是从 Wii U 游戏光盘创建的磁盘映像。生成的光盘映像文件可以由 [Cemu](https://cemu.info/) 等视频游戏模拟器加载以模拟游戏。 WUD 文件很大，因此被创建为多个段以便于传输。游戏信息以大约 2 GB 文件大小的 WUD 文件段导出。打开应用程序，如 Cemu，需要在打开这些分段文件之前将所有这些分段文件合并到一个 WUD 文件中。

## WUD 文件格式

WUD 文件以专有文件格式保存到光盘中，并且可以加载到 Cemu 模拟器中以在 PC 上模拟 Wii U 应用程序。由于它的大小，WUD 文件被[压缩](/zh/compression/) 以减小其文件大小。生成的压缩文件称为 WUX 文件。

## 参考

* [Wii U 模拟器 - Cemu](https://cemu.info/)
* [Cemu - 维基百科](https://en.wikipedia.org/wiki/Cemu)


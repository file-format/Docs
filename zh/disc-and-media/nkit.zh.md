{
  "date" : "2022-04-01",
  "keywords" :[ "nkit 文件","nkit 文件格式","什么是 nkit 文件","文件","nkit 示例","nkit 文件扩展名","扩展名","格式","nkit 页脚","文件nkit格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"了解 NKIT 文件格式和可以创建和打开 NKIT 文件的 API。",
  "title" :"NKIT - 磁盘映像文件格式",
  "linktitle" : "NKIT",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-04-01"
}

## 什么是一 .nkit 文件？

NKIT 文件是从 NintendoWii 和 GameCube 游戏中提取的数据的磁盘映像。 NKIT 适用于 Nintendo Toolkit 格式。生成的压缩 [ISO](/zh/compression/iso/) 文件利用这些游戏的主要数据与 Dolphin、Swiss 和 Nintendont 等模拟器程序一起运行。 NKit 提供原始 (iso) 和压缩 (gcz) 文件格式，它们的设计都考虑了可播放性和大小。

## NKIT 文件格式

NKit 文件格式是一种无损格式，用于缩小和恢复 Nintendo Wii 和 GameCube 图像。对于 GameCube 和 Wii 游戏，这些格式以 ISO 和 GCZ 文件格式提供。

|系统 |格式 |支持硬件 |Dolphin 支持 |可恢复 1:1 |备注|
---|---|---|---|---|---|
|游戏方块| nkit.iso|是 |是|是 |与压缩 GameCube iso 相同|
|游戏方块| nkit.gcz|没有|是|是 |GCZ 是 Dolphin 自己的块可搜索压缩格式|
|Wii| nkit.iso|否 是|是| RVT-H 格式只能在 Dolphin 中播放|
|Wii| nkit.gcz|否 是|是| GCZ 中的 RVT-H 只能在 Dolphin 中播放|

### NKIT 标头

NKIT 文件格式头如下。

|偏移量 |长度 |名称|
---|---|---|
|0x200 |0x4 |NKit 标头“NKIT"|
|0x204 |0x4 |NKit 版本“v01"|
|0x208 |0x4 |源图原CRC32|
|0x20C |0x4 |NKit CRC - 使 NKit 文件 CRC32 等于 0x208 处的源 CRC（在 GCZ 中为 0x4）|
|0x210 |0x4 |源图片长度|
|0x214 |0x4 |强制垃圾 ID（当光盘 ID 不同时 - 罕见 - 仅限 GameCube）|
|0x218 |0x4 |Wii 更新分区 CRC32 如果在转换时删除|

## 参考 ＃＃

* [NKIT 文件格式 - gbatemp](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)


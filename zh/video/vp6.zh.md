{
  "date" : "2021-02-15",
  "keywords" :["vp6 文件","vp6 文件格式","什么是 vp6 文件","文件","vp6 示例","vp6 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP6 - TrueMotion 视频文件",
  "description":"了解 VP6 文件格式和可以创建和打开 VP6 文件的 API。",
  "linktitle" : "VP6",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## 什么是 VP6 文件？

VP6 是 On2 技术于 2003 年 5 月推出的一种有损压缩视频格式。它是 TrueMotion 开发的 V3、V4 和 V5 系列视频编解码器的一部分。该格式很快被用于广播领域，例如 BBC 报道和 QuickLink 软件。 VP6 在 2005 年 1 月被 VP7 Codec 取代，具有更好的压缩兼容性。

## VP6 文件格式

V6 文件的完整规范不公开。 On2 最初公开了这些规范，但很快这些规范就对普通用户不可用。 VP6 文件格式的非官方文档可在 [multimedia wiki](https://wiki.multimedia.cx/index.php?title=On2_VP6) 获得，可供开发人员参考。

### 宏块 (MB)

与 MPEG-2、MPEG-4 第 2 部分和第 10 部分类似，VP6 文件的每个视频帧都由 16x16 宏块 (MB) 阵列组成。每个 MB 可以处于以下模式之一：

* 内部 MB
* Inter MB，null MV，前一帧参考
* Inter MB，差分 MV，前一帧参考
* Inter MB，四个 MV，前一帧参考
* Inter MB, MV 1, 前一帧参考
* Inter MB, MV 2, 前一帧参考
* Inter MB，null MV，带书签的帧参考
* Inter MB，差分 MV，带书签的帧参考
* Inter MB，MV 1，带书签的帧参考
* Inter MB，MV 2，带书签的帧参考

### 帧头

VP6 的帧头如下图所示，紧跟在大端位封装之后。

|语法|位数|类型|Symantecs|
---|---|---|---|
|frame_mode|1|Enum|0x0 表示帧内|
|qp |6 |无符号 |量化参数有效范围 0..63|
|标记| 1|常数| 0=VP61/62, 1=VP60|
|if (frame_mode == 0) { | 0 | |等于 INTRA_FRAME|
|版本 |5|常数| 6=VP60/61, 7=VP60(电子艺术), 8=VP62|
|版本2 |2|常数 |0=VP60, 3=VP61/62|
|交错 |1|布尔值 |true (1) 表示将使用隔行扫描|
|if (marker==1 or version2==0) {||||
|偏移量 |16 |无符号|辅助缓冲区偏移量（与缓冲区开始相关的字节）|
|}||||
|dim_y |8|未签名|视频的宏块高度|
|dim_x |8|未签名|视频宏块宽度|
|render_y |8 |无符号 |视频的显示高度|
|render_x |8 |无符号 |视频的显示宽度|
|}其他{||||
|if (marker==1 or version2==0) {||||
|offset |16 |无符号 |辅助缓冲区偏移（与缓冲区开始相关的字节）|
|}||||
|}||||

## 参考

* [VP6 维基百科](https://en.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20and%20JavaFX%20media%20files.)


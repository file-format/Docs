{
  "date" : "2021-09-08",
  "keywords" :["mgx 文件","mgx 文件格式","什么是 mgx 文件","文件","mgx 示例","mgx 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解帝国时代 2 扩展重播 MGX 文件格式和可以创建和打开 MGX 文件的 API。",
  "title" :"MGX - 帝国时代 2 扩展重播",
  "linktitle" : "MGX",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## 什么是一 .mgx 文件？

扩展名为 .mgx 的文件是帝国时代 II：征服者游戏的录制文件，可以在帝国时代 II 程序中重播。它包含用户播放的活动的完整记录。它可以在帝国时代 II 程序中加载和播放。重播后，游戏会显示用户为活动计划并玩过的所有事件和场景。

## MGX 文件格式 - 更多信息

MGX 文件的内部文件格式已经制定出来，可作为 [帝国时代 2：征服者-存档游戏文件格式规范](https://github.com/stefan-kolb/aoc-mgx-format)。规范概述了以下部分中的详细信息。

### 结构定义

GPX 文件格式的结构定义被认为是基于 [BinData Ruby Gem 声明](https://github.com/dmendel/bindata/wiki)，它提供了一种读写结构化二进制数据的方法。这让程序员可以指定二进制数据的格式，然后由 BinData 读取和写入。

### MGX 消息传递

MGX 消息传递基于两种类型的消息。

* GAMESTART - 指定游戏开始命令，目前尚未验证
* 聊天 - 描述游戏中的聊天消息。玩家和游戏本身 (Gaia) 都可以发出游戏内消息。

### 游戏动作

有几个 [GAMEPLAY Actions](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions) 已被检索到并且其详细信息可用。

## 参考

* [帝国时代2：征服者-存档游戏文件格式规范](https://github.com/stefan-kolb/aoc-mgx-format)


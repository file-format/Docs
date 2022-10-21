{
  "date" : "2022-02-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 CT 文件格式和可以创建和打开 CT 文件的 API。",
  "title" :"CT - 作弊引擎作弊表文件",
  "linktitle" : "CT",
  "menu" : {
    "docs" : {
    "identifier": "game-ct",
      "parent" : "game"
}
},
  "lastmod" : "2022-02-08"
}

## 什么是一 .ct 文件？

CT 文件是使用 [Cheat Engine](https://www.cheatengine.org/) 软件创建的作弊表文件，用于对基于 Windows 的游戏进行修改以进行作弊。作弊引擎是一个开源作弊引擎，它检查正在执行的游戏并记录其地址位置。此信息及其覆盖写入 CT 文件中，然后由游戏玩家加载以更改游戏属性，例如健康分数、最高分数和剩余生命。

## 作弊引擎 CT 文件格式

CT 文件与地址位置和其他相关信息一起保存，以便在游戏中被黑客入侵。在大多数情况下，文件保存为压缩的 [ZIP](/zh/compression/zip/) 存档，可以使用任何标准解压缩实用程序（如 WinZIP 或 7-Zip）轻松解压缩。

## 如何使用作弊表

1.下载表格并将其复制到Cheat Engine的文件夹
1.运行作弊引擎
1.运行游戏；
1.使用ALT+TAB的组合，通过Cheat Engine选择进程列表中的游戏
1. 如果表格在不同的文件夹中，只需按 Control+O 并将 Cheat Engine 引导到该文件夹。然后选择表（通常是process_name.ct）；
1.一旦表格加载完毕，如果有脚本，检查一下即可。
1. ALT+TAB 回到游戏，玩得开心。

## 参考

* [作弊引擎](https://www.cheatengine.org/)


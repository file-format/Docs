{
  "date" : "2023-01-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 GCF 文件格式和可以创建和打开 GCF 文件的 API。",
  "title" :"GCF 文件 - Nadeo 游戏 GCF 格式",
  "linktitle" : "GCF",
  "menu" : {
    "docs" : {
      "identifier":"game-gcf",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-19"
}

## 什么是 .gcf 文件？

.gcf 文件是 Steam 游戏平台使用的游戏缓存文件。它包含游戏数据，例如纹理、模型和游戏使用的其他文件。这些文件存储在用户的计算机上，用于减少更新或安装游戏时需要下载的数据量。 .gcf 文件还可用于创建游戏安装的备份或在计算机之间传输游戏。

GCF 文件可以由开源 C++ 编程库 [HLLib](https://developer.valvesoftware.com/wiki/HLLib) 读取和写入。

## GCF 文件格式

GCF 文件作为二进制文件保存到光盘。 GCF最初是Grid Cache File的缩写（Steam早期的代号是Grid），后来被当作Game Cache File。 GCF 文件是存储 Steam 游戏的存档文件。所有官方内容都下载为 GCF 文件。 GCF 文件也可以在游戏之间共享。

注意：GCF 是[VPK 文件格式](/zh/game/vpk/) 的前身。
## 参考

* [阀门软件](https://www.valvesoftware.com/en/)
* [GCF 文件格式](https://developer.valvesoftware.com/wiki/GCF)
* [HLLib - 用于读取 GCF 文件的开源 C++ 编程库](https://developer.valvesoftware.com/wiki/HLLib)


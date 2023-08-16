{
  "date" : "2022-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 MCR 文件格式和可以创建和打开 MCR 文件的 API。",
  "title" :"MCR - Minecraft 区域文件格式",
  "linktitle" : "MCR",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2022-12-14"
}

## 什么是 .mcr 文件？

Minecraft MCR 文件格式是 Minecraft 使用的一种数据格式，用于存储 Minecraft 世界的地形块。它基于 NBT（命名二进制标签）格式，该格式由流行的开源游戏引擎 Minecraft Forge 的开发人员开发。 MCR文件类型在一开始就被引入，后来被[MCA文件格式](/zh/game/mca/)所取代。

## MCR 文件格式

MCR 文件格式的结构是一系列命名的二进制标签，每个标签都包含一种特定类型的数据。顶级标签是“级别”标签，其中包含单个游戏级别的所有数据。在 Level 标签中，还有其他几个存储不同类型数据的命名标签，例如存储有关游戏世界信息的“Data”标签，以及存储有关数据的“Entities”和“TileEntities”标签分别是世界中的游戏对象和图块实体。

## MCR 文件格式里面有什么？

在 Minecraft MCR 文件格式中，区域是游戏世界的 32x32 块区域。 MCR 格式将游戏世界划分为多个区域，以便更有效地管理数据并允许更快地加载和保存游戏关卡。每个区域都存储在一个单独的文件中，MCR 文件格式使用坐标系统来识别每个区域在游戏世界中的位置。区域的坐标由区域左下角的块坐标确定。例如，坐标为 (-1,0) 的区域将位于游戏世界原点左侧的一个区域和下方的零个区域。

## MCR 文件格式规范

MCR 文件格式规范是公开可用的。 MCR 格式所基于的 NBT 格式规范可在 Minecraft Forge 网站上找到。此外，[Minecraft Wiki](https://minecraft.fandom.com/wiki/Region_file_format) 也有关于 MCR 文件格式的详细信息，包括它的结构和它支持的各种数据类型。

### MCR 文件中的压缩数据

Minecraft MCR 文件格式支持压缩。 MCR 文件格式基于允许数据以压缩形式存储的 [NBT 格式](https://minecraft.fandom.com/wiki/NBT_format)。这有助于减小 MCR 文件的大小并提高它们的传输和存储效率。这是 MCR 文件格式的一个重要特征，因为它允许玩家与其他人共享大型 Minecraft World 地形数据。

## 参考

* [我的世界世界编辑器](https://www.mcedit.net/)
* [关于我的世界](https://www.minecraft.net/)
* [区域文件格式](https://minecraft.fandom.com/wiki/Region_file_format)
* [NBT格式](https://minecraft.fandom.com/wiki/NBT_format)


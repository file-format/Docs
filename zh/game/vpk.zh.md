{
  "date" : "2023-01-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 Unreal Static Meshes VPK 文件格式和可以创建和打开 VPK 文件的 API。",
  "title" :"VPK 文件 - 虚幻静态网格文件",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "identifier":"game-vpk",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-16"
}

## 什么是一 .vpk 文件？

.vpk 文件是 **Source Engine** 使用的文件格式，这是 Valve Corporation 开发的游戏引擎。 VPK 文件用于打包游戏内容，如模型、纹理和声音，常用于军团要塞 2、Left 4 Dead 和反恐精英：全球攻势等游戏。可以使用各种工具打开和提取文件，例如 GCFScape 和 VPK 工具。

## VPK 文件格式 - 更多信息

VPK 文件作为二进制文件存储到光盘。单个 vpk 文件可以是 VPK 包的一部分，也可以充当独立的原始 VPK 文件。可以存储在 VPK 文件中的信息包括地图、材料、游戏内容和编舞场景。

### 如何创建 VPK 文件？

有多种创建 .vpk 文件的方法，具体取决于可用的工具。

1. `使用 VPK 工具：` 这是一个命令行工具，可用于创建和提取 VPK 文件。可以使用以下命令创建 VPK 文件：
```
"vpk.exe -M <directory> <output_file.vpk>"
```
这将从指定的目录创建一个 VPK 文件，并将其保存为指定的输出文件。

1.`使用 Hammer Editor：`Hammer Editor 是 Source SDK 中包含的一个工具，可用于为使用 Source 引擎的游戏创建和编辑关卡。它还包括通过右键单击“文件系统”选项卡中的文件夹并选择“创建 VPK”来创建 VPK 文件的功能

1.`使用Valve的VPK creator：`这是Valve开发的用于打包和发布游戏内容的工具。该工具可用于创建VPK文件，也是官方提供的VPK文件创建工具。

## 参考

* [阀门软件](https://www.valvesoftware.com/en/)
* [VPK 开发者资源](https://developer.valvesoftware.com/wiki/GCF)


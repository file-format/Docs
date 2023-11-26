{
"date": "2023-09-27",
  "keywords": [
"cfg",
"cfg 文件",
"cfg mame 配置文件",
"什么是 cfg 文件",
"如何打开cfg文件",
"文件",
"cfg 文件扩展名",
"扩大"
],
  "author": {
"display_name": "沙基尔·法伊兹"
},
"draft": "false",
"toc": true,
"title": "CFG 文件格式 - MAME 配置文件",
  "description":"了解 CFG MAME 配置文件格式以及可以创建和打开 CFG 文件的 API。",
"linktitle": "CFG MAME",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-mame",
"parent": "settings"
}
},
"lastmod": "2023-09-27"
}

## 什么是一 .cfg 文件？

CFG 文件是 MAME 街机视频游戏模拟器使用的 XML 键盘配置文件。它是自定义键盘控制和热键以满足玩家喜好的关键组件。这些文件存储确定键盘在玩游戏时如何与模拟器交互的映射和设置。通过编辑此文件,用户可以通过为游戏中的操作分配特定的键盘按键来定制他们的游戏体验,例如硬币插入,开始,移动和各种其他功能。

## MAME配置文件

MAME 代表**多街机模拟器**,是一款软件应用程序,可让您在计算机上模拟和玩街机游戏。 MAME 使用配置文件来自定义其行为和设置。这些配置文件通常位于 MAME 目录中的"cfg"文件夹中。

以下是设置和配置 MAME 时可能遇到的主要配置文件：

1. **mame.ini：** 这是MAME的主要配置文件。它包含适用于所有游戏的全局设置。您可以在 MAME 安装的根目录中找到该文件。

1. **default.cfg：** 该文件存储所有没有自己的配置文件的游戏的默认设置。它用作游戏特定设置的后备。

1. **game-specific.cfg：** 这些文件用于存储各个游戏的设置。它们通常以它们对应的游戏的 ROM 文件命名。例如,如果您有名为"pacman.zip"的游戏,则其配置文件将为"pacman.cfg"。

以下是您可能在 MAME 配置文件中找到的一些常见设置。

1. **rompath:** 指定街机游戏 ROM 所在的目录。

1. **cfg_directory:** 指定存储游戏特定配置文件的目录。

1. **nvram_directory：** 指定存储非易失性 RAM (NVRAM) 文件的目录。 NVRAM 存储高分和其他游戏特定数据。

1. **artwork_directory：** 指定存储图稿文件（例如边框,选取框和传单）的目录。

1. **samplepath:** 指定样本声音文件所在的目录。

1. **cheatpath:** 指定金手指文件所在的目录。

您还可以配置各种其他设置,例如视频和音频选项,控件和输入设备。要修改这些设置,您可以在文本编辑器中打开配置文件并进行必要的更改。

## 玛梅

MAME 代表**"多街机模拟器"**,是一款软件应用程序,旨在模拟和复制老式街机和街机游戏机的硬件。它允许用户在现代计算机和其他兼容设备上玩大量经典街机游戏。 MAME 是一个开源项目,已成为保存和享受街机游戏丰富历史的首选模拟器。

1. **仿真：** MAME 的主要目的是准确仿真街机的硬件,包括中央处理器 (CPU),声音芯片,图形芯片和输入设备。这种精度水平可确保游戏的行为尽可能接近原始街机体验。

1. **兼容性：** MAME 支持广泛的街机游戏 ROM,使其成为最全面的街机模拟器之一。它可以运行各种街机平台的游戏,包括 70 年代,80 年代,90 年代的经典游戏,甚至一些较新的街机游戏。

1. **保存：** MAME 的主要任务之一是保存街机游戏的历史。通过准确模拟街机硬件,MAME 有助于防止经典游戏的丢失,并确保后代能够按照最初的预期体验它们。

1. **前端：** 许多用户利用提供图形界面的前端应用程序通过 MAME 管理和启动游戏。这些前端使浏览 MAME 广泛的游戏库变得更加容易。

## 如何打开 CFG 文件？

打开或引用 CFG 文件的程序

- MAME（免费）（Windows）
- ExtraMAME（试用版）
- 麦克马梅 (MAC)

## 其他 CFG 文件

以下是使用 **.cfg** 文件扩展名的其他文件类型。

**设置**
- [CFG - Celestia 配置文件](/zh/settings/cfg-celestia/)
- [CFG - Citrix 服务器连接文件](/zh/settings/cfg-citrix/)
- [CFG - MAME 配置文件](/zh/settings/cfg-mame/)
- [CFG - LightWave 配置文件](/zh/settings/cfg-lightwave/)

**游戏**
- [CFG - 韦诺标记语言文件](/zh/game/cfg-wesnoth/)
- [CFG - MUGEN 配置文件](/zh/game/cfg-mugen/)
- [CFG - 源引擎配置文件](/zh/game/cfg-sourceengine/)

**系统及杂项**
- [CFG - CFG 文件](/zh/system/cfg/)
- [CFG - Cal3D 模型配置文件](/zh/misc/cfg-cal3d/)

## 参考
* [MAME](https://en.wikipedia.org/wiki/MAME)


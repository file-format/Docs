{
"date": "2023-09-27",
  "keywords": [
"cfg",
"cfg 文件",
"cfg 源引擎配置文件",
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
"title": "CFG 文件格式 - 源引擎配置文件",
  "description":"了解 CFG 源引擎配置文件格式以及可以创建和打开 CFG 文件的 API。",
"linktitle": "CFG Source Engine",
  "menu": {
    "docs": {
      "identifier": "game-cfg-sourceengine",
"parent": "game"
}
},
"lastmod": "2023-09-27"
}

## 什么是一 .cfg 文件？

**Valve 源引擎**上下文中的 CFG 文件（如《半条命 2》等游戏中所示）充当配置文件。这些文件用于通过纯文本命令列表更改各种游戏内设置。这些命令通常每行一个,负责自定义游戏的各个方面。

玩家和服务器管理员有几个选项来应用".cfg"文件中指定的更改：

1. **手动执行**：用户可以手动执行CFG文件中的命令。这意味着他们在游戏的开发者控制台中一一输入每个命令。此方法可以精确控制更改哪些设置以及何时更改。
    





2. **自动执行**：或者,玩家可以选择自动执行。这涉及将".cfg"文件放置在适当的游戏目录中。某些".cfg"文件,例如"autoexec.cfg",会在游戏启动时自动执行。这可确保应用指定的设置,而无需每次游戏启动时手动输入。

## 阀源发动机

Valve Source Engine,通常简称为**Source Engine**,是由 Valve Corporation 开发的高度通用且广泛使用的游戏引擎。它是许多流行视频游戏的基础,并为许多成功的游戏提供了动力。以下是有关 Valve Source Engine 的一些要点：

1. **历史**：Source 引擎于 2004 年随着 Valve 游戏"Counter-Strike 1.6"的发布而首次引入。此后它经历了多次更新和修订,最新版本称为 Source 2.0。
    





2. **著名游戏**：Source 引擎已用于各种广受好评的游戏,包括但不限于：
    





- 《半条命 2》及其剧集
- 《传送门》和《传送门 2》
- "团队要塞2"
- 《Left 4 Dead》和《Left 4 Dead 2》
- 《反恐精英：来源》和《反恐精英：全球攻势》
- 《刀塔 2》
3. **特点**：
    





- **灵活性**：Source Engine 以其灵活性而闻名,允许开发人员创建各种游戏类型,从第一人称射击游戏到益智游戏等等。
- **物理**：它包括强大的物理引擎,可实现逼真的对象交互和环境效果。
- **模组支持**：该引擎具有强大的模组支持,这导致了许多用户生成的内容和游戏模组的创建。
- **多人游戏功能**：Source Engine 已用于开发单人游戏和多人游戏,并为在线游戏提供广泛的网络功能。
    





4. **图形**：多年来,Source Engine 已获得图形更新,以跟上不断发展的硬件功能。它支持先进的渲染技术,如 HDR（高动态范围）照明和动态阴影。

## 如何打开 CFG 文件？

您可以选择使用 Microsoft Visual Studio Code 等文本编辑器或您选择的任何其他文本编辑器打开和修改".cfg"文件。这些文本编辑器提供用户友好的界面,用于查看和编辑".cfg"文件中的纯文本命令,允许您根据需要自定义设置。

打开或引用 CFG 文件的程序包括

- 微软 Visual Studio 代码
- 记事本
- 文本编辑
- 任何文本编辑器

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
* [来源（游戏引擎）](https://en.wikipedia.org/wiki/Source_(game_engine))


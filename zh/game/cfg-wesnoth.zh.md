{
"date": "2023-09-27",
  "keywords": [
"cfg",
"cfg 文件",
"cfg 韦诺标记语言文件",
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
"title": "CFG 文件格式 - 韦诺标记语言文件",
  "description":"了解 CFG Wesnoth 标记语言文件格式以及可创建和打开 CFG 文件的 API。",
"linktitle": "CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth",
"parent": "game"
}
},
"lastmod": "2023-09-27"
}

## 什么是一 .cfg 文件？

CFG 文件也称为**"韦诺标记语言"(WML)**。它是一种自定义标记语言,主要用于"韦诺之战"游戏,这是一款回合制策略游戏。 WML 用于定义和定制游戏的各个方面,包括场景,活动,单位等等。这是模组制作者和开发者为游戏创建内容的一种方式。

它的编写格式类似于 XML 和简单脚本的组合。以下是您可能在 WML 文件中找到的一些常见元素和结构的概述：

1. **标签：** WML 使用标签来定义游戏中的不同元素。标签括在尖括号中。例如：

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    










2. **属性：** 在标签内,您可以定义属性来指定与元素关联的属性或值。在上面的例子中,"type"和"hitpoints"是属性。
    










3. **数组和数组的数组：** 您可以创建数据数组甚至数组数组来定义单位列表,地形类型或其他游戏元素。
    










4. **条件语句：** WML 支持条件语句来控制游戏的流程。例如：

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    










5. **循环：** 您可以使用循环来迭代项目列表或重复执行操作。
    










6. **包括：** 您可以在主 WML 文件中包含其他 WML 文件,以组织和模块化您的内容。
    










7. **事件处理程序：** 您可以定义事件处理程序,以在游戏中发生特定事件时触发操作。
    











以下是定义自定义单位的 WML 文件的简化示例：

```
[unit_type]
    id=my_custom_unit
    name="Custom Unit"
    description="A unit created using WML."
    image="units/my_custom_unit.png"
    hitpoints=30
    movement_type=foot
[/unit_type]
```

## 韦诺之战

《韦诺之战》是一款流行的开源回合制策略游戏。它可用于多种平台,包括 Mac,Windows,Linux 等。该游戏由专门的志愿者社区开发,以其深刻而引人入胜的游戏玩法以及丰富的幻想世界而闻名。

《韦诺之战》的主要特色包括：

1. **奇幻设定：** 游戏设定在一个有着各种种族的奇幻世界,包括人类,精灵,矮人,兽人等等。游戏的传说和故事讲述是其吸引力的一个组成部分。
    










2. **回合制策略：** 游戏玩法是回合制的,玩家花时间在六边形网格上计划和执行他们的动作。它将战术战斗与战略决策结合起来。
    










3. **战役：** 该游戏提供了广泛的单人战役,每个战役都有自己的故事情节,角色和挑战。玩家可以探索不同的叙事和场景。
    










4. **多人游戏：** 《韦诺之战》支持在线多人游戏,让玩家可以在战略战斗中相互较量。多人游戏模式包括合作游戏和竞技比赛。

## 如何打开 CFG 文件？

CFG 文件通常与"韦诺之战"游戏中使用的韦诺标记语言 (WML) 相关,可以使用任何标准文本编辑器轻松编辑。这些文件包含用 WML 编写的人类可读代码,它定义了游戏的各个方面,包括场景,单位和战役。

虽然您可以使用任何文本编辑器来修改 CFG 文件,但一些高级文本编辑器（例如 Emacs 和 Vi）具有可用的 WML 语法突出显示插件。这些插件提供有用的颜色编码和格式,使用户更容易区分 WML 代码中的不同元素和结构。

打开或引用 CFG 文件的程序包括

- 韦诺之战（免费）（Windows,MAC,Linux）
- 微软记事本

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
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)

{
"date": "2023-09-27",
  "keywords": [
"cfg",
"cfg 文件",
"cfg Celestia配置文件",
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
"title": "CFG 文件格式 - Celestia 配置文件",
  "description":"了解 CFG Celestia 配置文件格式以及可以创建和打开 CFG 文件的 API。",
"linktitle": "CFG 塞拉斯蒂娅",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia",
"parent": "settings"
}
},
"lastmod": "2023-09-27"
}

## 什么是一 .cfg 文件？

Celestia 配置文件是 3D 宇宙模拟程序 Celestia 使用的纯文本文件。这些文件对于自定义 Celestia 的行为方式,显示哪些天体以及程序的显示方式至关重要。然而,编辑这些文件需要小心谨慎,因为不当的更改可能会破坏 Celestia 的加载过程,从而使其无法正常运行。

## 塞拉斯蒂娅

Celestia 是免费的开源 3D 天文学模拟软件,允许用户以高度逼真和交互式的方式探索和可视化宇宙。它由 Chris Laurel 开发,于 2000 年代初首次发布。 Celestia 可用于 Windows,macOS 和 Linux 操作系统。

Celestia 的主要功能和方面包括：

- **逼真的 3D 可视化：** Celestia 提供了我们太阳系以及恒星,星系和其他天体的详细且准确的表示。它使用高质量的3D模型和纹理来创造视觉沉浸式体验。

- **广泛的天体数据库：** 该软件附带了已知天体的庞大内置数据库,包括恒星,行星,卫星,小行星,彗星和航天器。用户可以轻松定位和探索这些对象。

- **科学准确性：** 虽然 Celestia 是可视化工具,但它的目标是根据现有的科学数据尽可能准确地表示天体和现象。

## Celestia 使用的文件格式

Celestia 利用各种文件格式来实现 3D 天文学模拟的不同方面。以下是 Celestia 使用的一些关键文件格式：

1. **配置文件（.cel）**
- *描述*：纯文本文件,允许用户自定义 Celestia 的行为,外观和内容。
- *目的*：自定义设置,定义位置和指定天体。

2. **3D模型和网格**
- *格式*：[.3ds](/zh/3d/3ds/),[.obj](/zh/3d/obj/),[.dae](/zh/3d/dae/),.ac
- *描述*：支持用于渲染天体和航天器的 3D 模型文件格式。
- *目的*：在 Celestia 中显示 3D 对象。

3. **纹理文件**
- *格式*：[.jpg](/zh/image/jpeg/),[.png](/zh/image/png/),[.dds](/zh/image/dds/)
- *描述*：这些文件提供天体的表面纹理。
- *目的*：将纹理映射到 3D 模型上以获得逼真的外观。

4. **明星目录和数据文件**
- *格式*：自定义格式,[.csv](/zh/spreadsheet/csv/),[.tsv](/zh/spreadsheet/tsv/)
- *描述*：用于表示恒星和其他天体的数据文件,确保准确的模拟。
- *目的*：准确表示天体。

5. **纹理立方体贴图**
- *描述*：立方体贴图用于模拟遥远天体（如星系）的外观。
- *目的*：用逼真的纹理渲染远处的物体。

6. **脚本文件**
- *描述*：这些文件包含用 Celestia 脚本语言编写的自定义脚本。
- *目的*：使用户能够在 Celestia 的宇宙中创建动态事件和动画。

## 塞拉斯蒂娅配置文件

以下是 Celestia 配置文件的基本概述：

1. **设置您的位置**：您可以使用纬度,经度和海拔高度参数指定您在地球上的位置。这使得 Celestia 能够准确地显示您所在位置的夜空。

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **自定义您的查看选项：** 您可以调整各种查看选项,例如视野,时间设置和渲染首选项。

```
Viewpoint
{
    Location "My Location"
    Follow "Earth"
    Eye [0.0 0.0 0.0]
    Center [0.0 0.0 0.0]
    Up [0.0 1.0 0.0]
    Fov 45
}

Time
{
    Date "2023-09-25T12:00:00.000Z"
    Clock "Now"
}

Rendering
{
    Atmosphere false
    Stars 7
    Planetshine 0.25
}

```

3. **加载天体：** 您可以将恒星,行星,小行星,航天器等天体添加到模拟中。每个对象都在配置文件中定义其属性。

```
Star "Sun"
{
    RA 0
    Dec 0
    Distance 0
    AppMag -26.74
    SpectralType "G2V"
}

Planet "Earth"
{
    Parent "Sol"
    Texture "earth.jpg"
    Radius 6371
    EllipticalOrbit
    {
        Period 365.25
        SemiMajorAxis 149.6e6
        Eccentricity 0.017
        Inclination 0
        AscendingNode 0
        ArgOfPericenter 102.94
        MeanAnomaly 100.464
}
}
```

4. **定义宇宙飞船：** 您可以创建自己的虚构宇宙飞船,也可以通过指定位置,方向和 3D 模型等参数来使用真实的宇宙飞船。

```
Spacecraft "Voyager 1"
{
    Parent "Sol"
    Class "spacecraft"
    Mesh "voyager.3ds"
    Radius 0.01
    EllipticalOrbit
    {
        Period 30700
        SemiMajorAxis 1.08e11
        Eccentricity 0.044
        Inclination 3.4
        AscendingNode 49.0
        ArgOfPericenter 44.0
        MeanAnomaly 35.0
}
}
```

5. **创建脚本：** 您可以使用 Celestia 的自定义脚本语言编写脚本来创建动态事件和动画。

## 如何打开 CFG 文件？

打开或引用 CFG 文件的程序

- Celestia（免费）适用于（Windows,Mac,Linux）

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
* [塞拉斯蒂娅](https://en.wikipedia.org/wiki/Celestia)


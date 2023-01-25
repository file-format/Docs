{
  "date" : "2023-01-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解帝国时代 2 扩展重播 MGX 文件格式和可以创建和打开 MGX 文件的 API。”,
  "title" :"MII 文件 - Wii 虚拟头像文件格式",
  "linktitle" : "MII",
  "menu" : {
    "docs" : {
      "identifier":"game-mii",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-15"
}

## 什么是 .MII 文件？

MII 文件是一种虚拟头像文件格式，用于在任天堂 Wii 游戏机上存储虚拟头像。这些文件包含头像的外观、动作和动画等信息。它们可用于游戏、社交网络应用程序和 Wii 上的其他软件。 MII 文件还包含有关化身的其他特征，例如性别、头发颜色、肤色、面部特征和眼睛类型。

您可以使用 [我的头像编辑器](https://rc24.xyz/goodies/mii/) 打开 MII 文件。

## 信息产业部文件格式

MII 文件格式在 [Wii Brew](https://wiibrew.org/wiki/Mii_data) 上有详细定义。 MII 文件中的字符串以 Unicode 格式 (UTF-16)、big-endian 存储。

### MI块

MII 文件数据以两个块存储在 Wiimote 上。每个块的长度为 750 个字节，带有 2 个字节的 CRC，使其总共为 752 个字节。每个块都以一个 4 字节的值（'RNCD'）开始，这似乎是 MII 文件格式的神奇数字。

## 如何创建 MII 文件？

有几种不同的方法可以为任天堂 Wii 创建头像：

1. `使用 Wii 内置的 Mii 频道：` 该频道允许您使用各种工具创建自定义头像，包括面部特征、体型和服装。创建头像后，您可以将其保存为 Mii 文件，并在 Wii 上的游戏和其他软件中使用。

1.`在 Nintendo 3DS 上使用 Mii Maker 应用程序：`Mii Maker 应用程序允许您使用 Nintendo 3DS 上的触摸屏和摄像头创建自定义头像。创建头像后，您可以将其保存为 Mii 文件并通过无线连接将其传输到 Wii。

1. `使用第三方软件：` 一些开发人员开发了允许您为 Wii 创建自定义头像的软件。该软件通常设计用于计算机，可能需要额外的步骤才能将头像传输到您的 Wii。

1.`使用预制头像：`Wii 上的某些游戏和其他软件可能带有您可以使用的预制头像。

在所有情况下，您都需要有一个任天堂帐户才能在 Wii 上创建和保存您的头像。

## 参考

* [我的头像编辑器](https://rc24.xyz/goodies/mii/)
* [Wii Brew](https://wiibrew.org/wiki/Mii_data)


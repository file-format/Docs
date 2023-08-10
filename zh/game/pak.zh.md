{
  "date" : "2021-10-20",
  "keywords" :[".pak","文件格式","什么是 pak 文件","文件","pak 示例","视频游戏包文件","扩展名"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 .pak 文件和可以创建和打开 PAK 文件的 API。",
  "title" :"PAK 文件格式 - 视频游戏包文件",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## 什么是一 .pak 文件？

PAK 文件是由不同的视频游戏创建的用于存档游戏数据的包文件。本质上，它是一种游戏文件格式。这可以包括多个游戏元素，例如图形、纹理、声音、对象以及其他游戏数据。压缩包大多保存为 .zip 文件，可以用 WinZip 和 WinRAR 等流行的解压软件解压。使用 PAK 文件的视频游戏示例包括 Quake、Hexen、Crysis 和 Half-Life。

## PAK 文件格式 - 更多信息

在大多数情况下，PAK 文件以 [ZIP 文件格式](/zh/compression/zip/) 保存。但是不同的应用程序可能使用不同的文件格式来存储这些文件。


## 如何打开 .pak 文件？

您可以使用 [PakExplorer](https://www.quaketerminus.com/tools.shtml) 和 [SpriteExplorer](http://www.slackiller.com/hlprograms.htm) 等应用程序打开 PAK 文件。

**------------------------------------------------ -------------------------------------------------- ----------------------**

## PAK 文件格式 - Simutrans 目标文件

带有 .pak 扩展名的文件是 [Simutrans](https://www.simutrans.com/en/) 交通模拟游戏文件格式。它包含模拟中使用的对象，例如用户制作的图形和数据内容。它可以有几个不同的对象，例如游戏车辆、建筑物、地形等。PAK 文件是使用 MakeObject 生成的，MakeObject 是一个编译 .dat 文件和 .png 图片以创建这些模拟对象的实用程序。 Simutrans 让玩家通过构建和管理陆路乘客、邮件和货物的运输系统来运行成功的运输系统

## 如何创建 PAK 文件？

Simutrans 列出了在 Windows 和 Linux 操作系统上创建 PAK 文件的示例。

### Windows 操作系统

```
simutrans_src
   makeobj.exe
   haus_01
        haus_01.dat
        haus_01.png
        pak.bat
   auto_03
        auto_03.dat
        auto_03.png
        pak.bat
   triebzug_01
        triebzug_vorn.dat
        triebzug_mitte.dat
        triebzug_hinten.dat
        triebzug_01.png
        pak.bat
```
### Linux BE/操作系统

```
simutrans_src
   makeobj
   haus_01
        haus_01.dat
        haus_01.png
        pak
   auto_03
        auto_03.dat
        auto_03.png
        pak
   triebzug_01
        triebzug_v.dat
        triebzug_m.dat
        triebzug_h.dat
        triebzug_01.png
        pak
```

## 参考

* [Simutrans](https://en.wikipedia.org/wiki/Simutrans)

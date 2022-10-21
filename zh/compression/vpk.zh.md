{
  "date" : "2022-03-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VPK 文件 - PlayStation Vita 应用程序包文件格式",
  "description":"了解 VPK 文件格式和可以创建和打开 VPK 文件的 API。",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-01"
}

## 什么是一 .vpk 文件？

带有 .vpk 扩展名的文件是一个压缩存档包文件，用于在 Sony PlayStation Vita 游戏机上安装第三方应用程序。这些文件只能安装在 HENkaku 的越狱 Vita PlayStation 上，使 PS Vita 和 PSTV 能够使用自定义的用户创建内容。 VPK 存档文件包含构成游戏的所有内容，包括 [PNG](/zh/image/png/) 文件等图像、[.bin](/zh/disc-and-media/bin/) 等设置文件，以及[XML](/zh/web/xml/) 文件格式的任何配置。

## VPK 文件格式

VPK 文件作为标准压缩 [ZIP](/zh/compression/zip/) 档案保存到光盘。这些可能包含多个文件夹和其他相关文件，供要安装在 Vita 游戏控制台上的第三方应用程序使用。要查看 VPK 包文件的内容，请将其扩展名从 .vpu 重命名为 .zip，然后使用标准解压缩实用程序（如 WinZip 或 WinRAR）提取内容。

Valvesoftware 有关于 [VPK 文件格式](https://developer.valvesoftware.com/wiki/VPK_File_Format) 的详细信息，可以从开发人员的角度参考。

## 如何安装 VPK 文件？

VPK 文件可以从命令行实用程序 VPK.exe 安装。在 Windows 操作系统上，文件可以放在 vpk.exe 文件上，该文件返回一个包含所有打包文件的 \*.vpk。或者，可以如下使用命令行工具。

### 创建 VPK 并添加文件

```
vpk <dirname>
```

### 提取 VPK 文件

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## VPK 查看器

* [VRF VPK 查看器](https://github.com/SteamDatabase/ValveResourceFormat)

## 参考

* [VPK 文件格式](https://developer.valvesoftware.com/wiki/VPK_File_Format)
* [VPK 文件](https://developer.valvesoftware.com/wiki/VPK)


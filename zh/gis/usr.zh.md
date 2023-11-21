{
"date": "2023-08-03",
  "keywords": [
"我们",
"usr 文件",
"什么是 usr 文件",
"如何打开 usr 文件",
"文件",
"usr 文件扩展名",
"扩大"
],
  "author": {
"display_name": "沙基尔·法伊兹"
},
"draft": "false",
"toc": true,
"title": "USR 文件格式 - Lowrance GPS 数据文件",
  "description":"了解 USR 格式以及可以创建和打开 USR 文件的 API。",
"linktitle": "USR",
  "menu": {
    "docs": {
      "identifier": "gis-usr",
"parent": "GIS"
}
},
"lastmod": "2023-08-03"
}

## 什么是 .usr 文件？

".usr"文件扩展名也与 Lowrance GPS 设备相关。特别是,它用于以 Lowrance GPS 设备使用的"用户数据格式"（USR 格式）格式存储 GPS 数据。

使用 Lowrance GPS 装置时,您可以将航点,轨迹和路线保存为".usr"文件。这些文件通常包含纬度,经度,海拔,时间戳以及与您的 GPS 活动相关的其他数据等信息。

以下是 Lowrance GPS 设备中 .usr 文件的一些常见用法：

- **航点：** 航点是 GPS 上标记的特定位置,例如地标,最喜欢的钓鱼点或兴趣点。您可以将这些位置另存为 .usr 文件,并且可以导入,导出它们或与其他 Lowrance GPS 用户共享。

- **轨迹：** 轨迹代表您的 GPS 运动记录的路径。您可以将轨迹日志保存为 .usr 文件,以便您稍后查看和分析您的路线或与其他人共享。

- **路线：** 路线是您可以创建并保存在 GPS 设备上的预定义路径。这些路由还可以保存为 .usr 文件以供将来使用或共享。

要管理 Lowrance GPS 设备上的 .usr 文件,通常使用 Lowrance 的"Insight Planner"或"Lowrance GPS Utility"等软件来导入,导出和操作 GPS 数据。

## USR 文件格式 - 更多信息

在 Lowrance iFinder GPS 设备中,会创建 .usr 文件并将其保存在插入设备的 MultiMediaCard (MMC) 存储卡上。这些文件包含用户数据,例如航路点,轨迹和路线。

要将 .usr 文件从 MMC 传输到计算机,您可以按照以下步骤操作：

- **卸下 MMC：** 小心地从 Lowrance iFinder GPS 设备上卸下多媒体卡 (MMC)。

- **将 MMC 插入计算机：** 使用适当的 MMC 读卡器将存储卡插入计算机的读卡器插槽中。

- **找到 .usr 文件：** 一旦 MMC 被您的计算机识别,您应该能够访问存储在其中的文件。查找 .usr 文件,其中包含您的 GPS 数据。

- **使用 GPSBabel 进行转换：** 要将 .usr 文件转换为另一种 GPS 格式,您可以使用 GPSBabel,这是一个免费的开源工具,用于处理各种 GPS 文件格式。 GPSBabel 支持多种输入和输出格式,允许您将 .usr 文件转换为与其他 GPS 软件或设备兼容的格式。

您可以从官方网站（http://www.gpsbabel.org/）下载GPSBabel并将其安装到您的计算机上。安装后,您可以使用该软件的命令行界面或图形用户界面（如果可用）来执行转换。

例如,如果要将 .usr 文件转换为 GPX 格式,可以使用如下命令：

```
gpsbabel -i lowranceusr -f input.usr -o gpx -F output.gpx
```

上面的命令指示 GPSBabel 读取 Lowrance USR 格式的输入文件"input.usr"并写入 GPX 格式的输出文件"output.gpx"。

- **导入/使用转换后的文件：** 转换后,您将获得新格式（例如 GPX）的 GPS 数据,您可以将其与支持该格式的其他 GPS 软件或设备一起使用。

## 如何打开 USR 文件？

打开或引用 USR 文件的程序包括

- GPSBabel（Windows）
- GPSBabel (Mac)
- GPSBabel (Linux)

## 参考
* [洛伦斯电子](https://en.wikipedia.org/wiki/Lowrance_Electronics)


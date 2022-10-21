{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SP3 - NGS SP3 文件",
  "description":"了解可以创建和打开 SP3 文件的 SP3 文件格式和 API。",
  "linktitle" : "SP3",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## 什么是 SP3 文件？

扩展名为 .sp3 的文件是国家大地测量 (NGS) 轨道格式，用于存储轨道信息。这是 NGS 的 SP1 和 SP2 格式的扩展，包括与轨道同时计算的卫星时钟校正信息。它主要基于位置和时钟，不包括速度。该格式于 1989 年在 Remondi 提出并于 1991 年被采用。除了卫星时钟校正信息外，它还包括轨道精度指数、注释行、GPS 周和与第一个纪元相关的周秒数等信息。 SP3 文件可以用 Wolfram Research Mathematica 打开。

## SP3 文件格式 - 更多信息

SP3 文件以 ASCII 文件格式保存到光盘中，其内容可以在任何文本编辑器中打开以供查看。 SP3 文件的结构如下图所示。

{{< figure src="../sp3-file-format.png" title="" >}}

## 参考

* [扩展标准产品 3 轨道格式 (SP3-c)](http://epncb.oma.be/ftp/data/format/sp3c.txt#:~:text=The%20SP3%20format%20is%20similar ,a%20more%20flexible%20header%20structure)
* [扩展国家大地测量标准 GPS 轨道格式](https://beta.ngs.noaa.gov/PUBS_LIB/Extending_the_NGS_Standard_GPS_Orbit_Formats_TR_NOS133_NGS46.pdf)


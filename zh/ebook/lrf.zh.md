{
  "date" : "2019-12-12",
  "keywords" :["LRF","文件","扩展名","格式","电子书","电子书"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 LRF 文件格式和可以创建和打开 LRF 文件的 API。",
  "title" :"LRF 文件格式 - 索尼便携式阅读器文件",
  "linktitle" : "LRF",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## 什么是一 .lrf 文件？

扩展名为 .lrf 的文件是宽带电子书 (BBeB) 文件，其中包含 Sony BBeB 的数据，包括文本、图像和分页数据。该文件以压缩二进制格式保存，其中包含标题、指定数量的对象和对象索引。 LRF 和 LRX 文件包含两种可用的 BBeB 书籍格式。 LRF 文件未加密，可以从 [LRX](/zh/ebook/lrf/) 文件编译。 LRF 文件可以从其他几种文件类型转换，包括 PDF 和 HTML。如果您的计算机无法打开 LRF 文件，那么您可能没有安装软件来打开或编辑 LRF 文件。可以打开 LRF 文件的程序有适用于 Windows 的 Calibre、BookDesigner、Makelrf 和 Canon Book Creator、适用于 Linux 的 Calibre、Calibre 和适用于 Macintosh 的 Sony Reader。

## 历史简介

LRF 文件类型首先由 [inXile Entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment) 与 Line Rider 相关联。 Line Rider 是一款互联网物理玩具，由斯洛文尼亚大学生 Boštjan Čadež 于 2006 年 9 月发明。索尼品牌的 eBook 电子阅读器（例如 Sony PRS-500 阅读器和 Sony Librie）使用 LRF 文件扩展名来存储文档和文本。这种专有文件类型以及相关的 LRS 和 LRX 文件现已过时。这三种文件类型构成了 BroadBand 电子书 (BBeB)，该电子书于 2010 年停产，当时索尼开始以 EPUB 格式销售其电子书。

## LRF 文件格式

LRF 文件格式的详细规范可在 [web archive](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat) 获得。 LRF 文件包括：
* 一个标题
* 多个对象
* 对象索引。

所有这些值都按 Intel（LSB 优先）顺序排列。

### LRF 标头

|偏移量（十六进制）|大小（字节）|名称/含义|示例值|
---|---|---|---|
|0 |8| LRF 签名| 4C 00 52 00 46 00 00 00 = Unicode 中的“LRF"|
|8 |2|版本？|大多数文件中为 999|
|A |2| “伪加密"|密钥字节 48|
|0C |4|根对象ID| 0x0044|
|10 |8|对象数 |342|
|18 |8|对象索引偏移| 0x00093440|
|20 |4|未知| 0|
|24 |1|旗帜| （16 - 从后到前，1 = 从前到后）16|
|25 |1|未知|（填充？）0|
|26 |2|未知| 1600|
|28 |2|未知| （填充？） 0|
|2A |2|身高？| 600|
|2C |2|宽度？| 800|
|2E |1|未知| 24|
|2F |1|未知|（填充？）0|
|30 |0x14|未知|零|
|44 |4|仅 PlaneStream (0x1E) 对象的对象 ID| 0x0042|
|48 |4|未知 |0x1536|
|4C |2| XMLCompSize| 0x035C|


## 参考

* [LRF 文件格式](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)
* [BBeB - 维基百科提供](https://en.wikipedia.org/wiki/BBeB)


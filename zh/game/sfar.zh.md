{
  "date" : "2021-10-20",
  "keywords" :["sfar 文件","sfar 文件格式","什么是 sfar 文件","文件","sfar 示例","质量效应 3 DLC 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解质量效应 3 SFAR 文件格式和可以创建和打开 SFAR 文件的 API。",
  "title" :"SFAR - 质量效应 3 DLC 文件",
  "linktitle" : "SFAR",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## 什么是一 .sfar 文件？

具有 .sfar 扩展名的文件是质量效应 3 用于将其 DLC（可下载内容）存储在压缩的专有存档中的游戏数据文件。质量效应 3 是由领先的游戏开发公司 Electronic Arts 创建的游戏。存储在 SFAR 文件中的 DLC 内容用于通过附加内容和功能扩展游戏。

## SFAR 文件格式 - 更多信息

SFAR 文件以二进制文件格式存储/保存为压缩存档文件。它们使用 LZX 和 LZMA 压缩算法来压缩内容。可以使用 ME3 Explorer 随附的 DLC 编辑器打开 SFAR 文件。除了SFAR，DLC Editor还可以解压其他游戏文件如[PCC](/zh/game/pcc/)。

## SFAR 文件格式规范

SFAR 文件分为以下四个主要块。

### SFAR 标头

SFF Header 包含有关组成文件的各种块的信息。

### SFAR 文件表

SFAR 文件表包含一个文件条目列表，其中每个条目长 30 个字节。

### 块大小表

Block-Size 包含多个条目，其中每个条目有 2 个字节长。该值指定与文件表中的条目对应的块大小。

### 块

SFAR 文件中的块块包含 SFAR 文件中的数据。

## 参考

* [DLC SFAR 文件格式 - 研究](https://www.tapatalk.com/groups/me3explorer/current-research-dlc-sfar-fileformat-t629.html)


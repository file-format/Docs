{
  "date" : "2021-09-08",
  "keywords" :["pcc 文件","pcc 文件格式","什么是 pcc 文件","文件","pcc 示例","pcc 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解质量效应 PCC 文件格式和可以创建和打开 PCC 文件的 API。",
  "title" :"PCC - 质量效应包文件",
  "linktitle" : "PCC",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## 什么是一 .pcc 文件？

.pcc 文件是一个 [质量效应游戏](https://www.ea.com/games/mass-effect/mass-effect-3) 文件，其中包含用于修改游戏内容的游戏数据，例如模型、纹理和房间。质量效应 2 和 3 是第一款基于 Unreal Engine 3 游戏引擎的射击游戏。该游戏最初由 [Bioware](https://www.bioware.com/about/) 开发，他们将大部分游戏资源保存在其专有的 PCC 文件格式中。 Bioware 被全球领先的互动娱乐出版商 Electronic Arts 收购。

## PCC 文件格式 - 更多信息

PCC 文件包含有助于整个文件组织的压缩和/或未压缩结构。

### 压缩的 PCC 结构

压缩的 PCC 文件由分割成块的表和数据组成。每个块包含可变数量的压缩块。

* `Chunks Header` - 一个 16 字节的公共标头，包含有关块的信息。
* `Chunk Header` - 一个 16 字节的标头，包含有关块形式中包含的原始压缩数据的信息。

### 未压缩的 PCC 结构

未压缩的 PCC 文件分为以下五个部分。

* `Header` - 包含有关 PCC 文件结构的基本信息。
* `Name Table` - 包含在包中找到的名称，包括导入类、导出和导出属性。
* `Import Table` - 包含 PCC 导入的所有类和对象。
* `导出表` - 包含存储在包中的所有对象。每个出口的大小可能不同。

## 参考

* [Me3Explorer - PCC 文件格式](https://me3explorer.fandom.com/wiki/PCC_File_Format)
* [质量效应游戏](https://www.ea.com/games/mass-effect/mass-effect-3)
* [Bioware](https://www.bioware.com/about/)


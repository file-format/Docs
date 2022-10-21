{
  "date" : "2021-04-08",
  "keywords" :["lzma 文件","lzma 文件格式","什么是 lzma 文件","文件","lzma 示例","lzma 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZMA - LZMA 压缩文件格式",
  "description":"什么是 LZMA 文件和可以创建和打开 LZMA 文件的 API。",
  "linktitle" : "LZMA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-18"
}

## 什么是一 .lzma 文件？

扩展名为 .lzma 的文件是使用 LZMA（Lempel-Ziv-Markov 链算法）压缩方法创建的压缩存档文件。这些主要在 Unix 操作系统上找到/使用，并且类似于其他压缩算法，例如 [ZIP](/zh/compression/zip/)，用于最小化文件大小。 LZMA 是一种遗留文件格式，正在或已经被 .xz 格式取代。 .lzma 格式的 MIME 类型是 \`application/x-lzma'。此文件格式由 Igor Pavlov 设计用于 LZMA SDK。

## LZMA 文件格式

LZMA 文件由两个主要部分组成：

1.页眉
1. 压缩数据


### LZMA 标头

LZMA 文件有一个 13 字节的标头，后跟 LZMA 压缩数据。 LZMA 标头包括：

* 特性
* 字典大小
* 未压缩大小

#### LZMA 标头属性

属性字段包含三个属性。括号中给出了缩写，后跟属性的值范围。该领域包括

1) 文字上下文位的数量 (lc, [0, 8])；
2) 文字位置位数 (lp, [0, 4])；和
3) 位置位数(pb, [0, 4])。

#### LZMA 字典大小

这存储为无符号 32 位小端整数，其值范围为 2^n 和 2^n + 2^(n-1)。 LZMA Utils 可以解压缩任何字典大小的文件。

#### 未压缩大小
未压缩大小存储为无符号 64 位小端整数。特殊值 0xFFFF_FFFF_FFFF_FFFF 表示 Uncompressed Size 未知。当且仅当 Uncompressed Size 未知时，该值才由 End of Payload Marker (\*) 表示。

## 参考

* [LZMA 文件格式](https://svn.python.org/projects/external/xz-5.0.3/doc/lzma-file-format.txt)
* [Lempel-Ziv-Markov链算法](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)


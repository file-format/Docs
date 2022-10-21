{
  "date" : "2019-12-09",
  "keywords" :["zl 文件","zl 文件格式","什么是 zl 文件","文件","zl 示例","zl 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZL - ZLIP 压缩文件格式",
  "description":"了解 ZL 文件格式和可以创建和打开 ZL 文件的 API。",
  "linktitle" : "ZL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-14"
}

## 什么是一 .zl 文件？

带有 .zl 扩展名的文件是一种 ZLIP 压缩文件格式，它使用 DEFLATE 压缩算法的变体来压缩文件。它独立于 CPU 类型、操作系统、文件系统和字符集，因此可用于信息交换。 [IETF 站点](https://tools.ietf.org/html/rfc1950) 上提供了 ZLIP 压缩的技术规范，可以从开发人员的角度参考。

## ZL 文件格式

zlib 流具有以下结构：

* `CMF (Compression Method and flags)` - 根据压缩方法，该字节分为 4 位压缩方法和 4 位信息字段。
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
* `CM（压缩方法）` - 它标识文件中使用的压缩方法。其取值及对应的压缩方式如下。

| CM价值|压缩|
|---|---|
|CM = 8|DEFLATE 窗口大小高达 32K|
|CM = 15|保留|

* `CINFO（压缩信息）` - 对于 CM = 8，CINFO 是 LZ77 窗口大小的以 2 为底的对数减八（CINFO=7 表示 32K 窗口大小）。

* `FLG (FLaGs)` - 这个标志字节被划分如下：
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## 参考 ＃＃

* [Zlib 文件格式规范](https://tools.ietf.org/html/rfc1950)


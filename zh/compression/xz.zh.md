{
  "date" : "2022-01-23",
  "keywords" :["xz 文件","文件格式","什么是 xz 文件","文件","xz 示例","xz 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XZ 文件 - XZ 压缩档案",
  "description":"了解 XZ 文件格式和可以创建和打开 XZ 文件的 API。",
  "linktitle" : "XZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-01-23"
}

## 什么是一 .xz 文件？

XZ 是一种使用 LZMA2 压缩算法的压缩文件格式。它被设计为流行的 gzip 和 bzip2 格式的替代品，并且与这些旧标准相比具有许多优势。 XZ 文件在许多平台上得到很好的支持，并且可以快速轻松地解压缩。虽然它们不像 [ZIP](/zh/compression/zip/) 或 [RAR](/zh/compression/rar/) 文件那么常见，但 XZ 存档可用于存储大量数据而不会牺牲压缩质量。如果需要压缩或解压大文件，XZ 文件扩展名值得考虑。

## XZ 文件格式

XZ 文件生成并作为二进制文件保存到光盘。它使用LZMA算法压缩数据，可以达到高达50%的压缩率。 XZ 文件通常用于软件分发和备份存档。它们可以使用 XZ 实用程序解压缩，该实用程序包含在大多数 Linux 发行版中。

## 在 Linux/Unix 上解压 XZ 文件

为了解压 XZ 文件，首先安装 `xz-utils` 包：
```
$ sudo apt-get install xz-utils
```

使用 `unxz` 命令提取 .xz 文件：
```
$ unxz compressed_xz_file.xz
```

或与 XZ 的 --decompress 选项一起使用：
```
$ xz --decompress compressed_xz_file.xz
```

## 参考

* [XZ Utils](https://en.wikipedia.org/wiki/XZ_Utils)


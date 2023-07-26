{
  "date" : "2022-03-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGZ 文件 - Gzipped Tar 文件",
  "description":"了解 TGZ 文件格式和可以创建和打开 TGZ 文件的 API。",
  "linktitle" : "TGZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-02"
}

## 什么是一 .tgz 文件？

扩展名为 .tgz 的文件是 TAR 存档文件，由多个文件和文件夹组成，已使用 Gnu Zip (gzip) 压缩软件进行压缩。 [TAR](/zh/compression/tar/) 文件通常将多个文件组合成一个文件，以便通过 Internet 进行备份或分发。它是解压缩文件，直到它使用 gzip 软件压缩，然后它成为 TGZ 文件。 TGZ 文件是压缩文件，占用的磁盘空间更少，并且可以通过电子邮件使用 Internet 轻松传输。一些可以打开 TGZ 文件的应用程序包括 WinZip、Apple Archive Utility、7-Zip 和 WinRAR。 TGZ 文件主要用于 UNIX 和 Linux 系统。

## TGZ 文件格式

TGZ 文件使用 [GZ](/zh/compression/gz/) 压缩算法保存为压缩的二进制文件。

## 如何在 Linux 上解压 .tgz 文件

在 Linux/Unix 操作系统上，可以使用以下命令从命令行解压 TGZ 文件。

```
tar zxvf tgzCompressedFile.tgz
```

上述命令解压缩压缩的 TGZ 文件并将其文件解压缩到 TAR 存档到磁盘。
## 参考 ＃＃

* [TGS](https://core.telegram.org/stickers#animated-stickers)
* [gzip - 维基百科](https://en.wikipedia.org/wiki/Gzip)


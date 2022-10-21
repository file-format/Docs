{
  "date" : "2021-04-08",
  "keywords" :["dar 文件","dar 文件格式","什么是 dar 文件","文件","dar 示例","dar 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DAR - 磁盘归档文件格式",
  "description":"了解 DAR 文件格式和可以创建和打开 DAR 文件的 API。",
  "linktitle" : "DAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## 什么是一 .dar 文件？

带有 .dar 扩展名的文件是使用 DAR 磁盘存档创建的压缩存档。它可以为整个磁盘或一组文件创建备份/存档。创建它是为了替换 UNIX 操作系统上的 [TAR](/zh/compression/tar/) 文件格式，并且可以创建为大量文件的拆分存档文件。 DAR 存档支持从系统中删除与存档中的主要文件链接的文件的选项。它提供差异、增量和减量备份的能力使其优于 TAR 文件。

## DAR 文件格式

DAR 文件是压缩档案，可以使用任何文件压缩，例如 [gzip](/zh/compression/gz/)、[bzip2](/zh/compression/bz2/)、lzo、xz 或 lzma。 DAR 文件的确切文件格式取决于用于压缩存档内容的格式类型。它还允许可选的 Blowfish、Twofish、AES、Serpent、Camellia 加密以及公钥加密和签名 (OpenPGP)。

### DAR 功能

DAR 文件格式的一些特点如下。

* 处理任何类型的 inode（目录、普通文件、符号链接、特殊设备、命名管道、套接字、门......）
* 处理硬链接的 inode（硬链接的普通文件、字符设备、块设备、硬链接的符号链接）
* 处理稀疏文件
*照顾Linux文件扩展属性，
* 处理 Linux 文件 ACL
* 处理 Mac OS X 文件分叉
* 处理一些文件系统特定的属性，如 HFS+ 文件系统的 Birthdate 和 ext2/3/4 文件系统的不可变、数据日志、安全删除、无尾合并、不可删除、noatime 属性。
* 使用 gzip、bzip2、lzo、xz 或 lzma 对每个文件进行压缩（而不是压缩整个存档）。个人可以根据文件名后缀选择不压缩已压缩的文件。
*从档案中的任何地方快速提取文件
* 通过保存档案中的文件目录快速列出档案内容
*实时文件系统备份：检测文件在读取备份时何时被修改，并可以重试将其保存到给定的最大重试次数
* 为每个切片即时生成哈希文件（MD5、SHA1 或 SHA-512），生成的文件与 md5sum 或 sha1sum 兼容，以便能够快速检查每个切片的完整性
* 独立于文件系统：它可用于将系统恢复到不同大小的分区和/或具有不同文件系统的分区[5]

## 参考

* [DAR](http://dar.linux.free.fr/)
* [DAR 磁盘存档器](https://en.wikipedia.org/wiki/Dar_(disk_archiver))


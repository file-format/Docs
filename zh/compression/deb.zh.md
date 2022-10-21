{
  "date" : "2021-04-08",
  "keywords" :["deb 文件","deb 文件格式","什么是 deb 文件","文件","deb 示例","deb 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DEB - Bzip 压缩焦油存档",
  "description":"了解 DEB 文件格式和可以创建和打开 DEB 文件的 API。",
  "linktitle" : "DEB",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## 什么是一 .deb 文件？

带有 .deb 扩展名的文件是一种 Debian 二进制包文件格式，可用于在 Linux 操作系统上分发软件包。它由两个 [TAR](/zh/compression/tar/) 归档文件组成。 DPKG 提供了读取和安装 DEB 包的机制。可以使用 APT 包软件管理界面安装 DEB 包。 DEB 文件的 Internet 媒体类型为 `application/vnd.debian.binary-package`。

## DEB 文件格式

一个 DEB 文件由两个 [TAR](/zh/compression/tar/) 归档文件组成。一个存档包含控制信息，另一个包含可安装数据。

### 包组织

DEB 文件是一个 **ar** 存档文件，具有 `!<arch> `。从 Debian 0.93 开始，DEB 文件的归档机制包含三个按特定顺序排列的文件。

1. `Debian Binary` - 注定会有一系列的行，用换行符分隔。目前，只有一行描述了版本号。当前版本号为 2.0。
1. `Control Archive` - 它包含一个 control.tar 存档，其中包含维护者脚本和有关包的元信息，例如包名称、版本、依赖项和维护者。
1. `Data Archive` - 它是一个名为 data.tar 的 tar 存档，包含实际可安装的媒体文件。存档可以使用 gz、bz2、lzma 或 xz 压缩，数据存档的文件扩展名会相应更改。

### 控制存档

控制档案可以包括如下内容。

* `control` - 它包含对包的简要描述以及其他信息，例如它的依赖关系。
* `md5sums` - 它包含包中所有文件的 MD5 校验和，以检测损坏或不完整的文件。
* `conffiles` - 它列出了应该被视为配置文件的包文件。除非指定，否则在更新期间不会覆盖配置文件。
* `preinst`、postinst、prerm 和 postrm - 在安装或删除软件包之前或之后执行的可选脚本
* `config` 是一个支持 debconf 配置机制的可选脚本。
* `shlibs` - 它是共享库依赖项的列表。

## 参考

* [DEB - 维基百科](https://en.wikipedia.org/wiki/Deb_(file_format))
* [Debian 二进制包格式](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)


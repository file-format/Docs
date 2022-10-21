{
  "date" : "2021-04-08",
  "keywords" :["rpm 文件","rpm 文件格式","什么是 rpm 文件","文件","rpm 示例","rpm 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPM - 红帽软件包管理器文件",
  "description":"了解 RPM 文件格式和可以创建和打开 RPM 文件的 API。",
  "linktitle" : "RPM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## 什么是 .RPM 文件？

带有 .rpm 扩展名的文件是 Red Hat Linux 操作系统软件包，用于在 Linux 系统上安装程序。 Red Hat Package Manager 使用 RPM 文件格式，是免费的开源软件包管理系统。虽然 RPM 文件可以直接用于安装程序，但可以使用名为 Alien 的 Debian 程序将这些文件转换为其他包格式，例如 [DEB](/zh/compression/deb/)。

## RPM 文件格式

RPM 文件是可以包含一组文件的二进制文件。大多数时候，RPM 文件是“二进制 RPM"，它们是软件的编译可执行文件。 RPM 文件可以包含可用于从源代码构建包的源 RPM (SRPM)。 RPM 文件格式由四个部分组成。

* Lead - 它将文件标识为 RPM 文件
* 签名 - 可用于确保完整性和/或真实性
* Header - 包含元数据，包括包名称、版本、架构、文件列表等。
* 文件存档 - 也称为有效负载，通常为 cpio 格式，使用 [GZIP](/zh/compression/gz/) 压缩

## 参考

* [RPM - 维基百科](https://rpm.org)
* [RPM 文档](https://rpm.org/documentation.html)


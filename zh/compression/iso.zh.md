{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ISO - 磁盘映像文件格式",
  "description":"什么是 ISO 文件和可以创建和打开 ISO 文件的 API。",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
      "identifier": "compression-iso",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## 什么是 ISO 文件？

带有 .iso 扩展名的文件是未压缩的存档磁盘映像文件，它代表光盘（如 CD 或 DVD）上的全部数据内容。基于 [ISO-9660](https://www.iso.org/standard/17505.html) 标准，ISO 映像文件格式包含光盘数据以及存储在其中的文件系统信息。 ISO 文件包含内容的精确副本的能力使其成为创建 CD/DVD 副本的完美文件类型，并且主要用于存储可引导数据以进行安装。大多数时候，ISO 文件被刻录到 USB/CD/DVD 作为可引导内容，用于引导机器进行安装。 ISO 文件的 MIME 类型为 application/x-iso9660-image。

## ISO 文件格式

ISO 文件格式与其他容器文件文件格式不同，尽管它归档了数据的指定内容。存档被创建为具有内容和文件系统信息的确切结构的二进制文件。 ISO 文件格式由 [ISO-9660](https://en.wikipedia.org/wiki/ISO_9660) 描述如下。

### ISO 文件的顶级结构

文件的整体结构包括：

* `System Area` - 32,768 字节，ISO_9660 未使用
* `Data Area` - 由卷描述符集和路径表、目录和文件组成

### 卷描述符集

数据区以卷描述符集开始，一组一个或多个卷描述符以卷描述符集终止符终止。这些共同充当数据区域的标题，描述其内容（类似于 FAT、HPFS 和 NTFS 格式化磁盘使用的 BIOS 参数块）。

卷描述符集如下所示。

|卷描述符集|
---|
|卷描述符 #1|
|...|
|卷描述符#N|
|卷描述符集终止符|

#### 卷描述符

每个卷描述符的大小为 2048 字节，并具有以下结构：

|零件 |类型 |标识符 |版本 |数据|
---|---|---|---|---|
|大小 |1 字节 |5 字节（始终为 'CD001'）|1 字节（始终为 0x01）|2,041 字节|

## 参考

* [光盘映像 - 维基百科](https://en.wikipedia.org/wiki/Optical_disc_image)
* [文件签名](https://www.garykessler.net/library/file_sigs.html)
* [ISO 9660 - 维基百科](https://en.wikipedia.org/wiki/ISO_9660)


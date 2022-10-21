{
  "date" : "2021-04-21",
  "keywords" :["豌豆文件","豌豆文件格式","什么是豌豆文件","文件","豌豆示例","豌豆文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEA - PeaZip 存档文件格式",
  "description":"了解 PEA 文件格式和可以创建和打开 PEA 文件的 API。",
  "linktitle" : "PEA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-21"
}

## 什么是一 .pea 文件？

扩展名为 .pea 的文件是 Pack、Encrypt 和 Authenticate 的首字母缩写词，是使用 [PeaZip](https://peazip.github.io/) 归档软件应用程序创建的 [zip](/zh/compression/zip/) 归档文件。它具有压缩和多卷输出的特点，并通过身份验证加密和密码学提供灵活的安全模型。这提供了数据的隐私和身份验证。 PeaZip 实用程序可作为开源引擎使用，可以根据需要为不同的操作系统编译。

## 豌豆文件格式

[PEA 文件格式规范](https://peazip.github.io/pea_help.pdf) 是公开的，供开发者参考。 PEA 档案是具有灵活安全模型和冗余完整性检查的二进制文件，范围从校验和到加密的强哈希。这定义了要控制的三个不同级别的通信：

* Streams - 由多个输入文件形成的实际输出数据流，可以写入多个输出卷
* 对象 - 输入文件和文件夹发送到 .pea 档案
* 卷 - 可以跨越用户定义大小的输出存档文件

其中每一项都是可选的，可以根据用户要求进行合并。 PEA 文件格式可以存储包含无限对象的单个流。每个流的大小最多为 2^64 字节。

PEA 文件在 EAX 或 HMAC 模式下使用 AES 提供可选的完整性检查和经过身份验证的加密，或者在 EAX 模式下使用 Twofish 和 Serpent。

### PEA 存档标题

归档标头为 10 个字节，结构如下。

|字节|说明|
---|---|
|1 |用于文件格式消歧的魔术字节字段：$EA|
|1 |版本号|
|1 |修订号|
|1 |音量控制方案|
|1 |声明构建流的操作系统|
|1 |声明操作系统日期和时间编码|
|1 |声明对象名称字符编码|
|1 |声明 CPU 类型（以 7 位编码）和字节序（以 msb 为单位）|
|1 |留作将来使用|

## 参考

* [PEA 文件格式规范](https://peazip.github.io/pea_help.pdf)
* [PEA 文件格式](https://peazip.github.io/pea-file-format.html#.pea_specifications)


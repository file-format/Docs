{
  "date" : "2019-10-11",
  "keywords" :["rar 文件","rar 文件格式","什么是 rar 文件","文件","rar 示例","rar 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RAR",
  "description":"什么是 RAR 文件扩展名和可以创建和打开 RAR 文件的 API。",
  "linktitle" : "RAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .rar 文件？

具有 .rar 扩展名的文件是为以压缩或正常形式存储信息而创建的存档文件。 RAR 代表 Roshal ARchive 文件格式，是由俄罗斯软件工程师 Eugene Roshal 于 1995 年创建的专有文件格式。该格式用于使用不同的方法归档文件，包括各种压缩技术。有几种应用软件可用于 Windows、Linux 和 MacOS 用于提取 RAR 文件。 WinRAR 软件，由 RARLab 提供，是 Microsoft Windows 平台的共享软件文件归档实用程序（免费 40 天）；该软件由同一作者 Eugene Roshal 移植到 Linux（仅作为提取器）。

## RAR 文件格式的版本历史

* v1.3（原创，没有“Rar！"签名）
* v1.5
* v2.0 - 随 WinRAR 2.0 和 Rar for MS-DOS 2.0 一起发布
* v2.9 - 在 WinRAR 3.00 版本中发布
* v5.0 - WinRAR 5.0 及更高版本支持

## RAR 格式的主要特点

RAR 在该领域已经存在了很长时间，并且一直是最受欢迎的归档文件格式之一。 RAR 格式的主要特点是：

**`高压缩比：`** 优于 [ZIP](/zh/compression/zip/)，可与 7z 和 zipx 格式媲美。

**`强大的文件加密设计：`** 加密的 RAR4 档案依赖于基于 AES-128 的加密，而加密的 RAR5 档案依赖于 AES-256 加密并改进了密钥调度

**`高级纠错和数据恢复功能：`** 存档创建期间的可选恢复记录

**`文件大小：`** 最小 20 字节和最大 2^63 字节大小（存档总大小的 8 艾字节）

**`多卷 RAR 档案：`** 可以将大型档案分成几个较小的文件，以便于通过网络传输。在这种情况下，文件扩展名增加 1 以表示拆分卷

## RAR 文件格式

RAR 格式的完整规范不公开，这就是为什么不能以简洁的方式制定有关格式的详细信息。

### 常规存档布局

5.0 版引入的 RAR 文件格式的总体布局如下：

|文件格式
---|
|自解压模块（可选）
|RAR 5.0 签名
|存档加密标头（可选）
|主存档标题
|存档评论服务标头（可选）
文件头 1
|前面文件的服务标头（NTFS ACL、流等）（可选）
|...
|文件头 N
|前面文件的服务标头（NTFS ACL、流等）（可选）
|恢复记录（可选）
|存档标题结束

上述RAR文件各部分的信息可以在[RAR 5.0文件格式规范](https://www.rarlab.com/technote.htm#arcstruct)文档中找到。

#### 自解压 RAR 档案

如果 RAR 文件本身是自解压的，则自解压信息包含在档案签名之前的文件开头。它的大小和内容没有定义。

#### RAR 5.0 签名

RAR 签名是一个 8 字节的标头，由以下幻数组成：

0x 52 61 72 21 1A 07 00

在哪里

0x6152 - HEAD_CRC

0x72 - HEAD_TYPE

0x1A21 - HEAD_FLAGS

0x0007 - HEAD_SIZE

## 参考

* [RAR 5.0 存档格式](https://www.rarlab.com/technote.htm)
* [RAR - 维基百科](https://en.wikipedia.org/wiki/RAR_(file_format))


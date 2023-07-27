{
  "date" : "2019-10-11",
  "keywords" :["gz 文件","gz 文件格式","什么是 gz 文件","文件","gz 示例","gz 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GZ 文件格式 - GNU 压缩存档文件",
  "description":"了解什么是 GZ 文件以及可以创建和打开 GZ 文件的 API。",
  "linktitle" : "GZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .gz 文件？

GZ 文件是使用标准 [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip) 压缩算法创建的压缩档案。它可能包含多个压缩文件,目录和文件存根。这种格式最初是为了替代 UNIX 系统上的压缩格式而开发的。并且仍然是 Linux 系统上最常见的存档类型之一。 [WinZip](https://www.winzip.com/en/) 等应用程序可以在 Windows 和 MacOS 上打开 GZ 文件以查看其内容。

## GZ 文件格式 - 更多信息

Gzip 使用 [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) 算法来压缩存档，与 [ZIP](/zh/compression/zip/) 存档格式不同的是，将压缩算法应用于完整存档而不是单个文件。由 Internet 工程任务组 (IETF) 发布的 GZIP 文件格式规范 4.3 版包含有关文件格式的详细信息。文件格式包括：

* 文件头
* 可选标题
* 压缩数据
* 文件页脚

## GZ 文件头 ##

GZ 文件头由 10 个字节组成，如下所示：

|偏移量|大小|值|描述
---|---|---|---|
|0|2|0x1f 0x8b|识别文件类型的幻数
|2|1| |压缩方式 * 0-7（保留）* 8（放气）
|3|1| |文件标志
|4|4| |32 位时间戳
|8|1| |压缩标志
|9|1| |操作系统标识

### 文件标志###

|值|标识符|描述
---|---|---|
|0x01|FTEXT|如果设置未压缩数据需要被视为文本而不是二进制数据。此标志提示跨平台文本文件的行尾转换，但不强制执行。
|0x02|FHCRC|文件包含头校验和 (CRC-16)
|0x04|FEXTRA|文件包含额外字段
|0x08|FNAME|文件包含原始文件名字符串
|0x10|FCOMMENT|文件包含注释
|0x20| |保留
|0x40| |保留
|0x80| |保留

＃＃＃ 操作系统 ＃＃＃

|价值|描述
---|---|
|0|FAT 文件系统 (MS-DOS, OS/2, NT/Win32)
|1|阿米加
|2|VMS（或 OpenVMS）
|3|Unix
|4|虚拟机/CMS
|5|雅达利服务条款
|6|HPFS 文件系统 (OS/2, NT)
|7|麦金塔
|8|Z-系统
|9|CP/M
|10|TOPS-20
|11|NTFS 文件系统 (NT)
|12|QDOS
|13|橡子RISCOS
|255|未知

## GZ 可选标题##

可选的额外标题是由文件标志表示的那些，包括原始文件名、额外字段、注释和标题校验和等信息。

## 压缩数据##

本节包含使用 DEFLATE 压缩算法的压缩数据。

## GZ 文件页脚##

文件页脚大小为 8 个字节，包含以下信息。

|偏移量|尺寸|描述
---|---|---|
|0|4|校验和 (CRC-32)
|4|4|以字节为单位的未压缩数据大小值

## 参考 ＃＃

* [gzip - 维基百科](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952：GZIP 文件格式规范](https://datatracker.ietf.org/doc/html/rfc1952)，由 IETF 提供。


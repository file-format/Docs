{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PST - Outlook 个人信息存储文件格式",
  "description":"了解 PST 文件格式和可以创建和打开 PST 文件的 API。",
  "linktitle" : "PST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .pst 文件？

带有 .pst 扩展名的文件表示存储各种用户信息的 Outlook 个人存储文件（也称为个人存储表）。用户信息存储在不同类型的文件夹中，包括电子邮件、日历项目、便笺、联系人和其他几种文件格式。 PST 文件用于离线归档电子邮件数据，以后可以在各种应用程序中加载和查看这些数据。

## PST 文件格式规范

PST 文件格式 [规范](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546) 可通过开放规范承诺从 Microsoft 作为免费且不可撤销的免费专利许可获得.

### PST 格式的类型

PST 文件格式根据文件类型的编码分为两种类型。 ANSI 编码的 PST 文件是较旧的文件格式，仅受 Outlook 2002 和更早版本支持。此类文件的最大大小限制为 2 GB（2^^31^^ 字节）并且不支持 Unicode。一种更现代的文件格式类型，基于 Unicode 编码，消除了文件大小限制，最大数据大小可达 50GB。

### PST 文件格式的逻辑组织

PST 文件格式的基础是 B-Tree，它保持数据排序并允许在对数时间内进行搜索、顺序访问、插入、删除等。 PST 文件的整体结构分为三层。

![Logical layers of a PST file](/zh/email/PST-1.png "Logical layers of a PST file")

`Node Database (NDB) Layer` - 节点数据库层位于 PST 文件的较低级别，包括节点数据库。这些节点实际上代表 PST 文件格式的较低级别的存储设施。从存储的角度来看，NDB 层由标头、文件分配信息、块和 BTree（Node BTree 和 Block BTree）组成。 NDB 层的节点和块通过数据 BID 链接，数据 BID 是节点引用的四个属性之一，即 NID（节点 ID）、父 NID、数据 BID（块 BID）和子节点 BID。

`Lists, Tables and Properties Layer -` LTP 层提供了对 NDB 之上更高级别概念的逻辑理解。除了其他元素，LTP 层主要包括属性上下文（PC）和表上下文（TC）。 PC 是属性的集合，而 TC 表示属性集合与这些属性的存在的二维矩阵。高效实现 PC 和 TC，LTP 层在 NDB 节点上使用以下两种类型的数据结构：

* Heap On Node (HN) - 允许将节点的数据流子分配到小的、可变大小的片段中。
* BTree on Heap (BTH) - BTH 提供了一种方便实用的数据搜索方式。如上所述，PC 是作为 BTH 实现的，这就是为什么它是通过在 HN 结构内部构建来实现的。

`消息传递层-` 用于处理 PST 文件的更高级别的规则和业务逻辑在此层实现。该层的逻辑输出结果为文件夹对象、消息对象、附件对象和属性，这通过组合 LTP 和 NDB 层而成为可能。修改 PST 内容时需要遵循的规则和要求也在这一层定义。

### PST 文件格式的物理组织

PST文件的高级文件组织如下图所示。这只是 PST 文件逻辑元素的不同概念的概述。

![Physical organization of the PST file format](/zh/email/PST-2.png "Physical organization of the PST file format")


#### PST 标头信息

PST 文件的 HEADER 结构位于文件的最开始处 0 偏移处。它包含有关 PST 文件的元数据信息和用于访问上述 NDB 层数据结构的 ROOT 信息。 Unicode 和 ANSI 版本的 PST 文件格式的 HEADER 结构不同。

标头以字节（0x21、0x42、0x44、0x4E）表示的 4 字节魔术字 **!BDN** 开头。另一个 2 字节幻数 **SM** (0x53, 0x4D) 位于文件开头的偏移量 8 处。版本信息（ANSI 或 Unicode）位于文件开头的 10 处。十六进制值 (0x17) 指定 Unicode PST 文件，而 0x0E 或 0x0F 表示 ANSI 文件格式。

|字段|描述
---|---|
|dwMagic（4 字节）|必须是“{ 0x21, 0x42, 0x44, 0x4E } ("!BDN")"
|dwCRCPartial (4 bytes)|从 wMagicClient (0ffset 0x0008) 开始的 471 字节数据的 32 位 CRC 值
|wMagicClient（2 字节）|必须是“{ 0x53, 0x4D }"。
|wVer (2 bytes)|文件格式版本。如果文件是 ANSI PST 文件，此值必须是 14 或 15，如果文件是 Unicode PST 文件，则必须是 23。
|wVerClient (2 bytes)|客户端文件格式版本。与本文档中描述的格式对应的版本是 19。基于本文档的新 PST 文件的创建者应该将此值初始化为 19。
|bPlatformCreate（1 字节）|该值必须设置为 0x01。
|bPlatformAccess（1 字节）|该值必须设置为 0x01。
|dwReserved（8 字节）|
|bidUnused（仅 8 字节 Unicode）|创建 Unicode PST 文件格式时添加的未使用填充。
|bidNextP（Unicode：8 字节；ANSI：4 字节）|下一页 BID。页面有一个特殊的计数器来分配 bidIndex 值。页面的 BID 的 bidIndex 值是从此计数器分配的。
|bidNextB（仅 4 字节 ANSI）：|下一个 BID。该值是指示要为下一个分配块分配的 BID 的单调计数器。 BID 值以 4 为增量递增。有关详细信息，请参阅第 2.2.2.2 节。
|dwUnique (4 bytes)|这是一个单调递增的值，每次修改 PST 文件的 HEADER 结构时都会修改。这个值的作用是提供一个唯一的值，并且保证每次header修改后HEADER CRCs是不同的。
|rgnid[]（128 字节）|32 个 NID 的固定数组，每个对应于 32 个可能的 NID_TYPE 之一（NID_TYPE、NID_TYPE_NORMAL_FOLDER、NID_TYPE_SEARCH_FOLDER、NID_TYPE_NORMAL_MESSAGE、NID_TYPE_ASSOC_MESSAGE）
|qwUnused (8 bytes)|未使用空间；必须设置为零。仅限 Unicode PST 文件格式。
|root（Unicode：72 字节；ANSI：40 字节）|ROOT 结构（第 2.2.2.5 节）。
|dwAlign (4 bytes)|未使用的对齐字节；必须设置为零。仅限 Unicode PST 文件格式。
|rgbFM（128 字节）|不推荐使用的 FMap。这不再使用，必须用 0xFF 填充。读者应该忽略这些字节的值。
|rgbFP（128 字节）|不推荐使用的 FPMap。这不再使用，必须用 0xFF 填充。读者应该忽略这些字节的值。
|bSentinel（1 字节）|必须设置为 0x80。
|bCryptMethod（1 字节）|指示 PST 文件中的数据如何编码。必须设置为预定义值之一（NDB_CRYPT_NONE、NDB_CRYPT_PERMUTE、NDB_CRYPT_CYCLIC）。
|rgbReserved (2 字节)|预订的;必须设置为零。
|bidNextB（8 字节）|指示下一个可用的 BID 值。仅限 Unicode PST 文件格式。
|bidNextB（仅 Unicode：8 字节）|下一个 BID。该值是指示要为下一个分配块分配的 BID 的单调计数器。 BID 值以 4 为增量递增。有关详细信息，请参阅第 2.2.2.2 节。
|dwCRCFull (4 bytes)|从 wMagicClient 到 bidNextB 的 516 字节数据的 32 位 CRC 值。仅限 Unicode PST 文件格式。
|ullReserved（8 字节）|保留；必须设置为零。仅限 ANSI PST 文件格式。
|dwReserved（4 字节）|保留；必须设置为零。仅限 ANSI PST 文件格式。
|rgbReserved2 (3 字节)|
|b保留（1 字节） |
|rgbReserved3 (32 字节) |

＃＃＃ 数据保护 ＃＃＃

为了安全起见，PST 文件也可以受密码保护，这需要加载应用程序在查看之前应用密码。应用于 PST 文件的密码存储在消息存储中。但是，这并不能提供强大的数据保护，因为可用工具可以删除密码。此外，用户指定的密码不用作编码和解码密码算法的密钥的一部分。因此，保护未经授权方访问的数据没有任何好处。将密码存储为原始字符串的 CRC-32 哈希也使其成为针对暴力方法的数据安全性较弱的方法。

## 参考 ＃＃

* [Outlook 个人文件夹 (.pst) 文件格式](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [个人文件夹文件格式规范](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)


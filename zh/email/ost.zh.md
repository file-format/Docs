{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OST - Outlook 存储文件格式",
  "description":"了解 OST 文件格式和可以创建和打开 OST 文件的 API。",
  "linktitle" : "OST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .ost 文件？

OST 或脱机存储文件代表用户在使用 Microsoft Outlook 向 Exchange Server 注册时在本地计算机上处于脱机模式的邮箱数据。它是在与服务器连接后首次使用 Microsoft Outlook 时自动创建的。创建文件后，数据将与电子邮件服务器同步，以便在与电子邮件服务器断开连接的情况下也可以脱机使用。 OST 文件可以用户邮箱项目，如电子邮件、联系人、日历信息、便笺、任务和其他类似数据。即使没有连接到服务器，用户也可以在 OST 文件中创建电子邮件和其他数据项，但这些不会与服务器同步。建立连接后，本地文件再次与服务器同步，使服务器和本地副本处于同一信息级别。

## OST 文件格式

OST（离线存储表）和 [PST](/zh/email/pst/)（个人存储表）文件格式由对应于存储用户的电子邮件、联系人和约会的个人文件夹文件 (PFF) 格式组成。 PFF 文件中的数据以 little-endian 格式存储，所有日期和时间均以 UTC 格式的 FILETIME 表示。 [MS-PST] 定义了两种类型的 PFF：

* 32 位 ANSI 格式
* 64 位 Unicode 格式

PST 文件格式 [规范](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx) 可从 Microsoft 获得，也适用于免费和免费的 OST 文件格式通过 Open Specification Promise 获得不可撤销的专利许可。它由以下可区分的元素组成：

* 文件头
* 文件头数据
* 索引分支节点
* 索引叶节点
*（文件）偏移索引
*（项目）描述符索引
* 本地描述符
* 项目表类型

### 标头信息

OST 文件的 HEADER 结构位于文件的最开始处 0 偏移处。它包含有关 OST 文件的元数据信息和用于访问上述 NDB 层数据结构的 ROOT 信息。 OST 文件格式的 Unicode 和 ANSI 版本的 HEADER 结构不同。

标头以字节（0x21、0x42、0x44、0x4E）表示的 4 字节魔术字 **!BDN** 开头。另一个 2 字节幻数 **SM** (0x53, 0x4D) 位于文件开头的偏移量 8 处。版本信息（ANSI 或 Unicode）位于文件开头的 10 处。十六进制值 (0x17) 指定 Unicode OST 文件，而 0x0E 或 0x0F 表示 ANSI 文件格式。

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

## 参考

* [Outlook 个人文件夹 (.ost) 文件格式](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx)
* [个人文件夹文件格式规范](https://github.com/libyal/libpff/blob/master/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)


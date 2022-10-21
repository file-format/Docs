{
  "date" : "2019-12-03",
  "keywords" :[ "doc", "file", "extension", "file format", "Word", "Document" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOC - Microsoft Word 文档文件",
  "description":"了解可以创建和打开 DOC 文件的 DOC 文件格式和 API。",
  "linktitle" : "DOC",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## 什么是一 .doc 文件？

带有 .doc 扩展名的文件表示由 Microsoft Word 或其他二进制文件格式的文字处理文档生成的文档。该扩展最初用于几个不同操作系统上的纯文本文档。它可以包含几种不同类型的数据，例如图像、格式化以及纯文本、图形、图表、嵌入对象、链接、页面、页面格式、打印设置等等。该格式在各种文档中都很流行，因为它为用户提供了编写手册、提案、规范、简历、文章或任何类似文档的多种选项。 DOC 的更新版本是 [DOCX](/zh/Word%20Processing/DOCX/)，它基于 Office OpenXML，其规范是公开可用的。

## 历史简介 ＃＃

[Corel](https://www.corel.com/en/) 的产品 WordPerfect 使用 DOC 作为其专有格式的扩展。在 1980 年代，WordPerfect 仍然是大多数计算机的使用选择，因为它易于使用，符合大多数计算机机器和操作系统。然而，当微软将 Microsoft Word 作为其文档文件格式产品并选择 DOC 扩展作为其专有格式时，WordPerfect 在 Windows 操作系统上的失败。随着 Microsoft Word 变得越来越流行，DOC 文件格式从 Microsoft Word 97 到 2003 经历了几次修订。在 2007 年，默认的 DOC 文件格式被 Office Open XML 格式（称为 DOCX）和新版本的Microsoft Word 现在将此新扩展名用作默认文件格式。

## DOC 文件格式规范 - 更多信息

微软直到 2008 年才发布了很长时间的 DOC 文件格式规范。2008 年 2 月，在 Microsoft Open Specification Promise 下发布了 .doc 文件格式的格式规范。尽管该规范没有描述 DOC 格式使用的所有功能，但它提供了有关使用此文件格式所需知识的充足信息。尽管如此，仍需要逆向工程来利用可用信息。规范已多次更新，最新的 [revision](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx) 为 8.0，于 2018 年 8 月更新.

###一些基本概念###

在我们深入了解 DOC 文件格式规范的任何细节之前，需要了解一些基本概念才能使用此文件格式。

**文件信息库 (Fib)：** Fib 结构包含有关文档的信息，并指定指向构成文档的各个部分的文件指针。
Fib 是可变长度结构。除了大小固定的基本部分之外，每个部分前面都有一个计数字段，用于指定下一个部分的大小。

**字符位置：** CP 或字符位置表示一个无符号 32 位整数，用作文档文本中字符的从零开始的索引。无法直接检索文件中每个字符的位置和大小，需要使用预先指定的算法计算。人物包括：

* 文件的文本
* 对象的锚点，例如脚注或文本框
* 控制字符，例如段落标记和表格单元格标记

**PLC：** PLC 结构是一个 CP 数组，后跟一个数据元素数组。任何 PLC 的数据元素必须是相同大小的零个或多个字节，因此，CP 的数量必须比数据元素的数量多 1。 PLC 结构具有不同的类型，其中每种类型都指定该类型是否允许重复的 CP。 PLC 结构包括：

* **aCP（可变长度）：** CP 元素的数组。每种类型的 **PLC** 结构都指定了 CP 元素的含义和允许的范围。
* **aData（可变长度）：** 每种类型的**PLC** 结构都指定了数据元素的结构和含义，对数据元素数量的任何限制，以及对其中包含的数据的任何限制。它还规定了数据元素和相应的 CP 之间的关系。

**有效选择：** .DOC 文件结构主要由一系列 CP 描述。在这种情况下，Microsoft 指定了许多要遵循的 [规则](https://msdn.microsoft.com/en-us/library/dd908861(v#office.12).aspx)。

**STTB：** STTB 是一个字符串表，它由一个标头组成，后跟一个元素数组。 **cData** 值指定数组中包含的元素数量。

**属性存储：**一个word文件可能有不同的元素，如文本、段落、表格、图片和部分，每个元素都可以有自己的属性。这些属性作为与默认值的差异存储在 Word 文件中。此类差异由 PR1 指定，该 PR1 由单个属性修饰符 (Sprm) 及其操作数组成。应用程序可以通过应用**Prl**s 列表来确定最终的属性集。

**密码保护：** Word 文件也可以使用密码保护，可以使用以下机制之一。

* XOR 混淆
* Office 二进制文件 RC4 加密
* Office 二进制文件 RC4 CryptoAPI 加密

如果 FibBase.fEncrypted 和 FibBase.fObfuscation 均为 1，则使用 XOR 混淆对文件进行混淆。

如果 FibBase.fEncrypted 为 1 且 FibBase.fObfuscation 为 0，则使用 Office Binary Document RC4 Encryption 或 Office Binary Document RC4 CryptoAPI Encryption 对文件进行加密，其中 EncryptionHeader 存储在 Table 流的第一个 FibBase.lKey 字节中。 EncryptionHeader.EncryptionVersionInfo 指定用于加密文件的加密机制。

### 文件结构###

原始的二进制 Word 文件是由多个存储和流组成的 OLE 复合文件。这些存储和流具有自己的结构和大小，指定了写入和读取的参数。这些是：

#### WordDocument 流####

此流包含从文件的其他部分引用的文档文本和其他信息。除了开头的 FIB 之外，该流没有预定义的结构，FIB 是强制性的，并且应该位于偏移量 0 处。该流不得大于 2147 MB。

#### 1TableStream 或 0TableStream ####

二进制 Word 文件可以包含称为 1Table 流或 0Table 流的表流。至少其中一个应该出现在文档中。但是，如果文档同时包含 1Table 和 0Table 流，则仅使用 base.fWhichTblStm 引用的流。必须忽略未引用的流。
表流不得大于 2147 MB。

＃＃＃＃ 数据流 ＃＃＃＃

数据流没有预定义的结构。它包含从 FIB 或文件的其他部分引用的数据。如果没有对它的引用，则不需要存在此流。数据流不得大于 2147 MB。

#### 对象池存储####

对象池存储包含嵌入式 OLE 对象的存储。如果文档中没有嵌入的 OLE 对象，则不需要存在此存储。

#### 自定义 XML 数据存储 ####

自定义 XML 数据存储是一个可选存储，其名称必须是“MsoDataStore"。

#### 摘要信息流####

摘要信息流是一个可选流，其名称必须是“\005SummaryInformation"，其中 \005 是值为 0x0005 的字符，而不是字符串文字“\005"。

#### 文档摘要信息流####

文档摘要信息流是一个可选流，其名称必须是“\005DocumentSummaryInformation"，其中 \005 是值为 0x0005 的字符，而不是字符串文字“\005"。

#### 加密流####

加密流是一个可选流，其名称必须是“加密"。除非满足以下两个条件，否则不得存在此流：

* 该文档使用 Office Binary Document RC4 CryptoAPI Encryption 进行加密。
* fDocProps 值在 EncryptionHeader.Flags 中设置。

#### 宏存储####

宏存储是包含文件宏的可选存储。如果存在，它必须是项目根存储。

#### XML 签名存储####

XML 签名存储是一个可选存储，其名称必须是“_xmlsignatures"。

#### 签名流####

签名流是一个可选流，其名称必须是“_signatures"。此流包含数字签名。

#### 信息权限管理数据空间存储####

信息权限管理数据空间存储是一个可选存储，其名称必须是“\006DataSpaces"，其中 \006 是值为 0x0006 的字符，而不是字符串文字“\006"。如果此存储存在，则受保护的内容流也必须存在。
如果此存储存在，则应从 [MS-OFFCRYPTO] 中指定的受保护内容流中读取除此存储和受保护内容流之外的所有指定流和存储，并且如果这些流和存储中的任何一个存在于受保护内容之外流，它们应该被忽略。

#### 受保护的内容流####

受保护的内容流是一个可选流，其名称必须是“\009DRMContent"，其中 \009 是值为 0x0009 的字符，而不是字符串文字“\009"。
如果该流存在，则信息权限管理数据空间存储也必须存在。

## 参考 ＃＃

* [MS-DOC 文件格式规范](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx)
* [文档计算](https://en.wikipedia.org/wiki/Doc_(computing))


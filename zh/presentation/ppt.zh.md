{
  "date" : "2019-12-13",
  "keywords" :[ "ppt 文件", "ppt 文件格式", "什么是 ppt 文件", "文件", "ppt 示例", "ppt 文件扩展名","扩展名", "格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 PPT 文件格式和可以创建和打开 PPT 文件的 API。",
  "title" :"PPT - PowerPoint 文件格式",
  "linktitle" : "PPT",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是PPT文件？

带有 PPT 扩展名的文件表示 PowerPoint 文件，该文件由一组幻灯片组成，用于显示为 SlideShow。它指定 Microsoft PowerPoint 97-2003 使用的二进制文件格式。一个 PPT 文件可以包含多种不同类型的信息，例如文本、项目符号点、图像、多媒体和其他嵌入的 OLE 对象。从 2007 年起，Microsoft 提出了更新的 PowerPoint 文件格式，称为 [PPTX](/zh/presentation/pptx/)，它基于 Office OpenXML，与这种二进制文件格式不同。 OpenOffice Impress 和 Apple Keynote 等其他几个应用程序也可以创建 PPT 文件。

## 历史简介 ＃＃

Microsoft 在 1987 年发布 PowerPoint 时引入了 PPT 文件格式。稳定的二进制格式在 PowerPoint 97-2003 for Windows 中被共享为默认格式。最新版本的 PowerPoint 以及包括 PowerPoint 2016 在内的二进制文件格式都支持读取和写入。

## 文件格式规范##

自推出以来，PPT 文件格式经历了多次修订，以增加新功能和增强功能。可用的最新版本规范是 2018 年 8 月发布的 6.0 版规范，不应与 PPT 文件格式的实际产品编号混合，因为 Microsoft 不再提供对该格式的修改。

### 文件格式概述###

PPT 文件格式的一些关键组成部分如下：

#### 幻灯片####

形状、文本、动画和媒体等用户数据被添加到幻灯片内的演示文稿中。演示文稿可以包含一张或多张幻灯片，这些幻灯片在演示文稿运行时显示为幻灯片。演示文稿包含母版幻灯片和标题母版幻灯片，它们充当演示文稿幻灯片的常见视觉属性的模板。还有一个笔记母版幻灯片和讲义母版幻灯片，其用途相似，并为所有笔记幻灯片和所有打印的讲义提供通用的视觉属性。

#### 形状####

形状是允许用户以占位符形状、图片和图表的形式向幻灯片添加各种内容的对象。母版幻灯片上的形状定义形状组的通用数据。

#### 占位符形状####

这些是特殊的占位符，用作各种对象的容器。不同的占位符形状可用于为插入特定类型的形状（如表格或图表）提供线索。在幻灯片内部，占位符形状采用主母版幻灯片、标题母版幻灯片或备注母版幻灯片的视觉属性。

#### 外部对象####

可以在幻灯片中嵌入外部对象，例如嵌入和链接的音频、链接的视频、嵌入和链接的 OLE 对象以及超链接。这些对象可用于激活链接对象，以便在幻灯片放映期间访问外部资源。

### 文件格式结构###

PowerPoint 二进制文件格式由以下流组成，以表示整体文档结构和数据。

* 当前用户流
* PowerPoint 文档流
*图片流
* 摘要信息和文档摘要信息（可选）

DOC 文件格式的完整规范可在 [Microsoft](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx) 中找到，应查阅参考以下详细信息中提到的部分。

#### 当前用户流####

它记录最后打开文档的用户，其名称必须是“当前用户"。

#### PowerPoint 文档流####

记录有关 PowerPoint 演示文稿的所有信息并解释其布局和内容。它是一个必需的流，其名称必须是“PowerPoint 文档"。此流的内容由一系列顶级记录指定。 PersistDirectoryAtom 和 UserEditAtom 记录中指定了记录序列的部分排序限制。

作为容器记录，DocumentContainer、MainMasterContainer（第 2.5.3 节）、HandoutContainer（第 2.5.8 节）、SlideContainer（第 2.5.1 节）和 NotesContainer（第 2.5.6 节）记录都是容器记录树的根和原子记录。在任何容器记录中，可以存在未明确列为子记录的其他记录。当 RecordHeader 结构（第 2.3.1 节）的 recType 字段包含 RecordType 枚举（第 2.13.24 节）未指定的值时，将识别未知记录。如果遇到这些未知记录，必须忽略，并且可以<1> 保留。通过从 RecordHeader 结构的末尾向前寻找 recLen 字节，可以忽略未知记录。

每次写入此流时，可以将新的顶级记录（用户编辑）附加到现有流中，或者可以用更新的顶级记录序列替换整个流内容。如果不替换整个流，则包括任何先前用户编辑的任何先前存在的顶级记录都可以被随后附加的包括当前用户编辑的顶级记录废弃。

####图片流####

这是一个可选流，包含有关 PowerPoint 演示文稿中包含的图片的数据。它的名称必须是“图片"。此流的内容由 [MS-ODRAW] 第 2.2.21 节中指定的 OfficeArtBStoreDelay 记录指定。

#### 摘要信息流####

它按照 Microsoft Office 标准保存有关文档的统计信息。摘要信息流的名称必须是“\005SummaryInformation"，其中\005是值为0x0005的字符，而不是字符串文字“\005"。对于加密的文档，应该省略这个流。此流的内容在 [MS-OSHARED] 2.3.3.2.1 节中指定。

#### 文档摘要信息流####

名称必须为“\005DocumentSummaryInformation"的可选流，其中 \005 是值为 0x0005 的字符，而不是字符串文字“\005"。对于加密文档，该流可以省略<2>。该流的内容在 [MS-OSHARED] 2.3.3.2.2 节中指定。

#### 加密摘要信息流####

名称必须为“EncryptedSummary"的可选流。此流仅存在于加密文档中。此流的内容在 [MS-OFFCRYPTO] 部分 2.3.5.4 中指定。

#### 数字签名存储####

名称必须是“_xmlsignatures"的可选存储。它可以被省略，也可以被忽略。此存储的内容在 [MS-OFFCRYPTO] 部分 2.5.2 中指定。

#### 自定义 XML 数据存储 ####

名称必须为“MsoDataStore"的可选存储。存储的内容在 [MS-OSHARED] 2.3.6 节中指定。

#### 签名流####

名称必须为“_signatures"的可选流。它应该被省略并且可以被忽略。此流的内容在 [MS-OFFCRYPTO] 2.5.1 节中指定。

## 参考 ＃＃

* [PPT文件格式规范](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)
* [[MS-OSHARED]：Office 常用数据类型和对象结构](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)
* [[MS-OFFCRYPTO] - Office 文档加密结构](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)
* [PowerPoint 文件格式](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)


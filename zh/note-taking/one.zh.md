{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONE - Microsoft OneNote 文件格式",
  "description":"了解可以创建和打开 ONE 文件的 ONE 文件格式和 API。",
  "linktitle" : "ONE",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是 .ONE 文件？ ##

由 .ONE 扩展名表示的文件由 Microsoft OneNote 应用程序创建。 OneNote 让您可以使用应用程序收集信息，就像使用草稿板记笔记一样。 OneNote 文件可以包含不同的元素，这些元素可以放置在文档页面上的非固定位置。这些元素可能包含文本、数字化手写和从其他应用程序复制的对象，包括图像、绘图和多媒体（音频/视频）剪辑。微软现在提供 OneNote 的在线版本作为 Office365 的一部分，Notes 可以通过 Internet 与其他 OneNote 用户共享。

## .ONE 文件格式规范 ##

OneNote 文件格式提供了一种将数字笔记表示为部分和页面的分层集的有效方法。每个页面都包含特定结构中的用户定义内容，以文件格式文档对象模型 (DOM) 表示。这种格式的数据模型如下图所示。

### 结构概述###

如 OneNote 文件格式的数据模型所示，OneNote 文档由不同的元素组成。

＃＃＃＃ 部分 ＃＃＃＃

节是 OneNote 文件中最顶层的容器，其中还包含不同的元素，例如：

* 页面
* 元数据
* 特性

元数据和属性包括部分名称、部分中包含的页面的标识以及这些页面出现的顺序。术语“节"是指节中的所有页面以及该数据在 OneNote® 修订存储文件中的表示，该文件具有 .one 文件扩展名。

＃＃＃＃ 页 ＃＃＃＃

OneNote 文档中的用户定义内容包含在页面内。页面信息包括文本、列表、表格、页面标题、图像和注释标签。页面由大纲对象组成，大多数包含的对象都添加到这些对象中。可以为每个页面分配一个名称以进行有意义的表示，并且也可以将对象直接添加到页面中。一个页面可以进一步包含分层系统中的子页面。

#### 属性和属性集####

OneNote 内容由属性、属性集和文件数据对象组成。属性集是表示某种类型内容的属性的集合。文件数据对象是包含图片、嵌入文件或音频/视频内容的二进制数据块。

#### OneNote 笔记本####

笔记本是存储在同一目录中的部分文件的集合。属性集合用于指定设置，例如笔记本中各部分的顺序和笔记本的颜色。

### 文件结构###

修订存储文件必须以 **Header** 结构开头。文件的其余部分被划分为字节块，其中每个块的大小和结构由引用它的字段指定。如果块被 **Header** 结构引用，或者被另一个可达块中的字段引用，则块是可达的。 **Header** 结构之外的数据和任何可到达的块必须被忽略。

所有结构都在 1 字节边界上对齐。除非另有说明，否则所有整数都有符号。除非另有说明，否则所有字段都是 [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7)。

#### 标题####

.ONE 文件的标头由包含不同唯一 ID 和字段的块组成，用于表示文件信息，如下所示：

`guidFileType（16 字节）：` 指定修订存储文件类型的 GUID。必须是下表中的值之一。


|文件格式|值
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile（16 字节）：` 指定此修订存储文件标识的 GUID。应该是全球唯一的。

`guidLegacyFileVersion（16 字节）：` 必须是“{00000000-0000-0000-0000-000000000000}"并且必须被忽略。

`guidFileFormat（16 字节）：` 指定文件是修订存储文件的 GUID。必须是“{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}"。

`ffvLastCodeThatWroteToThisFile（4 个字节）：` 一个无符号整数。必须是下表中的值之一，具体取决于文件类型。

|文件格式|值
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile（4 字节）：` 一个无符号整数。必须是下表中的值之一，具体取决于此文件的文件格式。


|文件格式|值
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile（4 字节）：` 一个无符号整数。必须是下表中的值之一，具体取决于此文件的文件格式。

|文件格式|值
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile（4 个字节）：` 一个无符号整数。必须是下表中的值之一，具体取决于此文件的文件格式。

|文件格式|值
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList（8 字节）：` 必须具有“fcrZero"值的 **FileChunkReference32** 结构。

`fcrLegacyTransactionLog（8 字节）：` 必须为“fcrNil"的**FileChunkReference32** 结构。

`cTransactionsInLog（4 字节）：` 一个无符号整数，指定事务日志中的事务数。不得为零。

`cbLegacyExpectedFileLength (4 bytes):` 一个必须为零且必须被忽略的无符号整数。

`rgbPlaceholder (8 bytes):` 一个必须为零且必须被忽略的无符号整数。

`fcrLegacyFileNodeListRoot（8 字节）：` 必须为“fcrNil"的**FileChunkReference32** 结构。

`cbLegacyFreeSpaceInFreeChunkList (4 bytes):` 一个必须为零且必须被忽略的无符号整数。

`fNeedsDefrag (1 byte):` 必须被忽略。

`fRepairedFile (1 byte):` 必须被忽略。

`fNeedsGarbageCollect（1 字节）：` 必须被忽略。

`fHasNoEmbeddedFileObjects（1 字节）：` 必须为零且必须被忽略的无符号整数。

`guidAncestor (16 bytes):` 一个 GUID，指定目录文件的 **Header.guidFile** 字段，由下表给出：


|目录文件格式|目录文件的位置
--- | --- |
|Section File - .One|目录文件与该文件位于同一目录中。
|目录文件 - .onetoc2|目录文件位于该文件的父目录中。

如果 GUID 为 {00000000-0000-0000-0000-000000000000}，则此字段不引用目录文件。

`crcName（4 字节）：` 一个无符号整数，指定此修订存储文件名称的 CRC 值。名称是文件名的 Unicode 表示形式，其扩展名和末尾的附加空字符。此 CRC 始终使用 .one 文件的 CRC 算法计算，无论此修订存储文件格式如何。

`fcrHashedChunkList（12 字节）：` 一个 **FileChunkReference64x32** 结构，指定对散列块列表中第一个 **FileNodeListFragment** 的引用。如果 **FileChunkReference64x32** 结构的值为“fcrZero"或“fcrNil"，则哈希块列表不存在。

`fcrTransactionLog（12 字节）：` 一个 **FileChunkReference64x32** 结构，指定对事务日志中第一个 **TransactionLogFragment** 结构的引用。 **fcrTransactionLog** 字段的值不得为“fcrZero"且不得为“fcrNil"。

`fcrFileNodeListRoot（12 字节）：` 一个 **FileChunkReference64x32** 结构，指定对根文件节点列表的引用。 **fcrFileNodeListRoot** 字段的值不得为“fcrZero"且不得为“fcrNil"。

`fcrFreeChunkList（12 字节）：` 一个 **FileChunkReference64x32** 结构，指定对第一个 **FreeChunkListFragment** 结构的引用。如果**FileChunkReference64x32**结构的值为“fcrZero"或“fcrNil"，则空闲块列表不存在。

`cbExpectedFileLength (8 bytes):` 一个无符号整数，指定此修订存储文件的大小（以字节为单位）。

`cbFreeSpaceInFreeChunkList (8 bytes):` 一个无符号整数，应该指定空闲块列表指定的空闲空间的大小（以字节为单位）。

`guidFileVersion（16 字节）：` 一个 GUID。当 **cTransactionsInLog** 字段或 **guidDenyReadFileVersion** 字段的值被更改时，**guidFileVersion** 必须更改为新的 GUID。

`nFileVersionGeneration（8 字节）：` 一个无符号整数，指定文件更改的次数。当 **guidFileVersion** 字段更改时，必须增加。

`guidDenyReadFileVersion（16 字节）：` GUID。当文件的现有内容被更改时，除了文件的**Header** 结构和未使用的存储块，**guidDenyReadFileVersion** 必须更改为新的 GUID。

`grfDebugLogFlags (4 bytes):` 必须为零。必须忽略。

`fcrDebugLog（12 字节）：` 必须具有值“fcrZero"的**FileChunkReference64x32** 结构。必须忽略。

`fcrAllocVerificationFreeChunkList (12 bytes):` 必须为“fcrZero"的**FileChunkReference64x32** 结构。必须忽略。

`bnCreated（4 字节）：` 一个无符号整数，指定创建此修订存储文件的应用程序的内部版本号。应该被忽略。

`bnLastWroteToThisFile（4 字节）：` 一个无符号整数，指定上次写入此修订存储文件的应用程序的内部版本号。应该被忽略。

`bnOldestWritten（4 字节）：` 一个无符号整数，指定写入此修订存储文件的最旧应用程序的内部版本号。应该被忽略。

`bnNewestWritten（4 字节）：` 一个无符号整数，指定写入此修订存储文件的最新应用程序的内部版本号。应该被忽略。

`rgbReserved (728 bytes):` 必须为零。必须忽略。

## 参考 ＃＃

* [[MS-ONESTORE] - OneNote 文件格式](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - 维基百科](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)


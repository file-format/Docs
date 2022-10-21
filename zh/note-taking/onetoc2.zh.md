{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONETOC2 - Microsoft OneNote 文件格式",
  "description":"了解 ONETOC2 文件格式和可以创建和打开 ONETOC2 文件的 API。",
  "linktitle" : "ONETOC2",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是 ONETOC2？ ##

使用过 [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app) 应用程序的人可能已经注意到笔记本文件夹中存在 .onetoc2 文件。 Microsoft OneNote 创建二进制 .onetoc2 文件作为目录，用于保存有关笔记本中不同笔记记录部分排序的索引。笔记本是存储在同一目录中的部分文件的集合。 .onetoc2 文件使用一组属性来指定设置，例如笔记本中的部分顺序和笔记本的颜色。

在 OneNote 2016 中创建笔记本时，它会自动保存为新的 2010-2016 文件格式。如果您希望 OneNote 2016 中的所有功能（例如数学方程式和链接笔记）正常工作，您将需要这种格式。

## ONETOC2 文件格式 ##

.onetoc2 文件格式表示为 OneNote 修订存储文件格式，它是一组结构，这些结构指定组织到交叉引用的对象空间中的修订存储，包含具有属性集的对象，并包含事务日志以确保跨异步文件的完整性写道。 [在线](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) 提供了 .onetoc2 文件格式的完整规范，并且可以参考开发应用程序.

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
：


|文件格式|值
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile（4 个字节）：` 一个无符号整数。必须是下表中的值之一，具体取决于此文件的文件格式。


|文件格式|值
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

## 参考 ＃＃

* [[MS-ONESTORE] - OneNote 文件格式](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - 维基百科](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)


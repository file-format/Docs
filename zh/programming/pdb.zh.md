{
  "date" : "2019-10-11",
  "keywords": [ "pdb file", "pdb", "extension", "format", "What is a pdb file", "pdb file format", "PDB metadata" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDB 文件格式 - 程序数据库文件",
  "description":"了解 PDB 文件格式和可以创建和打开 PDB 文件的 API。",
  "linktitle" : "PDB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## 什么是一 .pdb 文件？

扩展名为 .pdb 的文件是一个程序数据库文件，其中包含已编译的可执行文件 (EXE/DLL) 的调试信息。在调试模式下编译应用程序时，Microsoft 编译器会生成 PDB 文件。 PDB 文件的存在有助于对可执行文件进行逆向工程，因为它包含有关模块所有符号的重要信息。正是由于这个原因，这些文件与最终的可执行文件分开。微软的[DgbHelp API](https://learn.microsoft.com/en-us/windows/win32/debug/dbghelp-functions)可以打开一个PDB文件来获取publics和exports、全局符号、局部符号、输入数据、源文件和行号。

## PDB 文件格式

PDB 是 Microsoft 的专有文件格式，尚未在任何地方正式记录。但是，[此处](https://github.com/Microsoft/microsoft-pdb) 提供了一个起始文档，并且可以参考。

### PDB 流

PDB 文件由多个流组成，其中每个流充当一个虚拟的单个文件并包含信息。 PDB 文件编写者可以写入这些文件，并且仅在发出显式提交后才最终确定文件。编译器可以继续写入 PDB 文件，但只有在所有用户代码编译成功时才提交。 PDB 文件由以下流组成：

|流序号 |内容 |简短说明|
---|---|---|
|1| Pdb（标头）|版本信息，以及将此 PDB 连接到 EXE 的信息|
|2| Tpi（类型管理器）|可执行文件中使用的所有类型。|
|3| Dbi（调试信息）|保存部分贡献和“Mods"列表|
|4|名称地图|保存散列字符串表|
|4-(n+4)| n Mod's（模块信息）|每个 Mod 流包含一个 compiland| 的符号和行号
|n+4|全局符号哈希|允许按名称搜索全局符号的索引|
|n+5|公共符号哈希|允许按地址搜索公共符号的索引|
|n+6|符号记录|全局和公共符号的实际符号记录|
|n+7|输入哈希| TPI 流使用的哈希值。|

PDB 文件中的每个流都包含若干页，这些页不一定是连续编号的。

### PDB 标头

一个 PDB 文件具有一个包含用于识别和验证特定格式的签名的标题。签名的长度取决于 PDB 格式。标题可能比单页长。

### PDB 元数据
PDB 元数据负责识别所有组件流，给出每个流的长度和页面序列。连续给流下达命令；从 0 开始。还有一个无序的根流，其中包含一些元数据。

## 参考
* [PDB - 维基百科](https://en.wikipedia.org/wiki/Program_database)
* [微软 PDB](https://github.com/Microsoft/microsoft-pdb)


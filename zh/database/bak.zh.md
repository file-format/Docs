{
  "date" : "2020-11-11",
  "keywords" :["BAK","扩展名","文件","文件格式","BAK文件类型","BAK文件扩展名","数据库文件类型","数据库文件格式","数据库文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 BAK 文件格式和可以创建和打开 BAK 文件的 API。",
  "title" :"BAK 文件格式 - 数据库备份文件",
  "linktitle" : "BAK",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-12-04"
}

## 什么是一 .bak 文件？

带有 .bak 扩展名的文件通常是一个备份文件，不同的软件工具使用它来存储数据的备份。从数据库的角度来看，Microsoft SQL Server 使用 BAK 文件来存储数据库的内容。与数据库关联的所有数据和文件都以这种文件格式存储，以便在数据库因任何原因损坏或无效时进行检索。出于安全目的，可以在其他服务器上存储和索引备份文件。多个应用程序可以创建 BAK 文件，例如 SQL Server Management Studio、Transact-SQL 和 Windows PowerShell。

## BAK 文件格式

BAK 文件的内部细节未知，但人们普遍认为它基于 Microsoft 磁带格式 (MTF)。 MTF 规范可用，可以参考以了解文件的结构。该文档为具有存储管理操作、磁带驱动器和文件系统的一般知识的任何人提供有关 MTF 存储的详细信息。

### 数据集

数据集是在数据备份或恢复期间写入存储介质（磁带、光盘等）的对象的集合。在大量数据的情况下，数据集由多种媒体组成。

### MTF 的基本要素

MTF 文件由构成其构建块的一些基本元素组成。这些元素是：

#### 描述符块

描述符块 (DBLK) 用于格式控制并构成 MTF 文件的主要基础。单个 MTF 文件为每个唯一角色定义多个 DBLK。每个 DBLK 是一个可变长度的数据块，分为以下四个部分：

* `Common Block Header` - 所有 DBLK 通用的固定长度结构。这是唯一需要的块头。
* `DBLK 类型信息` - 特定于正在定义的 DBLK 类型的固定长度块
* `Operating System Data` - 根据 DBLK 类型和操作系统定义的特定数据
* `DBLK 信息` - 不能与固定长度 DBLK 信息一起保存的可变长度 DBLK 特定信息。

 {{< figure src="../bak.png" alt="Microsoft SQL 备份文件格式" >}}

＃＃＃＃ 数据流

MTF 文件中的数据流用于数据封装和对齐。它包括一个流标头，后跟流数据。一个流头只能封装一种类型的流数据。

{{< figure src="../bak_datastream.png" alt="Microsoft SQL 备份文件格式" >}}

#### 文件标记

文件标记用于在媒体中进行逻辑分隔和快速访问。文件标记由设备驱动程序或通过使用软文件标记描述符块来模拟，以防正在使用的设备不提供文件标记。

## 参考 ＃＃

* [[MS-BCP]：批量复制格式](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)


{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EDB 文件格式 - Exchange 邮件数据库文件",
  "description":"了解 EDB 文件格式和可以创建和打开 EDB 文件的 API。",
  "linktitle" : "EDB",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2020-09-16"
}

## 什么是一 .edb 文件？

具有 .edb 文件扩展名的文件是由 Microsoft Exchange Server 创建的邮箱数据库，用于存储与邮件相关的数据。 EDB，Exchange 数据库，存储进程中和非 SMTP 的消息。 EDB 也称为可扩展存储引擎 (ESE) 数据库文件，并使用 b-tree 结构存储文件。作为存储文件，EDB 文件可以转换为其他邮件存储文件格式，例如 [PST](/zh/email/pst/) 和 [OST](/zh/email/ost/)。

## 教育局文件格式

没有可供参考的官方/开放 EDB 文件格式规范。对文件格式进行逆向工程已经取得了一些进展，导致部分规范解码。根据这些，EDB 文件包括：
* File Header - 包含数据库文件头信息
* Fixed Size Pages - 包含由表和索引组成的数据库

### 数据库文件头
数据库文件头位于第一个数据库页面中，并且至少为 668 字节。除了其他字段外，文件头还包含“文件格式版本"和“文件类型"。

＃＃＃＃ 文件类型
|类型|描述
---|---|
|0|数据库|
|1|流媒体|

`注意：` 这些类型的标识符是未知的。

#### 文件格式版本
EDB 的原始格式始于 1997 年 4 月，此后不断发展以应对变化。

|修订日期|版本|修订|说明
---|---|---|---|
|1997 年 4 月| 0x00000620|0x00000000|原版操作系统Beta格式。|
|1997 年 5 月 |0x00000620|0x00000001|在目录中添加用于条件索引和 OLD 的列。|
|1997 年 6 月|0x00000620|0x00000002|在 IDB 中添加 fLocalizedText 标志。|
|1997 年 10 月|0x00000620|0x00000003|将 SPLIT_BUFFER 添加到空间树根页面。|
|1998 年 1 月|0x00000620|0x00000002|恢复修订以使 ESE97 保持向前兼容。|
||0x00000620|0x00000003|将新的标记列添加到目录（“CallbackData"和“CallbackDependencies"）。|
|1998 年 5 月|0x00000620|0x00000004|超长值 (SLV) 支持：signSLV、fSLVExists 在 dbheader 中。|
|1998 年 5 月|0x00000620|0x00000005|新的 SLV 空间树。|
|1998 年 10 月|0x00000620|0x00000006|SLV 空间图。|
|1998 年 12 月|0x00000620|0x00000007|4 字节 IDXSEG。|
|1999 年 1 月|0x00000620|0x00000008|新模板列格式。|
|1999 年 6 月|0x00000620|0x00000009|已排序的模板列。用于 Windows XP SP3|
||0x00000620|0x0000000b|包含带有 ECC 校验和的页眉，用于 Exchange|
||0x00000620|0x0000000c|用于 Windows Vista (SP0)|
||0x00000620|0x00000011|支持 2 KiB、16 KiB 和 32 KiB 页面。带有额外 ECC 校验和的扩展页眉。列压缩。空间提示。用于 Windows 7 (SP0)|
|1999 年 5 月|0x00000623|0x00000000|新空间经理。|

### 数据库文件

EDB 数据库文件包含数据库中所有表的模式。此外，它还包括所有数据库表的记录和表的索引。它的位置由以下标识符确定。

* JetCreateDatabase
* JetCreateDatabase2
* JetAttach 数据库
* JetAttachDatabase2

基于这些，可以如下评估数据库的状态。

|值|标识符|描述
---|---|---|
|1|JET_dbstateJustCreated|刚刚创建数据库。|
|2|JET_dbstateDirtyShutdown|数据库需要运行硬恢复或软恢复才能变得可用或可移动。不应尝试在此状态下移动数据库。|
|3|JET_dbstateCleanShutdown|数据库处于干净状态。可以在没有任何日志文件的情况下附加数据库。|
|4|JET_dbstateBeingConverted|正在升级数据库。|
|5|JET_dbstateForceDetachInternal|此值在 WindowsXP 中引入|
 

## 参考
* [可扩展存储引擎（ESE）数据库文件（EDB）规范]（https://github.com/libyal/libesedb/tree/master/documentation）


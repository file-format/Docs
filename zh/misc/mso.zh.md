{
  "date" : "2022-03-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSO - Microsoft Office 宏参考文件",
  "description":"了解 MSO 文件和可以创建和打开 MSO 文件的 API。",
  "linktitle" : "MSO",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-03-12"
}

## 什么是一 .mso 文件？

MSO 文件是一种数据容器文件格式，在使用 Microsoft Outlook 发送 HTML 消息时创建。这主要发生在 Microsoft Office 2000 应用程序中。在大多数情况下，电子邮件会附加名称为 **Oledata.mso** 的文件。电子邮件收件人在打开此类电子邮件时，即使没有安装相同的软件，也可以正确查看文件。 MSO 文件参考 [Microsoft 复合文档文件格式 (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)。

## 微软 MSO 文件格式

MSO 文件以 Microsoft 复合文档文件格式 (MCDF) 保存，该格式也称为对象链接和嵌入 (OLE) 或组件对象模型 (COM) 结构化存储复合文件实现二进制文件格式。

### MSO 文件格式结构

MSO文件格式的内部文件格式结构在[结构](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd ) MCDF 文档的部分。文件分配表 (FAT) 管理扇区分配和扇区链。它包含一个 32 位扇区号数组。数组中的每个索引代表一个扇区号，而它的值代表链中的下一个扇区或一个特殊值。

## 参考

* [COM 结构化存储](https://en.wikipedia.org/wiki/COM_Structured_Storage)
* [Microsoft 复合文档文件格式 (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)


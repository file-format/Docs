{
  "date" : "2023-01-09",
  "keywords" :[ "ABCDDB", "什么是 ABCDDB 文件", "扩展名", "文件", "文件格式", "数据库文件类型", "数据库文件格式", "数据库文件" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 ABCDDB 文件格式和可以创建和打开 ABCDDB 文件的 API。",
  "title" :"ABCDDB 文件格式 - Apple 地址簿联系人列表数据库文件",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## 什么是一 ABCDDB 文件？

扩展名为 **.ABCDDB** 的文件代表 Apple Address Book Contact List Database。它属于 **Address Book** 应用程序，通常也称为 **Contacts**。它是一个内置应用程序，包含在 iOS 和 macOS 操作系统中。联系人应用程序使用户能够保存和组织与其联系人相关的信息，包括个人、企业和组织。这个应用程序允许用户跟踪姓名、地址、电话号码和电子邮件地址等详细信息，并将他们的联系人分组。

## 与 SQLite 的关系和典型路径

Apple 的地址簿（也称为联系人）将联系人信息作为 vCard 存储在元数据文件夹中。 **文件 _ABCDDB_ 实际上是 _SQLite 3 数据文件_**。

SQLite 是一种流行的数据库管理系统，它被设计为轻量级和独立的。它用于许多不同类型的软件和设备。 SQLite 是一种 RDBMS，这意味着它将数据存储在通过键相互关联的表中。它可以处理一系列数据类型，包括整数、浮点数、字符串和二进制数据。此外，SQLite 支持事务，使用户能够将多个数据库操作作为一个工作单元一起执行。

带有 ABCDDB 扩展名的文件通常存储在这里

`~/Library/Application Support/AddressBook/AddressBook-v22.abcddb`

## 修复损坏的联系人数据库

在尝试执行此操作之前，请先进行备份。那么请导航至

`~/Library/Application Support/AddressBook`

在该目录中，您将找到三个文件，包括扩展名为 .abcddb 的文件

- `addressbook-v22.abcddb`
- `addressbook-v22.abcddb-wal`
- `addressbook-v22.abcddb-shm`

删除所有这些文件并重新打开联系人，它将再次开始工作。

## 从备份恢复地址簿数据库

假设，您的 AddressBook 数据库联系人存储在 addressbook-v22.abcddb 中

- 首先备份您的地址簿数据并退出所有应用程序。
- 将您的数据库文件移动到 `~/Library/Application Support/AddressBook` 子目录
- 启动 **Address Book.app**。

## 将 ABCDDB 文件数据导出到 Microsoft Access

由于该文件是 SQLite 3 数据文件，您可以使用 ODBC 连接器将 abcddb 文件中的数据导出到 Microsoft Access。

SQLite ODBC 连接器是一个软件库和驱动程序，它使支持 ODBC 接口的应用程序能够连接到 SQLite 数据库。它包括一个定义 ODBC 接口的库，以及一个将此接口转换为对 SQLite API 的调用的驱动程序。要使用 SQLite ODBC 连接器，您必须先安装它，然后在您的计算机上设置 ODBC 数据源。完成这些步骤后，任何配备了 ODBC 支持的应用程序都将能够连接到数据源并从 SQLite 数据库中检索数据。

## 参考
* [修复损坏的联系人数据库](https://discussions.apple.com/docs/DOC-10581)
* [适用于 Mac 的联系人数据库](https://nitroreward.weebly.com/blog/contact-database-for-mac)
* [如何在 Windows 7 Excel 中打开或导出 abcddb 文件？](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file-in-windows-7-excel)


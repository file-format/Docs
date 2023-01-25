{
  "date" : "2023-01-17",
  "keywords" :[ "DSN", "什么是 DSN 文件", "扩展名", "文件", "文件格式", "数据库文件类型", "数据库文件格式", "数据库文件" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 DSN 文件格式和可以创建和打开 DSN 文件的 API。”,
  "title" :"DSN 文件格式 - 数据库源名称文件”，
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## 什么是一 .dsn 文件？

DSN代表“数据源名称”，它是一种用于存储数据库连接信息的文件格式。 DSN 文件通常与 ODBC（开放式数据库连接）结合使用，并允许通过提供连接到特定数据库的必要信息（例如服务器名称、用户名和密码）轻松访问特定数据库。该文件通常为纯文本格式，可以使用文本编辑器创建和编辑。它可以在 Windows、Linux 和 Mac 等各种操作系统上使用。

## 如何创建 DSN 文件？

创建 DSN 文件的方法可能因操作系统和可用工具而异。以下步骤概述了在 Windows 系统上创建 DSN 文件的过程。

1. 通过在开始菜单中搜索“ODBC 数据源”来打开 ODBC 数据源管理器。
2. 选择“系统DSN”选项卡并单击“添加”按钮。
3. 为要连接的数据库选择合适的驱动程序，然后单击“完成”。
4. 填写连接数据库的必要信息，例如服务器名称、用户名和密码。
5. 单击“确定”保存 DSN 文件。

或者，您可以通过创建扩展名为 .dsn 的纯文本文件并以以下格式输入必要的连接信息来手动创建 DSN 文件：

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

然后，您可以使用此文件的路径作为代码/脚本中的 DSN 来连接到数据库。

## 打开 DSN 文件的程序

DSN 文件是一个纯文本文件，它存储用于连接到数据库的信息，例如服务器名称、用户名和密码。它通常与 ODBC（开放式数据库连接）结合使用，以提供对特定数据库的轻松访问。

要打开和查看 DSN 文件的内容，您可以使用任何文本编辑器，例如记事本、Sublime Text、Atom 等。这些程序将允许您打开 DSN 文件并查看其中存储的连接信息。

但是，要使用 DSN 文件连接到数据库并执行 SELECT、INSERT、UPDATE、DELETE 等操作，需要支持 ODBC 的程序，例如 Python、Java、C# 等编程语言或 Microsoft Access 等数据库管理工具, SQL Server Management Studio 是必需的。这些程序可以使用 DSN 文件中的信息连接到数据库并执行所需的操作。

## 参考
* [什么是 DSN（数据源名称）？](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30- 606e-2436fe26e89f)
* [如何创建文件 DSN 以用作 ODBC 导入的数据源？](https://www.ibm.com/support/pages/how-do-i-create-file-dsn-use-data-源 odbc 导入）


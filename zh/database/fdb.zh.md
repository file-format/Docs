{
  "date" : "2023-01-18",
  "keywords" :[ "FDB", "什么是 FDB 文件", "扩展名", "文件", "文件格式", "数据库文件类型", "数据库文件格式", "数据库文件" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 FDB 文件格式和可以创建和打开 FDB 文件的 API。”,
  "title" :"FDB 文件格式 - Microsoft Dynamics NAV 数据库文件”，
  "linktitle" : "FDB",
  "menu" : {
    "docs" : {
      "identifier":"database-fdb",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-18"
}

## 什么是一 .fdb 文件？

.fdb 文件是用于 Microsoft Dynamics NAV 中的数据库文件的文件扩展名。 .fdb 文件扩展名代表“Firebird 数据库文件”，它是 Firebird 数据库管理系统使用的文件格式，它是 Microsoft Dynamics NAV 使用的基础数据库引擎。 .fdb 文件包含 NAV 系统的所有数据、表格和结构，包括财务数据、库存数据、客户数据等。保留 .fdb 文件的备份非常重要，以确保数据完整性并能够在出现任何问题时恢复数据。 .fdb 文件可以导出、导入，也可以用于复制。

## 与 Microsoft Dynamics NAV 的关系

FDB 文件是 Microsoft Dynamics NAV 中的数据库文件。 Microsoft Dynamics NAV 是 Microsoft 开发的企业资源规划 (ERP) 软件。它专为中小型企业设计，提供广泛的业务管理功能，包括财务管理、供应链管理、制造、项目管理等。它建立在 Microsoft Dynamics 平台之上，并与其他 Microsoft 产品（如 Office 和 Outlook）完全集成。 Dynamics NAV 可以通过 Web 客户端和 Windows 客户端访问，还可以使用自己的开发环境 C/AL 进行定制和与其他系统集成。它通常被制造、批发分销和服务行业的公司使用。

## .fdb 文件怎么打开？

FDB 文件通常使用 Microsoft Dynamics NAV 开发环境或 Microsoft Dynamics NAV 客户端打开和管理。

以下是在 Microsoft Dynamics NAV 中打开 .fdb 文件的步骤：

1. 打开 Microsoft Dynamics NAV 开发环境。
2. 单击“文件”菜单并选择“打开”或按“Ctrl+O”
3. 导航到保存 .fdb 文件的位置。
4. 选择.fdb 文件并单击“打开”按钮。

您还可以通过使用 NAV 客户端连接到数据库来打开 .fdb 文件。

1. 打开导航客户端。
2.点击“文件”菜单，选择“连接”
3. 在“服务器”字段中，输入.fdb 文件所在服务器的名称或IP 地址。
4. 输入适当的“数据库名称”和“凭据”
5. 单击“连接”按钮。

也可以使用 Firebird 数据库管理系统管理软件打开 .fdb 文件，因为它是 Microsoft Dynamics NAV 使用的底层数据库引擎。

## 参考
* [微软动态导航](https://dynamics.microsoft.com/en-us/nav-erp/)
* [如何在 Dynamics NAV 中添加新的数据库文件](https://learn.microsoft.com/en-us/dynamics-nav/how-to--add-new-database-files)


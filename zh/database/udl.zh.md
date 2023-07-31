{
  "date" : "2021-06-21",
  "keywords" :["UDL","扩展名","udl 文件","udl 文件格式","数据库文件类型","数据库文件格式","什么是 udl 文件"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 UDL 文件格式和可以创建和打开 UDL 文件的 API。",
  "title" :"UDL - 微软通用数据链接文件",
  "linktitle" : "UDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-21"
}

## 什么是一 .udl 文件？
扩展名为 .udl 的文件称为 Microsoft 通用数据链接文件；指定连接属性； Windows 应用程序使用它来建立与数据库的连接。 UDL 文件包含 OLE DB 数据源的连接字符串；具有用户名和密码以及基本的连接字符串属性。为避免在连接字符串中直接手动指定属性，可以使用“数据链接属性"对话框将连接信息保存在 .udl 文件中作为替代方法。

## UDL 文件格式
基本上，UDL（通用数据链接）文件是一个简单的文本文件，由具有特定属性或属性的数据库连接字符串组成。创建 UDL 文件后，可以使用 SQL Server Management Studio 对其进行测试，以验证连接性。

### 连接字符串属性
可以在 UDL 中设置以下属性以确保正确连接：

- **服务器名称**：您要访问的数据库所在服务器的位置。
- **身份验证选项**
- **Windows 身份验证**：使用当前登录用户的 Windows 帐户凭据对 SQL Server 进行身份验证。
- **SQL Server 身份验证**：使用登录 ID 和密码进行身份验证。
- **Active Directory - 集成**：使用 Azure Active Directory 身份进行集成身份验证；也可用于对 SQL Server 的 Windows 身份验证。
- **Active Directory - 密码**：使用 Azure Active Directory 身份验证用户 ID 和密码。
- **Active Directory - 支持 MFA 的通用**：使用 Azure Active Directory 身份进行交互式身份验证。
- **Active Directory - 服务主体**：使用 Azure Active Directory 服务主体进行身份验证。
- **服务器 SPN**：如果您使用受信任的连接，则可以为服务器指定服务主体名称 (SPN)。
- **用户名**：输入登录数据源时用于身份验证的用户 ID。
- **密码**：输入登录数据源时用于身份验证的密码。
- **空白密码**：选中后，允许指定的提供程序在连接字符串中使用空白密码。
- **允许保存密码**：允许将密码与连接字符串一起保存。
- **对数据使用强加密**：通过连接传递的数据将被加密。
- **信任服务器证书**：将验证服务器的证书。
- **数据库**：您要访问的数据库名称。
- **附加数据库文件作为数据库名称**：指定可附加数据库的主文件的名称。

## 参考 ＃＃

* [Microsoft 数据访问组件](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)
* [通用数据链接 (UDL) 配置](https://learn.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)


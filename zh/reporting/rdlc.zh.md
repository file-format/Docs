{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDLC - 报告定义语言客户端",
  "keywords" :["rdlc","报告定义语言","mkv格式","XSD","报告定义语言客户端"],
  "description":"了解 RDLC 文件格式,它是 SQL Server Reporting Services 报告定义的 XML 表示形式。",
  "linktitle" : "RDLC",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## 什么是一 .rdlc 文件？ ##

RDLC 代表报告定义语言客户端。实际上它是使用微软报告技术创建的报告文件的扩展。 SQL Server 2005 版本的报表设计器用于创建这些文件。客户端的**ReportViewer**控件可以直接执行RDLC报表。

## RDL 与 RDLC 文件
|.rdl 文件 |.rdlc 文件|
---|---|
|RDL 文件由报表设计器的 SQL Server 2005 版本创建|RDLC 文件由报表设计器的 Visual Studio 2005 版本创建|
|在 SQL Server Reporting Services 中使用|在 Visual Studio 中使用|
|是远程报告|是本地报告|
|需要 Reporting Services 实例来运行它|不需要 Reporting Services 实例|

## 创建客户端报告定义 (.rdlc) 文件
ReportViewer 控件用于使用控件的内置处理能力运行客户端报表定义 (.rdlc) 文件。您在本地处理模式下运行的客户端报告可以在您的应用程序项目中轻松创建。以下是创建报告的方法：

- 使用**报告向导** 创建新的客户端报告定义 (.rdlc)。

- 使用 Visual Studio 创建新的客户端报告定义 (.rdlc) 文件。

- 以编程方式生成报告定义。


您只能通过在 **ReportViewer** 控件中运行报表来预览报表。请注意，您可以随时打开和编辑报表定义，然后构建或部署应用程序以检查结果。

## 参考 ＃＃

- [创建客户端报告定义 (.rdlc) 文件](https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/ms252067(v=vs.100))


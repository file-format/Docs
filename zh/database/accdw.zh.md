{
  "date" : "2021-08-30",
  "keywords" :["ACCDW","扩展名","文件","文件格式","数据库文件类型","数据库文件格式","数据库文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 ACCDW 文件格式和可以创建和打开 ACCDW 文件的 API。",
  "title" :"ACCDW - Microsoft Access 数据库链接文件",
  "linktitle" : "ACCDW",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-30"
}

## 什么是一 .acdw 文件？

带有 .accdw 扩展名的文件是使用 Microsoft Access 创建的链接文件，其中包含有关从 SharePoint 服务器下载 Access 数据库文件即 [ACCDB](/zh/database/accdb/) 的链接的信息。这使用户可以共享远程托管的数据库文件。打开 ACCDW 文件会将链接的 ACCDB 文件下载为用户计算机上的本地副本。下载的文件将保存到默认下载位置，并且可以通过导航到该位置进行访问。通常，这些文件以引用客户端数据库的名称“SiteServer.accdb"下载和存储。

## ACCDW 文件格式 - 更多信息

ACCDW 文件是一个 XML 文件，它提供指向托管 Access Services 的 SharePoint 站点的链接。它只是一个快捷方式，需要互联网连接才能运行它们。在联机的情况下，SharePoint 会在本地缓存，以便提供稍后将其脱机的选项。

## 参考

* [Access 2016 规范](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [下载 .accdw 文件](https://social.technet.microsoft.com/Forums/en-US/7bf02e9e-6246-44da-9513-4cf8f2cc2fb2/downloaded-accdw-file)
* [我应该使用哪种 Access 文件格式？](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?ui=en-us&rs=en-us&ad=us)


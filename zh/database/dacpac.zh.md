{
  "date" : "2021-09-06",
  "keywords" :["dacpac","扩展名","文件","文件格式","数据库文件类型","数据库文件格式","数据层应用程序包"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 DACPAC 文件格式和可以创建和打开 DACPAC 文件的 API。",
  "title" :"DACPAC - 数据层应用程序包",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## 什么是一 .DACPAC 文件？

带有 .dacpac（代表数据层应用程序包）扩展名的文件是一个数据库文件，由 Microsoft SQL Server 数据层应用程序创建，其中包含用于表示数据库对象的数据库模型。由于它包含数据库的完整模型，因此它用于从模型中可用的详细信息中恢复数据库。 DACPAC 文件通常移交给部署团队，以便在客户场所安装以恢复数据库。这些可以打开
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019?ranMID=24542&ranEAID=4LioSo*jxMc&ranSiteID=4LioSo.jxMc-XSp30B6cXpiTS89wo0jYzw&epi=4LioSo.jxMc-XSp30B6cXpiTS89wo0jYzw&ir =1&OCID=AID2200057_aff_7593_1243925&tduid=%28ir__gn1tqusqf0kf6whl2qniaboutn2xruqfmyy1hzec00%29%287593%29%281243925%29%284LioSo.jxMc-XSp30B6cXpiTS89wo0jYzw%29%28%29&irclickid=_gn1tqusqf0kf6whl2qniaboutn2xruqfmyy1hzec00).

## DACPAC 文件格式 - 更多信息

DACPAC 数据包文件实际上是压缩的 ZIP 文件，其中包含几个 [XML](/zh/web/xml/) 文件，其中包含有关数据库模型的信息，例如用于恢复数据库的表和视图。为了查看 DACPAC 文件的内容，将文件从 .dacpac 重命名为 [.zip](/zh/compression/zip/) 并使用任何解压缩实用程序提取 zip 存档。

以下是在 DACPAC 文件中找到的几个文件。

* [内容类型].xml
```
<?xml version="1.0" encoding="utf-8"?>
<Types
xmlns="http://schemas.openxmlformats.org/package/2006/content-types">
<Default Extension="xml" ContentType="text/xml" />
</Types>
```
* DacMetadata.xml

```
<?xml version="1.0" encoding="utf-8"?>
<DacType xmlns="http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02">
<Name>客户关系管理</Name>
<Version>1.0.0.0</Version>
</DacType>
```
* 起源.xml

* 模型.xml

需要注意的是，DACPAC 不包含 DATA 和其他服务器级对象。该文件可以包含可能保存在 SSDT 项目中的所有对象类型。

## 参考

* [数据层应用程序 - 好处](https://docs.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications?view=sql-server-ver15)
* [部署数据层应用程序 - Microsoft](https://docs.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [如何创建 DACPAC 文件？](https://sqlplayer.net/2018/10/how-to-create-dacpac-file/)


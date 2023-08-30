{
  "date" : "2020-11-11",
  "keywords" :["DTSX","扩展名","文件","文件格式","数据库文件类型","数据库文件格式","数据库文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 DTSX 文件格式和可以创建和打开 DTSX 文件的 API。",
  "title" :"DTSX 文件格式 - SQL Server DTS 设置文件",
  "linktitle" : "DTSX",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## 什么是一 .DTSX 文件？

具有 .dtsx（数据转换服务包 XML）扩展名的文件是一种数据转换服务 (DTS) 文件，Microsoft SQL 使用该文件来引用将数据从一个数据库传输到另一个数据库的数据迁移步骤/规则。这包括在起始点和目的地点之间的数据传输期间可能需要的转换和任何可选处理步骤。 SQL Server Integration Services (SSIS) 是 Microsoft SQL Server 的一个组件，它使用 DTSX 文件来识别在数据库服务器之间处理数据的步骤。 DTSX 文件可以使用 Microsoft SQL Server 2019 打开。

## DTSX 文件格式

数据库服务器之间的数据移动需要规则和处理步骤来确保此操作期间数据的完整性。 SSIS 确保所有这些活动，从企业中的不同来源移动和整合数据，都可以方便地进行。这就是 DTSX 出现的地方，它定义了 SSIS 使用的结构，以建立可以处理数据的步骤，因为它遵循这些步骤。

DTSX 描述的数据流如下图所示。

{{< figure src="../DataFlowDTSX.png" alt="数据流 DTSX" >}}

DTSX 基于 [XML](/zh/web/xml/) 并记录在 [MS-DTSX](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)。 DTSX XML 的增强重构是 DTSX 2.0，它包括结构的新属性、将命名属性替换为父 XML 属性、指定大多数属性值的默认值以及在父元素内放置重复元素。 DTSX 结构使用这些 [XML 模式](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc) 描述，结构格式为明文 XML。

## 参考

* [DTSX 格式 - 微软](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
* [DTSX 2 格式 - Microsoft 提供](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)


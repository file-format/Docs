{
  "date" : "2020-11-11",
  "keywords" :["NSF","扩展名","文件","文件格式","数据库文件类型","数据库文件格式","数据库文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 NSF 文件格式和可以创建和打开 NSF 文件的 API。",
  "title" :"NSF 文件格式 - Lotus Notes 数据库格式",
  "linktitle" : "NSF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## 什么是一 .nsf 文件？

扩展名为 .nsf（Notes Storage Facility）的文件是 [IBM Notes 软件](https://en.wikipedia.org/wiki/HCL_Domino) 使用的数据库文件格式，以前称为 Lotus Notes。它定义了存储不同类型对象的模式，例如电子邮件、约会、文档、表单和视图。所有这些信息都包含在一个用于业务协作的 NSF 文件中，类似于 PST/OST 文件。一些可以打开 NSF 文件的应用程序包括 IBM Lotus Notes 和 IBM Domino。

## NSF 文件格式规范

NSF 文件本质上是二进制文件，它们的规范由 Joachim Metz 在 [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)。根据这些详细信息，NSF 文件包括：

* 文件头
* 数据库头

此外，它包括：

* 超级块
* 桶描述符块
* 位图
* 记录重定位向量桶
* 摘要桶
* 非汇总桶


### NSF 文件头

NSF 文件头大小为 6 个字节。它包括：

|偏移量|大小|值|描述|
---|---|---|---|
0|2|0x1a 0x00|签名|
2|4| |数据库头大小|

### 数据库头

NSD 数据库标头包含以下已确认的值。

* 数据库信息
* 数据库标识符（DBID）
* 复制信息
* 数据库信息缓冲区标志
* 标题
* 类别
* 班级
* 设计类（模板名称）
* 特别说明标识符
* 填充
* 数据库信息2
* 数据库信息 3
* 数据库信息 4
* 数据库信息 5
* 填充
* 数据库实例标识符（DBIID）
* 复制历史

## 参考

* [NSF 格式 - Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)


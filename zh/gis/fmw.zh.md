{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FMW 文件 - FME 工作台文件格式",
  "description":"了解 FMW 文件格式和可以创建和打开 FMW 文件的 API。",
  "linktitle" : "FMW",
  "menu" : {
    "docs" : {
      "identifier":"gis-fmw",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## 什么是一 FMW 文件？

FMW 文件是使用 FME Workbench 软件（作为 FME 桌面套件的一部分）创建的项目文件，用于空间数据转换。它包含用于空间数据操作的用户定义设置，例如输入数据集、翻译属性、投影和输出设置。空间数据操作设置存储为可视布局，易于编辑和再次保存。

您可以使用 [Safe Software FME Desktop](https://fme.safe.com/platform/) 打开 FMW 文件。

## FMW 文件格式 - 更多信息

FMW 文件作为二进制文件存储在光盘上，只能使用 FME Desktop 软件读取。该软件还可以从多种关系数据库格式中读取数据，还支持多种数据格式。

### FMW 速览

|事实|价值|
---|---|
|读者/作家|读者|
|许可级别|基础|
|依赖项|无|
|数据集类型|文件|
|特征类型|固定|
|典型的文件扩展名|.fmw|
|自动翻译支持|是|
|用户定义的属性|否|
|坐标系统支持|否|
|通用颜色支持|否|
|空间索引|无|
|需要架构|否|
|交易支持|否|
|几何类型属性|无|
|编码支持|否|

### FMW 几何支持

|几何|支持？|
---|---|
|聚合|否|
|圈子|没有|
|圆弧|无|
|甜甜圈多边形|没有|
|椭圆弧|无|
|省略号|没有|
|行|没有|
|无|是|
|点|没有|
|多边形|没有|
|光栅|没有|
|固体|没有|
|表面|没有|
|文本|否|
|z 值|没有|


## 参考

* [安全软件 FME 桌面](https://fme.safe.com/platform/)
* [FMW 简介](https://docs.safe.com/fme/html/FME_Desktop_Documentation/FME_ReadersWriters/fmw/quick_facts_fmw.htm)

